---
type: method
aliases: [Mixed-effects Logistic Regression, GLMM, 混合效應模型, 廣義線性混合模型]
---
# 混合效應邏輯斯迴歸（Mixed-effects Logistic Regression）

## 白話解釋
- **邏輯斯迴歸**：預測「是／否」的結果（例如：有沒有幻覺），並看哪些因素讓「是」的機會變高或變低。
- **混合效應**：同一個病例被測了很多次（不同模型、不同條件），這些結果彼此有關聯。混合效應模型會把「這題本身比較難」的影響考慮進去，避免誤判。

## 在文獻中怎麼被使用
- [[omar2025multi]]：結果為幻覺（是／否），每個病例設為隨機截距；固定效應為溫度、防護指令、長短版；結果以 [[odds-ratio|OR]] 與 95% CI 呈現（p.3）。
- 多重比較用 Bonferroni 校正（p.3）。

## 相關頁面
[[odds-ratio]]
