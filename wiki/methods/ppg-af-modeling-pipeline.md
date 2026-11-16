---
type: method
aliases: [PPG modeling pipeline, AF detection pipeline, 穿戴裝置建模流程, 自己跑模型]
---
# 穿戴裝置 PPG 偵測心房顫動：自己跑模型的流程

> 本頁除標註來源者外，皆為 ⚠️ 推論（一般做法）。[[lubitz2022detection]] 未公開演算法細節與資料。

## 白話總覽
```
收資料 → 清訊號 → 切段 → 算特徵 → 每段分類 → 合併判定 → 和心電圖對答案 → 算 PPV／敏感度
```

## 步驟與技術
| 步驟 | 要做什麼 | 常用技術／工具 | 文獻做法 |
|---|---|---|---|
| 1. 取得資料 | PPG 波形、加速度計、同步心電圖標註 | 公開資料庫（需查證是否含 PPG + AF 標註，如 PhysioNet）或自行收案 | Fitbit 資料不公開（p.1416） |
| 2. 前處理 | 濾波、偵測脈搏峰值、算脈搏間隔 | 帶通濾波；Python SciPy、NeuroKit2、HeartPy | — |
| 3. 品質控制 | 去除動作與訊號品質差的片段 | 加速度計門檻、訊號品質指標 | 只用靜止時段（p.1416） |
| 4. 切視窗 | 固定長度、重疊 | pandas、NumPy | 5 分鐘、重疊 50%（p.1416） |
| 5. 特徵 | 心律不規則程度 | RMSSD、pNN50、SDNN、樣本熵、Shannon 熵、Poincaré 指標 | 未公開 |
| 6. 模型 | 每段是否不規則 | 邏輯斯迴歸、隨機森林、XGBoost（scikit-learn、xgboost）；1D CNN、LSTM（PyTorch、TensorFlow） | 未公開 |
| 7. 彙總 | 連續 N 段陽性才通知 | 規則式後處理 | N = 11（p.1416） |
| 8. 標籤對齊 | PPG 與心電圖時間同步 | 時間戳對齊、加緩衝 | ±1 分鐘（p.1417） |
| 9. 資料切分 | 訓練／驗證／測試 | **以「人」為單位切分**，避免同一人同時在訓練與測試 | — |
| 10. 評估 | 診斷表現 | PPV、敏感度、特異度、Clopper-Pearson CI（statsmodels） | p.1417–1418 |
| 11. 軟體 | — | Python、R | Python 3.7、R 4.1.0（p.1418） |
| 12. 運算環境 | 大量資料 | 雲端或伺服器 | 中央伺服器運算（p.1416） |

## 常見難點
- 動作雜訊、配戴鬆緊、膚色差異影響 PPG 品質。
- 心電圖標註昂貴；陣發性 AF 讓「參考標準」也可能漏抓。
- 類別不平衡（AF 只佔少數），PPV 受盛行率影響（見 [[sensitivity-specificity-ppv-npv]]）。
- 隱私與資料取得（需 IRB、知情同意）。

## 相關頁面
[[sliding-window]]、[[photoplethysmography]]、[[cross-validation]]
