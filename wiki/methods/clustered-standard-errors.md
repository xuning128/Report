---
type: method
aliases: [Huber-White, Robust standard errors, Cluster-robust variance, 群集穩健標準誤, 重複測量]
---
# 群集穩健標準誤（Huber-White 法）

## 白話解釋
同一個寶寶每天都有一筆資料，這些資料彼此很像（同一個人）。如果當作互相獨立，會**高估**統計顯著性。Huber-White 法調整標準誤，把「同一個人（或同一家手足）」當成一群來處理。
- 和 [[mixed-effects-logistic-regression|混合效應模型]]目的相似，都是處理重複測量，但做法不同。

## 在文獻中怎麼被使用
- [[kausch2024apnea]]：所有單變項與多變項邏輯斯迴歸都以 Huber-White 法調整，群集包含個別病人與手足（PDF p.5）。
- [[omar2025multi]] 處理類似問題用的是混合效應模型（p.3）。

## 相關頁面
[[time-series-outcome-labeling]]、[[mixed-effects-logistic-regression]]
