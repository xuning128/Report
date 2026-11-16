# 知識庫目錄 (Index)

> 每次 ingest 後更新。格式：`[[頁名]]` — 一行摘要
> 文獻數：5｜最後更新：2026-11-16

## 文獻 (papers)
- [[omar2025multi]] — LLM 在臨床病例中被植入假資訊時，幻覺率 50–82%；防護指令可降到 44%（風險／限制類）
- [[ada2026prevention]] — ADA 2026 糖尿病預防指引：糖尿病前期切點、第 2 型風險因子、介入效果（領域知識）
- [[lin2022point]] — 台灣三總 AI 心電圖估血鉀：外部驗證、黑盒子實用研究、偽陽性預後差（核心文獻）
- [[kausch2024apnea]] — Pre-Vent 極早產兒：床邊監視器心肺事件預測晚發性敗血症；時間序列標記範本（核心文獻）
- [[lubitz2022detection]] — Fitbit 心臟研究：穿戴裝置 PPG 偵測心房顫動，PPV 98%；滑動視窗範本、自己跑模型的技術清單（核心文獻）

## 概念 (concepts)
- [[large-language-model]] — 大型語言模型 (LLM)
- [[llm-hallucination]] — 幻覺：AI 編造不存在的資訊
- [[adversarial-attack]] — 對抗式攻擊：故意設陷阱考 AI
- [[clinical-decision-support]] — 臨床決策支援 (CDS)
- [[sycophancy]] — 迎合傾向：AI 順著使用者講
- [[retrieval-augmented-generation]] — 檢索增強生成 (RAG)
- [[prediabetes]] — 糖尿病前期
- [[t2d-risk-factors]] — 第 2 型糖尿病風險因子（預測特徵候選）
- [[diabetes-prevention-program]] — 美國糖尿病預防計畫 (DPP)
- [[type-1-diabetes-stages]] — 第 1 型糖尿病分期
- [[metformin]] — 二甲雙胍
- [[dyskalemia]] — 血鉀異常（低鉀／高鉀）
- [[electrocardiogram]] — 心電圖
- [[ai-enabled-ecg]] — AI 心電圖
- [[deep-learning]] — 深度學習、卷積神經網路
- [[late-onset-sepsis]] — 晚發性敗血症
- [[preterm-infant]] — 極早產兒與年齡算法（GA、PMA、PNA）
- [[cardiorespiratory-events]] — 新生兒心肺事件（呼吸暫停、低血氧、心跳過慢）
- [[continuous-physiological-monitoring]] — 床邊連續生理監測
- [[atrial-fibrillation]] — 心房顫動
- [[photoplethysmography]] — PPG、脈搏間隔序列
- [[wearable-devices]] — 穿戴裝置
- [[cha2ds2-vasc]] — CHA₂DS₂-VASc 中風風險分數

## 方法與指標 (methods)
- [[mitigation-prompt]] — 防護指令／提示工程
- [[temperature]] — 溫度參數
- [[simulated-clinical-vignettes]] — 模擬病例（可模仿的研究設計）
- [[llm-as-judge]] — 用 LLM 自動批改
- [[mixed-effects-logistic-regression]] — 混合效應邏輯斯迴歸
- [[odds-ratio]] — 勝算比與信賴區間
- [[hazard-ratio]] — 風險比 (HR)
- [[person-years]] — 人年與發生率
- [[glycemic-tests]] — 血糖檢查：A1C、空腹血糖、OGTT、CGM
- [[evidence-grading]] — 指引的證據等級
- [[external-validation]] — 外部驗證 ⭐
- [[black-box-pragmatic-study]] — 黑盒子實用研究 ⭐
- [[roc-auc]] — ROC 曲線與 AUC
- [[sensitivity-specificity-ppv-npv]] — 敏感度、特異度、PPV、NPV（含盛行率說明）⭐
- [[c-index]] — C-index
- [[cox-regression]] — Cox 比例風險模型、存活分析
- [[mean-absolute-error]] — 平均絕對誤差
- [[multiple-imputation]] — 多重插補
- [[time-series-outcome-labeling]] — 時間序列資料的結果標記 ⭐
- [[static-vs-dynamic-risk-markers]] — 持續型 vs. 變化型風險訊號
- [[cross-validation]] — 交叉驗證（內部驗證）
- [[calibration]] — 校準度
- [[pseudo-r-squared]] — McFadden's pseudo R²
- [[clustered-standard-errors]] — 群集穩健標準誤（Huber-White）
- [[tripod-reporting]] — TRIPOD 報告規範
- [[sliding-window]] — 滑動視窗與「連續 N 段」規則 ⭐
- [[ppg-af-modeling-pipeline]] — 穿戴裝置 PPG 自己跑模型的流程 ⭐

## 資料集 (datasets)
- [[tsgh-ed-ecg-cohort]] — 三軍總醫院急診心電圖世代（未公開）
- [[pre-vent-cohort]] — Pre-Vent 美國 5 家 NICU 極早產兒監測世代
- [[fitbit-heart-study]] — Fitbit Heart Study（個人資料不公開）

## 關鍵字 (keywords)
- [[kw-llm-hallucination]] — LLM 幻覺
- [[kw-adversarial-attack]] — 對抗式攻擊
- [[kw-clinical-decision-support]] — 臨床決策支援
- [[kw-prompt-engineering]] — 提示工程
- [[kw-prediabetes]] — 糖尿病前期
- [[kw-diabetes-prevention]] — 糖尿病預防
- [[kw-diabetes-risk-factors]] — 糖尿病風險因子
- [[kw-ai-ecg]] — AI 心電圖
- [[kw-dyskalemia]] — 血鉀異常
- [[kw-deep-learning-prediction]] — 深度學習預測模型
- [[kw-neonatal-sepsis]] — 新生兒敗血症
- [[kw-preterm-infant]] — 早產兒
- [[kw-physiological-monitoring-prediction]] — 生理監測資料預測
- [[kw-atrial-fibrillation]] — 心房顫動
- [[kw-wearable-devices]] — 穿戴裝置
- [[kw-ppg]] — PPG

## 綜合分析 (synthesis)
- [[overview]] — 領域全貌
- [[contradictions]] — 文獻間矛盾
- [[research-gaps]] — 研究缺口
- [[research-questions]] — 研究問題

## 其他
- [[glossary]] — 術語白話表
- [[log]] — 工作紀錄
