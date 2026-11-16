---
type: method
aliases: [Cross-validation, k-fold cross-validation, 交叉驗證, 10 折交叉驗證, internal validation, 內部驗證]
---
# 交叉驗證（Cross-validation）

## 白話解釋
把資料分成 10 份，輪流拿 1 份當考卷、其他 9 份當練習題，做 10 次再平均成績。這樣每筆資料都被考過一次，比只切一次更穩定。屬於**內部驗證**（資料都來自同一批）。

## 在文獻中怎麼被使用
- [[kausch2024apnea]]：10 折交叉驗證計算 AUC（cvAUC）；完整模型 0.783（PDF p.5, p.18）。
  - ⚠️ 推論：只有內部驗證，沒有在其他醫院的資料上測試。

## 和外部驗證的差別
| | 交叉驗證（內部） | [[external-validation|外部驗證]] |
|---|---|---|
| 測試資料 | 同一批資料切出來的 | 另一家醫院／另一段時間 |
| 能回答 | 模型在「這批人」準不準 | 模型換地方還準不準 |
| 例子 | [[kausch2024apnea]] | [[lin2022point]] |

## 相關頁面
[[external-validation]]、[[roc-auc]]、[[time-series-outcome-labeling]]
