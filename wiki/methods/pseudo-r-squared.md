---
type: method
aliases: [McFadden's pseudo R-squared, pseudo R2, log loss, 偽 R 平方, 對數損失]
---
# McFadden's pseudo R²（模型配適度）

## 白話解釋
衡量模型「整體解釋了多少」，0 = 跟什麼都不知道一樣，越接近 1 越好。邏輯斯迴歸沒有一般的 R²，所以用這個代替。數值通常很小，0.2–0.4 就算很好（⚠️ 推論：常見經驗說法）。
- **log loss（對數損失）**：模型給的機率和真實結果差多少，越小越好。

## 在文獻中怎麼被使用
- [[kausch2024apnea]]：以 log loss 評估配適，並換算成 McFadden's pseudo R²（PDF p.5）；逐步加入變項後從 0.067 升到 0.094（PDF p.18）。

## 相關頁面
[[calibration]]、[[roc-auc]]
