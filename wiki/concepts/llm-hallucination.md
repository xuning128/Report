---
type: concept
aliases: [Hallucination, AI 幻覺, 幻覺]
---
# 幻覺（Hallucination）

## 白話解釋
AI 一本正經地講出不存在的事。像一個不想說「我不知道」的學生，乾脆編一個聽起來很合理的答案。

## 正式定義
- 一般定義：產生無意義或與來源內容不一致的內容（[[omar2025multi]] p.5，引用 Ji et al., 2023）。
- [[omar2025multi]] 的操作型定義：回答中延伸、認可或把刻意植入的假元素當成真的（p.2）。

## 在文獻中怎麼被使用
- [[omar2025multi]]：在臨床病例中植入假資訊，6 個模型的幻覺率為 50–82%（p.1）。
- 常見形式：捏造參考文獻、數值錯誤、虛構病例細節或疾病（[[omar2025multi]] p.1, p.5）。

## 為什麼會發生
- LLM 依靠機率關聯，而不是查證過的資訊（[[omar2025multi]] p.5）。
- 有研究者認為部分幻覺是 LLM 架構本身固有的，無法完全消除（[[omar2025multi]] p.5）。
- 模型傾向附和使用者（[[sycophancy|迎合傾向]]）（[[omar2025multi]] p.5–6）。

## 怎麼降低
- [[mitigation-prompt|防護指令]]有效但無法消除；調低 [[temperature|溫度]]無效（[[omar2025multi]] p.3）。
- [[retrieval-augmented-generation|RAG]]、思維鏈提示也有幫助但無法消除（[[omar2025multi]] p.5，引用 Kim et al., 2025）。
- 人工把關 (human-in-the-loop)（[[omar2025multi]] p.5）。

## 相關頁面
[[adversarial-attack]]、[[sycophancy]]、[[large-language-model]]
