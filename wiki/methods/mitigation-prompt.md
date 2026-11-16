---
type: method
aliases: [Mitigation Prompt, Prompt Engineering, 提示工程, 防護指令]
---
# 防護指令／提示工程（Mitigation Prompt / Prompt Engineering）

## 白話解釋
在問 AI 之前先加一段「規矩」，例如「只用確定的資訊，不確定就說不確定」。就像考試前提醒學生「不會的題目不要亂猜」。

## 正式定義
提示工程：透過提供更多脈絡、明確指示或範例，引導模型產生較安全的輸出（[[omar2025multi]] p.5）。

## 在文獻中怎麼被使用
- [[omar2025multi]]：防護指令要求只用經臨床驗證的資訊、承認不確定性（p.2）。
  - 整體幻覺率 66% → 44%，OR = 0.27（p.3）。
  - GPT-4o：53% → 23%（p.1）。
  - 作者結論：提示工程是他們觀察到最有效的短期策略，但無法消除錯誤（p.5）。

## 例子
OR = 0.27 的意思：加了防護指令後，出錯的「勝算」只剩原本的約 1/4。

## 優點／限制
- 優點：簡單、不用改模型、比調整溫度有效（[[omar2025multi]] p.5）。
- 限制：只能部分降低錯誤（[[omar2025multi]] p.5）。

## 相關頁面
[[temperature]]、[[llm-hallucination]]、[[retrieval-augmented-generation]]
