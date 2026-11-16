---
type: concept
aliases: [AI-ECG, AI-enabled ECG, AI 心電圖, ECG-K+]
---
# AI 心電圖（AI-enabled ECG）

## 白話解釋
讓 AI 讀心電圖，找出人眼看不出來的細微變化，用來估計血液數值（如血鉀）或預測疾病。

## 在文獻中怎麼被使用
- [[lin2022point]]：ECG12Net 從心電圖估算血鉀（ECG-K+），比抽血早約 40 分鐘（p.2）；「抽血正常但 AI 判異常」的病人預後較差，可能反映潛在心臟問題（p.4, p.9）。
- 作者提出應用：在急診背景中，對每張 ECG 自動計算 ECG-K+（p.9）。
- 其他研究（作者引用）：AI-ECG 可偵測左心室收縮功能不良、心房顫動、估算 HbA1c（p.8, p.11）。

## 優點／限制
- 優點：簡單、便宜、非侵入、快速（p.9）。
- 限制：黑盒子、族群差異、PPV 受盛行率影響（p.7, p.10）。

## 相關頁面
[[electrocardiogram]]、[[deep-learning]]、[[clinical-decision-support]]
