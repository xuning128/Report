---
type: method
aliases: [Cox proportional hazards model, Cox regression, Cox 迴歸, 存活分析, survival analysis, Kaplan-Meier, censoring, 設限]
---
# Cox 比例風險模型（Cox Proportional Hazards Model）

## 白話解釋
- **存活分析**：不只看「有沒有發生事件」，也看「多久之後發生」。
- **Cox 模型**：同時考慮多個因素（年齡、檢驗值等），算出每個因素的[[hazard-ratio|風險比 (HR)]]。
- **設限 (censoring)**：追蹤結束時還沒發生事件、或中途失去聯絡的人，不能當作「沒發生」，要特別處理。
- **Kaplan-Meier 曲線**：畫出各組隨時間的存活比例。

## 在文獻中怎麼被使用
- [[lin2022point]]（p.10–11）：用 Cox 模型分析 ECG-K+、抽血血鉀與死亡的關係；用 pspline 檢驗 U 型關係；存活者在最後一次就醫時設限；分三層調整（人口學 → 病史 → 檢驗值）。

## 相關頁面
[[hazard-ratio]]、[[c-index]]
