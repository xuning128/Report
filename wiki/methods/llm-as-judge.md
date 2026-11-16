---
type: method
aliases: [LLM-as-a-judge, 自動分類, LLM 評審]
---
# LLM 當評審（LLM-as-a-Judge）

## 白話解釋
用一個 AI 去批改另一個 AI 的答案，省下大量人工。但需要人工抽查，確認 AI 評審改得準。

## 在文獻中怎麼被使用
- [[omar2025multi]]：用 GPT-4o 判斷 5,400 個輸出是否為幻覺；兩位醫師隨機抽查 200 筆，一致率 100%（p.2–3）。

## 優點／限制
- 優點：可評估大量輸出、人力需求少（[[omar2025multi]] p.5）。
- ⚠️ 推論：評審模型若同時是受測模型（如 GPT-4o），可能有偏袒自己的風險。

## 相關頁面
[[simulated-clinical-vignettes]]
