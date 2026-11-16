# 02 Content — 健康數據 × AI

- **狀態**：定稿（2026-11-16 大綱第 4 版確認）
- **依據**：`01-outline.md` 第 4 版（2026-11-16 確認）
- **張數**：17（使用者 2026-11-16 要求互動式簡報，加入小測驗；使用者 2026-11-16 曾刪除 ADA 後又決定保留；使用者 2026-11-16 加入 Limitations and Future Work、Critical Thinking、Take-home）
- **字數規則**：每頁「重點＋條列」≤ 80 字；表格、圖、講稿不計
- **圖片**：全部自製（`doc/assets/` 無圖檔）
- **互動設計**（使用者 2026-11-16 指定）：
  - 逐步顯示：卡片、步驟、表格列按一下才出現（往回翻時全部顯示）
  - 可操作的圖：點時間軸的某一天、某一段，或滑過點圖、長條，下方顯示說明與出處
  - 點開看細節：標「＋」的卡片、步驟、表格列，點一下展開「點開細節」
  - 小測驗：第 15 張，3 題選擇題，點選後立刻顯示答案與出處
- **字數規則補充**：「點開細節」與測驗解析預設隱藏，不計入 80 字

---

## 1｜封面
- **版型**：封面
- **標題**：健康數據 × AI
- **副標**：從資料、預測模型，到 AI 的可靠度
- **說明行**：生成式 AI 課程報告｜5 篇文獻整合｜2026
- **講稿**：今天用 5 篇文獻，串起健康數據、NLP、預測模型與 AI 四個子主題。

## 2｜報告地圖
- **版型**：表格
- **重點**：5 篇文獻各補上一塊拼圖
- **表格**（● 直接相關、○ 可當對照）：

| 子主題 | Omar 2025 | ADA 2026 | Lin 2022 | Kausch 2024 | Lubitz 2022 |
|---|---|---|---|---|---|
| 健康數據 | ● | ● | ● | ● | ● |
| NLP | ● | | | | |
| 預測模型 | | ● | ● | ● | ● |
| AI | ● | | ● | ○ | ● |

- **來源**：01-outline 對照表；Kausch 用傳統統計，當 AI 的對照（kausch PDF p.5）
- **講稿**：表格看得出 NLP 只有 Omar 一篇，最後會在研究缺口回來談。

## 3｜健康數據：資料從哪來
- **版型**：卡片 ×4
- **重點**：四種資料型態
- **條列**：
  - 單次檢查：急診心電圖＋抽血（lin p.1）、血糖（ada p.S51）
  - 連續監測：NICU 監視器，47,512 住院日（kausch PDF p.6）
  - 穿戴裝置：手錶 PPG，455,699 人（lubitz p.1415）
  - 文字：300 例模擬病例（omar p.2）
- **講稿**：Lin 兩院共 34,803 + 6,492 次急診（lin p.1）；Omar 的病例不是真實病歷。
- **點開細節**：
  - 單次檢查：心電圖與抽血需在 1 小時內才納入（lin p.10）
  - 連續監測：心電、胸阻抗、血氧三種波形（kausch PDF p.2–4）
  - 穿戴裝置：只用靜止時段，靠加速度計判斷（lubitz p.1416）
  - 文字：每例只藏 1 個假資訊，長短兩版（omar p.2）

## 4｜健康數據：預測目標怎麼定義
- **版型**：表格
- **重點**：好的結果定義要有切點、持續時間與確認方式
- **表格**：

| 結果 | 定義 | 來源 |
|---|---|---|
| 糖尿病前期 | A1C 5.7–6.4%，或 IGT、IFG | ada p.S51 |
| 晚發性敗血症 | 出生 72 小時後血液培養陽性，且抗生素 ≥5 天 | kausch PDF p.4 |
| 心房顫動 | 心電圖上持續 ≥30 秒 | lubitz p.1417 |
| 重度高鉀 | 血鉀 ≥6.5 mmol/L（共分 7 級） | lin p.10 |

- **講稿**：ADA 是臨床指引，授權限制只引用切點數字，不重畫其圖表。

## 5｜健康數據：預測特徵怎麼選
- **版型**：卡片 ×4
- **重點**：特徵可以由人挑，也可以讓模型自己學
- **條列**：
  - 臨床風險因子：BMI、血糖、妊娠糖尿病史（ada p.S53–S56）
  - 事件指標：呼吸暫停、心跳過慢（kausch PDF p.4）
  - 原始波形：12 導程心電圖（lin p.10）
  - 視窗序列：5 分鐘脈搏間隔（lubitz p.1416）
- **講稿**：越往下越依賴模型自己找規則，可解釋性也越低（⚠️ 推論）。
- **點開細節**：
  - 臨床風險因子：亞裔 BMI 切點較低，>23（ada p.S52）
  - 事件指標：插管時無法算呼吸暫停，只在未插管時計算（kausch PDF p.4）
  - 原始波形：ECG12Net，82 層卷積神經網路（lin p.10）
  - 視窗序列：演算法細節未公開（lubitz p.1417）

## 6｜預測模型：時間怎麼標記
- **版型**：圖
- **重點**：「未來會不會發生」和「現在有沒有」，標記方式完全不同
- **圖表規格**：
  - 圖片來源：自製
  - 圖型：時間軸（兩列）
  - 上列 Kausch：每天一列；確診日與前 2 天標 1，其他天標 0，確診後 10 天排除（kausch PDF p.5）
  - 下列 Lubitz：5 分鐘視窗、重疊 50%，連續 11 段不規則（≥30 分鐘）才發通知（lubitz p.1416）
- **講稿**：Kausch 是提前預測，Lubitz 是同時偵測；排除治療期是為了不讓標籤被治療污染。
- **圖的互動說明**：
  - -5、-4、-3：距確診 3 天以上 → 標 0
  - -2、-1、0：落在「未來 3 天內」→ 標 1
  - +1 … +10：治療與恢復期，不納入分析
  - +11：恢復後重新開始 → 標 0
  - Lubitz 每一段：5 分鐘，每 2.5 分鐘取一段；連續 11 段不規則才通知（lubitz p.1416）

## 7｜預測模型：可模仿的研究設計
- **版型**：步驟 ×6
- **重點**：六個可以直接借用的設計
- **條列**：
  1. 黑盒子實用研究：AI 背景運算，不給醫師看（lin p.10）
  2. 外部驗證：換一家醫院再測（lin p.2）
  3. 逐步加入變項，看 AUC 增益（kausch PDF p.5）
  4. 校正重複測量（kausch PDF p.5；omar p.3）
  5. 事先註冊、固定演算法（lubitz p.1417）
  6. 事先計算樣本數（lubitz p.1417）
- **講稿**：第 4 點：同一個寶寶每天一列、同一病例被測多次，都要校正。
- **點開細節**：
  1. 醫師的處置不受 AI 影響，可以公平比較（lin p.10）
  2. 兩院使用相同切點（lin p.2）
  3. 只用 PMA 0.739 → 完整模型 0.783（kausch PDF p.18）
  4. Kausch 用 Huber-White；Omar 用混合效應模型（kausch PDF p.5；omar p.3）
  5. 註冊編號 NCT04380415（lubitz p.1415）
  6. 目標 155 人、檢定力 80%（lubitz p.1417）

## 8｜預測模型：表現要連驗證方式一起看
- **版型**：圖＋表格
- **重點**：任務與驗證方式不同，AUC 不能直接比高低（⚠️ 推論）
- **圖表規格**：
  - 圖片來源：自製
  - 圖型：點圖，x 軸 AUC 0.70–1.00
  - Lin 重度低鉀：教學醫院 0.9497、社區醫院 0.9194（lin p.2）
  - Lin 重度高鉀：教學醫院 0.9658、社區醫院 0.9865（lin p.2）
  - Kausch：僅 PMA 0.739、完整模型 0.783（kausch PDF p.18）
- **表格**：

| 研究 | 驗證方式 | 來源 |
|---|---|---|
| Lin | 外部驗證（同體系社區醫院） | lin p.2 |
| Kausch | 內部驗證（10 折交叉驗證） | kausch PDF p.5 |
| Lubitz | 前瞻性，以心電圖貼片為參考標準；敏感度 67.6% | lubitz p.1419 |

- **講稿**：Lin 的社區醫院和教學醫院屬同一體系，外推仍有限（⚠️ 推論）。

## 9｜預測模型：自己跑模型需要的技術
- **版型**：步驟 ×6
- **重點**：以穿戴裝置偵測 AF 為例（⚠️ 推論，原文未公開演算法）
- **條列**：
  1. 資料：PPG＋心電圖標註
  2. 前處理：濾波、找峰值
  3. 切視窗：5 分鐘、重疊 50%（lubitz p.1416）
  4. 特徵：心率變異度
  5. 模型：XGBoost、CNN
  6. 評估：以「人」切分資料
- **講稿**：工具可用 SciPy、NeuroKit2；論文用 Python 3.7 與 R 4.1.0（lubitz p.1418）；以人切分是避免同一人同時出現在訓練與測試。

## 10｜AI：「判錯」反而有訊號
- **版型**：表格
- **重點**：抽血正常、AI 卻判異常的人，30 天死亡風險較高
- **表格**：

| 組別（對照：血鉀正常） | 30 天死亡 HR（95% CI） |
|---|---|
| 抽血高鉀 | 3.66（3.02–4.44） |
| 抽血正常、AI 判低鉀 | 1.40（1.16–1.69） |
| 抽血正常、AI 判高鉀 | 1.49（1.00–2.24） |

- **條列**：
  - 作者解釋：模型可能學到造成血鉀異常的疾病特徵（lin p.9）
- **來源**：lin p.2, p.4, p.9
- **講稿**：這些人較老、共病多；屬觀察性發現，不代表因果（⚠️ 推論）。

## 11｜AI × NLP：LLM 會被假資訊帶著走
- **版型**：圖
- **重點**：6 個 LLM 有 50–82% 會照單全收（omar p.1）
- **圖表規格**：
  - 圖片來源：自製
  - 圖型：橫向長條圖，整體幻覺率
  - 預設 65.9%、防護指令 44.2%、溫度 0 66.5%（omar p.3）
- **條列**：
  - 防護指令有效（OR 0.27），但無法消除（omar p.3）
  - 調低溫度無效（omar p.3）
- **講稿**：GPT-4o 同時是受測模型和評審，結果可能偏向它（⚠️ 推論）。
- **圖的互動說明**：
  - 預設：各廠商標準設定，65.9%
  - 防護指令：44.2%，OR 0.27（95% CI 0.23–0.32）
  - 溫度 0：66.5%，OR 1.05，無顯著差異（omar p.3）

## 12｜AI：可靠度取決於模型類型與驗證
- **版型**：對照
- **重點**：同樣叫 AI，可靠度差很多（⚠️ 推論）
- **條列**：
  - 生成式 LLM：通用、讀文字、易被錯誤輸入誤導（omar p.3）
  - 單一任務深度學習：真實資料＋外部驗證，表現穩定（lin p.2）
  - 傳統統計：特徵可解釋，但只有內部驗證（kausch PDF p.5）
- **講稿**：評讀 AI 研究時，先看任務、資料、驗證方式，再看數字。
- **點開細節**：
  - 生成式 LLM：蒸餾模型 Distilled-DeepSeek-R1 最差，OR 8.41（omar p.3）
  - 單一任務深度學習：比抽血報告早 42.8 分鐘（lin p.2）
  - 傳統統計：遵循 TRIPOD 報告規範（kausch PDF p.4）

## 13｜Limitations and Future Work
- **版型**：表格＋條列
- **重點**：各篇作者自述的限制，指向下一步
- **表格**（作者自述的限制）：

| 研究 | 主要限制 | 來源 |
|---|---|---|
| Omar | 模擬病例；每題只跑一次 | omar p.6 |
| Lin | 只有東亞族群；未評估提早處置是否改善結果 | lin p.10 |
| Kausch | 以天為單位，可能錯過快速惡化 | kausch PDF p.8 |
| Lubitz | 敏感度不完美；參與者偏向既有使用者 | lubitz p.1423 |

- **條列**（Future Work）：
  - 外部驗證：Kausch 只有內部驗證（kausch PDF p.5）
  - 亞洲族群：Lubitz 亞裔僅 2.9%（lubitz p.1420）
  - 真實病歷測 LLM（omar p.6）
  - 補 NLP 文獻：用病歷做預測（⚠️ 推論）
- **講稿**：最後一點是本知識庫的缺口，下一步補論文。

## 14｜Critical Thinking
- **版型**：表格
- **重點**：讀 AI 研究時，先問這四個問題（⚠️ 推論，本報告歸納）
- **表格**：

| 問題 | 本次文獻的例子 | 來源 |
|---|---|---|
| 誰出資？ | Fitbit 出資；Kausch 兩位作者持股 | lubitz p.1418；kausch PDF p.1 |
| 誰當評審？ | GPT-4o 同時是受測模型與評審 | omar p.2–3 |
| 驗證夠獨立嗎？ | 外部驗證醫院屬同一醫療體系 | lin p.2 |
| 能重現嗎？ | 資料或程式碼未公開 | lin p.11；omar p.6；lubitz p.1418 |

- **講稿**：這些不代表研究錯，而是解讀數字時要打折扣的地方。
- **點開細節**：
  - 誰出資：統計分析由麻州總醫院執行（lubitz p.1418）
  - 誰當評審：醫師抽查 200 筆，一致率 100%（omar p.2–3）
  - 驗證夠獨立嗎：儀器與流程相近（lin p.2；⚠️ 推論）
  - 能重現嗎：Omar 資料需向作者索取（omar p.6）

## 15｜小測驗
- **版型**：互動測驗（3 題，點選後顯示答案與出處）
- **重點**：三題，檢查自己聽懂了沒
- **題目**：
  1. Kausch 怎麼標記「敗血症」？ A 只有確診當天標 1｜**B 確診日與前 2 天標 1**｜C 住院期間全部標 1
     - 解析：預測「未來 3 天內」，確診後 10 天排除（kausch PDF p.5）
  2. 哪一篇做了外部驗證？ **A Lin**｜B Kausch｜C Omar
     - 解析：Lin 在同體系社區醫院驗證（lin p.2）；Kausch 只有 10 折交叉驗證（kausch PDF p.5）
  3. 哪個方法能降低 LLM 幻覺？ A 溫度調成 0｜**B 加防護指令**｜C 改用短版病例
     - 解析：防護指令 65.9% → 44.2%；溫度 0 無效；短版反而稍微更容易出錯，OR 1.22（omar p.3）
- **講稿**：可以請聽眾舉手選答案，再點出正解。

## 16｜Take-home
- **版型**：卡片 ×3
- **重點**：三件帶回家的事（⚠️ 推論，本報告歸納）
- **條列**：
  - 先定義結果與時間窗，再談模型
  - 驗證方式決定數字能信多少
  - AI 不是同一種東西：看任務、資料、驗證
- **講稿**：對應第 4–6 張、第 8 張、第 11–12 張。

## 17｜參考文獻
- **版型**：參考文獻
- American Diabetes Association Professional Practice Committee for Diabetes. (2026). 3. Prevention or delay of diabetes and associated comorbidities: Standards of care in diabetes—2026. *Diabetes Care, 49*(Suppl. 1), S50–S60. https://doi.org/10.2337/dc26-S003
- Kausch, S. L., Lake, D. E., Di Fiore, J. M., Weese-Mayer, D. E., Claure, N., Ambalavanan, N., Vesoulis, Z. A., Fairchild, K. D., Dennery, P. A., Hibbs, A. M., Martin, R. J., Indic, P., Travers, C. P., Bancalari, E., Hamvas, A., Kemp, J. S., Carroll, J. L., Moorman, J. R., Sullivan, B. A., & the Prematurity-Related Ventilatory Control (Pre-Vent) Investigators. (2024). Apnea, intermittent hypoxemia, and bradycardia events predict late-onset sepsis in extremely preterm infants. *The Journal of Pediatrics, 271*, Article 114042. https://doi.org/10.1016/j.jpeds.2024.114042
- Lin, C., Chau, T., Lin, C.-S., Shang, H.-S., Fang, W.-H., Lee, D.-J., Lee, C.-C., Tsai, S.-H., Wang, C.-H., & Lin, S.-H. (2022). Point-of-care artificial intelligence-enabled ECG for dyskalemia: A retrospective cohort analysis for accuracy and outcome prediction. *npj Digital Medicine, 5*, Article 8. https://doi.org/10.1038/s41746-021-00550-0
- Lubitz, S. A., Faranesh, A. Z., Selvaggi, C., Atlas, S. J., McManus, D. D., Singer, D. E., Pagoto, S., McConnell, M. V., Pantelopoulos, A., & Foulkes, A. S. (2022). Detection of atrial fibrillation in a large population using wearable devices: The Fitbit Heart Study. *Circulation, 146*, 1415–1424. https://doi.org/10.1161/CIRCULATIONAHA.122.060291
- Omar, M., Sorin, V., Collins, J. D., Reich, D., Freeman, R., Gavin, N., Charney, A., Stump, L., Bragazzi, N. L., Nadkarni, G. N., & Klang, E. (2025). Multi-model assurance analysis showing large language models are highly vulnerable to adversarial hallucination attacks during clinical decision support. *Communications Medicine, 5*, Article 330. https://doi.org/10.1038/s43856-025-01021-3

---

## 查詢紀錄
- 2026-11-16｜Notion › 跨篇綜合分析 › 領域全貌：與本機一致（沿用階段 1 查詢）
- 2026-11-16｜本機 wiki › papers/ 5 篇（全部數字核對來源）
- 2026-11-16｜本機 wiki › methods/ppg-af-modeling-pipeline（第 9 張）
- 2026-11-16｜本機 wiki › glossary（講義術語表）
- 2026-11-16｜本機 wiki › papers/ 限制、評析段落（第 13、14 張）
