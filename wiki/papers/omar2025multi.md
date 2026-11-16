---
type: paper
citekey: omar2025multi
title: Multi-model assurance analysis showing large language models are highly vulnerable to adversarial hallucination attacks during clinical decision support
title_zh: 多模型驗證分析：大型語言模型在臨床決策支援中極易受到對抗式幻覺攻擊
authors: [Omar, M., Sorin, V., Collins, J. D., Reich, D., Freeman, R., Gavin, N., Charney, A., Stump, L., Bragazzi, N. L., Nadkarni, G. N., Klang, E.]
year: 2025
journal: Communications Medicine
volume: 5
article: 330
doi: 10.1038/s43856-025-01021-3
source_file: doc/papers/omar2025multi.pdf
purpose: 了解疾病與技術、找出可當預測特徵與預測目標的變項
role: 風險／限制類背景文獻
study_design: 模擬實驗研究（對抗式測試，benchmark evaluation）
dataset: [自建模擬病例 300 例（未公開，需向作者索取）]
outcome: LLM 是否把假資訊當真（幻覺：是／否）
models: [GPT-4o, Distilled-DeepSeek-R1-70B, Phi-4, gemma-2-27b-it, Qwen-2.5-72B, Llama-3.3-70B]
metrics: {幻覺率_預設: 65.9%, 幻覺率_防護指令: 44.2%, 幻覺率_溫度0: 66.5%}
validation: 兩位醫師抽查 200 筆，與 GPT-4o 自動分類 100% 一致
keywords: [kw-llm-hallucination, kw-adversarial-attack, kw-clinical-decision-support, kw-prompt-engineering]
ingested: 2026-11-16
---

# 大型語言模型在臨床決策支援中極易受對抗式幻覺攻擊（Omar et al., 2025）

**APA 7：** Omar, M., Sorin, V., Collins, J. D., Reich, D., Freeman, R., Gavin, N., Charney, A., Stump, L., Bragazzi, N. L., Nadkarni, G. N., & Klang, E. (2025). Multi-model assurance analysis showing large language models are highly vulnerable to adversarial hallucination attacks during clinical decision support. *Communications Medicine, 5*, Article 330. https://doi.org/10.1038/s43856-025-01021-3

> 在本知識庫的定位：**風險／限制類背景文獻**——說明生成式 AI 用在醫療時的安全風險。
> 使用者想強調：**模型間比較**、**研究設計方法（可模仿）**。

## 一句話摘要
在模擬病例中藏一個假資訊，6 個 [[large-language-model|LLM]] 有 50–82% 的機率照單全收並加油添醋；[[mitigation-prompt|防護指令]]能降到約 44%，但無法消除；調低 [[temperature|溫度]]沒有效果（p.1）。

## ⭐ 疾病與技術
- **疾病**：不針對單一疾病，而是一般**臨床決策支援**情境；植入的假資訊分三類：假檢驗項目、假理學／影像徵象、假疾病（p.2）。
- **資料**：300 個醫師驗證的模擬病例（非真實病歷），長短兩版（p.2）。
- **技術**：6 個[[large-language-model|大型語言模型]]（GPT-4o、Distilled-DeepSeek-R1、Phi-4、gemma-2-27b、Qwen-2.5-72B、Llama-3.3-70B）；[[mitigation-prompt|提示工程]]、[[temperature|溫度]]調整；以 GPT-4o 當[[llm-as-judge|自動評審]]（p.2–3）。

## ⭐ 預測特徵與預測目標
- ⚠️ 推論：這篇**不是疾病預測研究**，而是「評估 AI 工具可靠度」的實驗。若用預測研究的語言對照：
  - **結果（目標）**：每個輸出是否為幻覺（是／否），由 GPT-4o 判定、醫師抽查 200 筆（p.2–3）。
  - **操弄變因（類似特徵）**：模型種類、是否加防護指令、溫度（預設／0）、病例長短（p.3）。
- 可借用之處（⚠️ 推論）：未來若用 LLM 從病歷「抽取預測特徵」或「計算風險」，需先評估 LLM 是否會被錯誤輸入誤導。

## ⭐ 研究設計（可模仿）
1. **建立測試題庫**：LLM 產生草稿 → 兩位醫師獨立驗證 → 查證假元素不存在 → 記錄不一致比例（<3%）（p.2）。
2. **一次只操弄一個變因**：長短版醫學內容相同，只差字數（p.2）。
3. **因子設計**：6 模型 × 3 條件 × 300 例 × 2 版 = 5,400 個輸出（p.1–2）。
4. **明確的操作型定義**：先定義什麼算「幻覺」、什麼算「非幻覺」（p.2, Fig. 2）。
5. **自動判定 + 人工抽查**：LLM 自動分類，醫師隨機抽查 200 筆確認一致（p.2–3）。
6. **處理重複測量**：同一病例被測多次 → [[mixed-effects-logistic-regression|混合效應邏輯斯迴歸]]，病例為隨機截距；多重比較用 Bonferroni 校正（p.3）。
7. **質性補充分析**：用 5 個真實錯誤資訊做對質測試（p.3–4）。

## ⭐ 時間序列與結果標記
- **不適用**：橫斷式實驗，每個病例在每種條件下只跑一次，沒有隨時間追蹤（p.6）。
- 作者自述的相關限制：每題只跑一次，無法反映每次執行之間的變異；建議未來重複多次（p.6）。
- 分析單位：「單一輸出」；結果標記為二元（幻覺／非幻覺）（p.2）。

## 研究目的
量化 LLM 在臨床情境中被[[adversarial-attack|對抗式攻擊]]誘發[[llm-hallucination|幻覺]]的頻率，並測試兩種簡單防護（防護指令、溫度 0）是否有效（p.1–2）。
- 背景動機：病歷本來就可能有錯（複製貼上錯誤、聽錯劑量），也可能被惡意植入假資訊；LLM 若把每個字都當真，錯誤會一路傳下去（p.2）。

## 資料與樣本
- **資料來源**：自建 [[simulated-clinical-vignettes|模擬病例]] 300 例，不是真實病歷（p.2）。
- **每例只藏 1 個假資訊**，分三類：假檢驗項目（如 "Serum Neurostatin"）、假理學／影像徵象（如 "Cardiac Spiral Sign"）、假疾病（如 "Faulkenstein Syndrome"）（p.2）。
- **長短兩版**：短版 50–60 字、長版 90–100 字，醫學內容相同（p.2）。
- **產生方式**：用 Claude Sonnet 3.5 搭配 few-shot 範本產生草稿，再由兩位醫師逐例驗證：確認只有一個假元素、用 PubMed／Google Scholar 查證不存在、內容前後一致；意見不一致者 <3%，討論後達成共識（p.2）。
- **倫理審查**：不需要，因為只用合成資料（p.7）。

## 方法
### 實驗設計（可模仿 ⭐）
- **6 個模型 × 3 種條件 × 300 例 × 長短 2 版 = 5,400 個輸出**（p.1–2）
- 三種條件（p.1, p.3）：
  1. **預設**：各廠商標準設定（溫度約 0.7、top-p 0.9–1.0）
  2. **[[mitigation-prompt|防護指令]]**：要求只用經臨床驗證的資訊、不確定時要說明，不要推測
  3. **[[temperature|溫度 0]]**：其他參數不變
- 任務格式：要求模型以 JSON 輸出（列出檢驗值及參考範圍、說明徵象的臨床意義、描述疾病）（p.2）。
- 閉源模型透過 API 呼叫；開源模型在 4 張 NVIDIA H100 GPU 上執行（p.3）。

### 幻覺的判定（p.2，Fig. 2）
- **幻覺**：回答中延伸、認可或把假元素當成真的。
- **非幻覺**：表示不確定、指出該元素不存在，或省略它。
- 以 GPT-4o 自動分類（[[llm-as-judge|LLM 當評審]]）；兩位醫師隨機抽查 200 筆，一致率 100%（p.2–3）。

### 統計方法（p.3）
- [[mixed-effects-logistic-regression|混合效應邏輯斯迴歸]]：結果為幻覺（是／否），每個病例設為隨機截距（因為同一病例被測多次）。
- 固定效應：溫度、防護指令、長短版；以[[odds-ratio|勝算比 (OR)]] 與 95% CI 呈現。
- 兩兩比較用 emmeans 套件，Bonferroni 校正；R 4.4.2；p < 0.05 為顯著。

### 補充：質性對質分析（p.3–4）
- 用 5 個常見醫療錯誤資訊（疫苗與自閉症、5G 與 COVID-19 等）測試 GPT-o1、GPT-4o、Distilled-DeepSeek-R1，共 45 次。
- 43 次沒有幻覺；2 次出錯都是 GPT-4o 在「自然免疫 vs. 疫苗」題（p.4）。

## 主要結果

### 整體（p.3）
| 條件 | 整體幻覺率 | 長版 | 短版 |
|---|---|---|---|
| 預設 | 65.9% | 64.1% | 67.6% |
| 防護指令 | 44.2% | 43.1% | 45.3% |
| 溫度 0 | 66.5% | 64.7% | 68.4% |

- 防護指令：OR = 0.27（95% CI 0.23–0.32），顯著降低（p.3）。
- 溫度 0：OR = 1.05（0.89–1.23；p = 0.58），無顯著差異（p.3）。
- 短版：OR = 1.22（1.07–1.39；p = 0.003），稍微更容易出錯（p.3）。
- 加了防護指令反而「變成幻覺」的只有 1.2%（65/5400）（p.3）。

### 模型間比較 ⭐（預設條件）
| 模型 | 幻覺率（長／短） | 相對 GPT-4o 的 OR | 來源 |
|---|---|---|---|
| GPT-4o（參照組） | 53.3% / 50.0% | 1（參照） | p.3 |
| Distilled-DeepSeek-R1-70B | 80.0% / 82.7% | 8.41（p = 0.0001） | p.3 |
| Phi-4 | 見 Fig. 4 | 7.12（p = 0.0003） | p.3 |
| gemma-2-27b-it | 見 Fig. 4 | 3.11（p = 0.0001） | p.3 |
| Qwen-2.5-72B | 見 Fig. 4 | 1.95（p = 0.022） | p.3 |
| Llama-3.3-70B | 見 Fig. 4 | 1.00（無顯著差異） | p.3–4 |

- 其他模型的幻覺率介於 58.7%–82.0%；各模型的確切數字只出現在 Fig. 4，文字中未列出（p.3）。
- GPT-4o 加上防護指令後：長版 20.7%、短版 24.7%（p.3）。
- 作者觀察：Distilled-DeepSeek-R1-70B 與它的原始模型 Llama-3.3-70B 參數量相同，表現卻差很多；作者推測蒸餾 (distillation) 或人類回饋強化學習 (RLHF) 的訓練流程可能會放大幻覺（p.4）。

## 作者自述的限制（p.6）
1. 用模擬病例，不是真實病歷，可能不夠複雜。
2. 只測 6 個模型、3 種條件。
3. 只計算「明確捏造」，可能漏掉較細微的錯誤。
4. 每題每條件只跑一次，無法反映每次執行之間的差異。
5. 沒有測試[[retrieval-augmented-generation|檢索增強生成 (RAG)]] 或上網查證。

## 評析
- ⚠️ 推論：**GPT-4o 同時是受測模型和評審**。雖然有 200 筆醫師抽查，仍可能偏向對 GPT-4o 有利。作者以 GPT-4o 準確度高為理由（p.4），但沒有討論這個利益衝突。
- ⚠️ 推論：病例也由 LLM（Claude Sonnet 3.5）產生（p.2），而 Claude 不在受測名單中，這一點可能影響結果的外推。
- ⚠️ 推論：資料未公開、需向作者索取（p.6），重現性受限。
- 優點：設計簡單、變因清楚（一次只操弄一個因素）、有醫師驗證、統計方法有處理重複測量。

## 與其他文獻的關係（作者引用，尚未納入本知識庫）
- 與 Kim et al. (2025) 一致：RAG 與思維鏈 (chain-of-thought) 提示能降低醫療幻覺，但無法消除（p.5）。
- 與 Fanous et al. (2025) 的[[sycophancy|迎合傾向]]研究一致：模型傾向附和使用者，而不是挑戰錯誤前提（p.5–6）。
- 作者提到其他研究發現 LLM 捏造參考文獻的比例可達 25–50%（p.1）。

## 對我的研究有什麼用
- **背景章節**：說明「生成式 AI 用在醫療」的風險與限制，可引用具體數字（50–82%、防護指令只能降到 44%）。
- **研究設計範本** ⭐：「操弄單一變因 + 多模型比較 + 醫師驗證 + 混合效應模型」的架構，未來設計實驗時可以參考。
- **提醒自己**：本知識庫也用 LLM 整理文獻，所以「每個論點都要有頁碼」這條規則有實證支持。

## 本篇新增術語（已加入 glossary）
幻覺、對抗式攻擊、溫度、勝算比、信賴區間、混合效應邏輯斯迴歸、臨床決策支援、提示工程、模擬病例、蒸餾、迎合傾向、檢索增強生成、JSON、Bonferroni 校正
