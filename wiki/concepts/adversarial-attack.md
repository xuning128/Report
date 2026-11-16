---
type: concept
aliases: [Adversarial Attack, Adversarial Hallucination Attack, 對抗式幻覺攻擊]
---
# 對抗式攻擊（Adversarial Attack）

## 白話解釋
故意設陷阱考 AI。例如在病歷裡寫一個根本不存在的檢驗項目，看 AI 會不會假裝知道並開始解釋。

## 正式定義
在提示詞中嵌入捏造的細節，誘使模型產生或延伸錯誤資訊（[[omar2025multi]] p.1）。

## 在文獻中怎麼被使用
- [[omar2025multi]]：每個模擬病例植入 1 個假檢驗項目、假徵象或假疾病（p.2）。
- 假資訊的來源可能是**無意的**（複製貼上錯誤、聽錯劑量、拼錯檢驗值），也可能是**惡意的**（假訊息宣傳）（[[omar2025multi]] p.2）。

## 相關頁面
[[llm-hallucination]]、[[simulated-clinical-vignettes]]
