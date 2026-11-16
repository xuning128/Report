---
type: method
aliases: [Clinical Vignettes, Simulated Cases, 模擬病例, 臨床情境題]
---
# 模擬病例（Simulated Clinical Vignettes）

## 白話解釋
由醫師（或 AI 輔助）編寫的假病例，用來測試 AI 或人的判斷。好處是可以精準控制變因、不涉及病人隱私；缺點是不如真實病歷複雜。

## 在文獻中怎麼被使用
- [[omar2025multi]]：300 例，每例只藏 1 個假元素；長短兩版只差字數（p.2）。
  - 製作流程：LLM（Claude Sonnet 3.5）+ few-shot 範本產生 → 兩位醫師獨立驗證 → 查 PubMed／Google Scholar 確認假元素不存在 → 不一致者討論達成共識（p.2）。
  - 不需要倫理審查（p.7）。

## 優點／限制
- 優點：變因可控、可大量產生、不涉及隱私（[[omar2025multi]] p.2, p.7）。
- 限制：可能無法反映真實臨床資訊的複雜度（[[omar2025multi]] p.6）。

## 可模仿的設計要點 ⭐
1. 一次只操弄一個變因（例：只差字數）
2. 至少兩位領域專家獨立驗證
3. 記錄不一致比例與解決方式

## 相關頁面
[[adversarial-attack]]、[[llm-as-judge]]
