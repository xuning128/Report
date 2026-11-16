# 術語白話表 (Glossary)

> 依英文字母排序。每次 ingest 時新增。

| 術語 | 英文 | 白話解釋 | 例子 | 首次出現 |
|---|---|---|---|---|
| 加速度計 | Accelerometer | 偵測動作的感測器，用來判斷是否靜止 | 只在靜止時分析 PPG | [[lubitz2022detection]] |
| 對抗式攻擊 | Adversarial attack | 故意設陷阱考 AI，看它會不會上當 | 在病歷寫一個不存在的檢驗項目 | [[omar2025multi]] |
| AF 負荷 | AF burden | 監測期間處於心房顫動的時間比例 | 中位數 7% | [[lubitz2022detection]] |
| 心電圖貼片 | Ambulatory ECG patch | 貼在胸前、可連續記錄一週的心電圖 | 當作參考標準 | [[lubitz2022detection]] |
| 呼吸暫停 | Apnea | 停止呼吸一段時間 | 新生兒 ≥20 秒 | [[kausch2024apnea]] |
| 曲線下面積 | Area under the ROC curve (AUC) | 模型分辨有病／沒病的能力，0.5 亂猜、1 完美 | 重度高鉀 AUC 0.97 | [[lin2022point]] |
| 心房顫動 | Atrial fibrillation (AF) | 心房不規則亂跳，會增加中風風險 | 手錶偵測 PPV 98% | [[lubitz2022detection]] |
| 自體抗體 | Autoantibody | 身體產生攻擊自己組織的抗體 | 第 1 型糖尿病前會先出現 | [[ada2026prevention]] |
| 黑盒子實用研究 | Black-box pragmatic study | AI 在真實流程中運算但不給醫師看，避免影響處置 | ECG-K+ 在背景計算 | [[lin2022point]] |
| 血液培養 | Blood culture | 抽血培養看有沒有細菌，用來確診敗血症 | 培養陽性 = 有細菌 | [[kausch2024apnea]] |
| Bonferroni 校正 | Bonferroni correction | 一次做很多比較時，把「顯著」的門檻調嚴，避免碰巧得到顯著結果 | 比較 6 個模型兩兩之間的差異 | [[omar2025multi]] |
| 心跳過慢 | Bradycardia | 心跳突然變很慢 | 新生兒 <80 下、≥5 秒 | [[kausch2024apnea]] |
| 校準度 | Calibration | 模型給的機率準不準 | 說 20% 就真的約 20% 發生 | [[kausch2024apnea]] |
| 設限 | Censoring | 追蹤結束時還沒發生事件或失聯的人，要特別處理 | 存活者在最後一次就醫時設限 | [[lin2022point]] |
| CHA₂DS₂-VASc | CHA₂DS₂-VASc score | 心房顫動病人的中風風險加分表 | 年齡 ≥75 歲加 2 分 | [[lubitz2022detection]] |
| 時型 | Chronotype | 天生偏好早睡早起或晚睡晚起 | 晚睡型糖尿病勝算 2.5 倍 | [[ada2026prevention]] |
| 臨床決策支援 | Clinical decision support (CDS) | 幫醫師做判斷的電腦工具 | 藥物交互作用提醒 | [[omar2025multi]] |
| Clopper-Pearson 區間 | Clopper-Pearson exact interval | 比例（如 PPV）的精確信賴區間算法 | PPV 95% CI 95.5–99.5% | [[lubitz2022detection]] |
| 群集穩健標準誤 | Cluster-robust standard errors (Huber-White) | 校正同一個人重複測量造成的高估 | 同一寶寶每天的資料 | [[kausch2024apnea]] |
| C-index | Concordance index | 預測「誰比較早發生事件」的準確度，考慮時間的 AUC | 死亡 C-index 0.834 | [[lin2022point]] |
| 信賴區間 | Confidence interval (CI) | 估計值的「可能範圍」；95% CI 包含 1 時，OR 通常不顯著 | OR 1.05（0.89–1.23）→ 不顯著 | [[omar2025multi]] |
| 連續血糖監測 | Continuous glucose monitoring (CGM) | 貼皮膚的感測器整天記錄血糖 | 第 1 型追蹤 | [[ada2026prevention]] |
| 卷積神經網路 | Convolutional neural network (CNN) | 擅長處理圖片和波形的深度學習模型 | ECG12Net 有 82 層 | [[lin2022point]] |
| Cox 比例風險模型 | Cox proportional hazards model | 同時考慮多個因素、算出各自 HR 的存活分析方法 | 分析血鉀與死亡 | [[lin2022point]] |
| 交叉驗證 | Cross-validation | 資料分 10 份輪流當考卷，屬內部驗證 | 10 折交叉驗證 | [[kausch2024apnea]] |
| 深度學習 | Deep learning | 用多層神經網路從大量資料自己找規則 | 從心電圖估血鉀 | [[lin2022point]] |
| 糖尿病預防計畫 | Diabetes Prevention Program (DPP) | 美國大型生活型態介入試驗與推廣計畫 | 3 年降低 58% 風險 | [[ada2026prevention]] |
| 蒸餾 | Distillation | 用大模型教小模型，讓小模型模仿大模型的回答 | DeepSeek-R1 蒸餾到 Llama-70B | [[omar2025multi]] |
| 血鉀異常 | Dyskalemia | 血鉀太低（≤3.5）或太高（≥5.5） | 急診約 2% 高鉀 | [[lin2022point]] |
| 心電圖 | Electrocardiogram (ECG) | 記錄心臟電流變化的檢查；12 導程 = 12 個角度 | 10 秒 12 導程 | [[lin2022point]] |
| 證據等級 | Evidence grade | 建議有多少好證據支持；A 最強 | 建議 3.3 為 A | [[ada2026prevention]] |
| 外部驗證 | External validation | 用另一家醫院的資料測試模型 | 社區醫院驗證 | [[lin2022point]] |
| 極早產兒 | Extremely preterm infant | 懷孕未滿 28–29 週就出生的寶寶 | 平均 26.4 週出生 | [[kausch2024apnea]] |
| 偽陰性 | False negative | 真的有病，模型卻說沒有 | 抽血低鉀但 AI 判正常 | [[lin2022point]] |
| 偽陽性 | False positive | 其實沒病，模型卻說有 | 抽血正常但 AI 判高鉀 | [[lin2022point]] |
| 少樣本提示 | Few-shot prompting | 給 AI 幾個範例，讓它照樣做 | 給 2 個醫師寫的病例範本 | [[omar2025multi]] |
| 吸入氧氣濃度 | Fraction of inspired oxygen (FiO2) | 給病人吸的氣體中氧氣的比例 | 越高代表需要越多氧氣 | [[kausch2024apnea]] |
| 懷孕週數 | Gestational age (GA) | 出生時懷孕了幾週 | 足月約 40 週 | [[kausch2024apnea]] |
| 妊娠糖尿病 | Gestational diabetes mellitus (GDM) | 懷孕期間出現的糖尿病 | 之後得第 2 型的風險高 | [[ada2026prevention]] |
| A1C（糖化血色素） | Glycated hemoglobin (HbA1c) | 反映過去約 3 個月平均血糖 | 5.7–6.4% = 糖尿病前期 | [[ada2026prevention]] |
| 幻覺 | Hallucination | AI 一本正經地講出不存在的事 | 解釋一個根本不存在的疾病 | [[omar2025multi]] |
| 風險比 | Hazard ratio (HR) | 兩組「發生速度」差幾倍，考慮時間 | statin HR 1.36 | [[ada2026prevention]] |
| 心率變異度 | Heart rate variability (HRV) | 心跳間隔的變化程度 | RMSSD、pNN50 | [[lubitz2022detection]] |
| 空腹血糖異常 | Impaired fasting glucose (IFG) | 空腹血糖偏高但未達糖尿病 | 糖尿病前期的一種 | [[ada2026prevention]] |
| 葡萄糖耐受不良 | Impaired glucose tolerance (IGT) | 喝糖水後血糖降得慢 | 糖尿病前期的一種 | [[ada2026prevention]] |
| 間歇性低血氧 | Intermittent hypoxemia (IH) | 血氧一陣一陣掉下去又回來 | SpO2 <80% 持續 10–300 秒 | [[kausch2024apnea]] |
| 侵入性呼吸器 | Invasive mechanical ventilation | 插氣管內管、由機器幫忙呼吸 | 會掩蓋呼吸暫停訊號 | [[kausch2024apnea]] |
| JSON | JavaScript Object Notation | 一種結構化的文字格式，方便電腦讀取 | {"檢驗": "血糖", "範圍": "70–100"} | [[omar2025multi]] |
| 大型語言模型 | Large language model (LLM) | 讀過大量文字、會產生回答的 AI，例如 ChatGPT | GPT-4o、Llama | [[omar2025multi]] |
| 晚發性敗血症 | Late-onset sepsis (LOS) | 出生 3 天後才發生的血液細菌感染 | 極早產兒最多約 15% | [[kausch2024apnea]] |
| McFadden's pseudo R² | McFadden's pseudo R-squared | 邏輯斯迴歸的整體配適度，越大越好 | 0.067 → 0.094 | [[kausch2024apnea]] |
| 平均絕對誤差 | Mean absolute error (MAE) | 預測值平均差多少 | 0.365 mmol/L | [[lin2022point]] |
| Metformin（二甲雙胍） | Metformin | 最常見的第一線糖尿病藥 | 可用於高風險者預防 | [[ada2026prevention]] |
| 混合效應邏輯斯迴歸 | Mixed-effects logistic regression | 預測「是／否」，並考慮同一題被重複測量的統計方法 | 同一病例被 6 個模型測試 | [[omar2025multi]] |
| 多重插補 | Multiple imputation | 根據其他資料合理猜測遺漏值數次再合併 | 處理檢驗缺漏 | [[lin2022point]] |
| 陰性預測值 | Negative predictive value (NPV) | 模型說沒病時，真的沒病的比例 | 高鉀 NPV 99.8% | [[lin2022point]] |
| 新生兒加護病房 | Neonatal intensive care unit (NICU) | 照顧早產或重症新生兒的加護病房 | 第 IV 級為最高級 | [[kausch2024apnea]] |
| 勝算比 | Odds ratio (OR) | 兩組「發生勝算」差幾倍；1 = 沒差 | OR 0.27 → 勝算剩約 1/4 | [[omar2025multi]] |
| 口服葡萄糖耐受試驗 | Oral glucose tolerance test (OGTT) | 喝 75 g 糖水後 2 小時測血糖 | 173–199 mg/dL = 高風險 | [[ada2026prevention]] |
| 陣發性 | Paroxysmal | 一陣一陣發作，不是一直都有 | 陣發性 AF 不易抓到 | [[lubitz2022detection]] |
| 週期性呼吸 | Periodic breathing | 停一下、喘一下，反覆循環 | 早產兒常見 | [[kausch2024apnea]] |
| 人年 | Person-years | 人數 × 追蹤年數 | 每 100 人年 11 例 | [[ada2026prevention]] |
| 光體積變化描記法 | Photoplethysmography (PPG) | 手錶用光照皮膚量脈搏 | Fitbit 背面綠光 | [[lubitz2022detection]] |
| 床邊檢驗 | Point-of-care test (POC) | 在病人旁邊立即完成的檢查 | 心電圖 | [[lin2022point]] |
| 陽性預測值 | Positive predictive value (PPV) | 模型說有病時，真的有病的比例；受盛行率影響 | 高鉀 PPV 只有 10–15% | [[lin2022point]] |
| 矯正年齡 | Postmenstrual age (PMA) | 懷孕週數 + 出生後週數 | 預測敗血症最強因子 | [[kausch2024apnea]] |
| 出生後天數 | Postnatal age (PNA) | 出生到現在幾天 | 敗血症中位數第 23 天 | [[kausch2024apnea]] |
| 糖尿病前期 | Prediabetes | 血糖偏高但未達糖尿病，像黃燈 | A1C 5.7–6.4% | [[ada2026prevention]] |
| 盛行率 | Prevalence | 族群中有某病的比例 | 急診高鉀 1.4–2.1% | [[lin2022point]] |
| 提示工程 | Prompt engineering | 調整給 AI 的指令來改善回答 | 加一句「不確定就說不確定」 | [[omar2025multi]] |
| 血氧飽和度 | Pulse oximetry oxygen saturation (SpO2) | 血氧機測出血液含氧百分比 | 正常約 95% 以上 | [[kausch2024apnea]] |
| 品質調整生命年 | Quality-adjusted life-year (QALY) | 把「活多久」和「活得多好」合成一個數字，用來算成本效益 | 每 QALY 12,878 美元 | [[ada2026prevention]] |
| ROC 曲線 | Receiver operating characteristic curve | 畫出各切點的敏感度與誤判率 | 用來算 AUC | [[lin2022point]] |
| 參考標準 | Reference standard | 用來判斷「真實答案」的方法 | 一週心電圖貼片 | [[lubitz2022detection]] |
| 檢索增強生成 | Retrieval-augmented generation (RAG) | 讓 AI 先查資料再回答，像開書考 | 先搜尋 PubMed 再回答 | [[omar2025multi]] |
| 敏感度 | Sensitivity | 真的有病的人，模型抓到幾成 | 重度高鉀 93.8% | [[lin2022point]] |
| 模擬病例 | Simulated clinical vignette | 編寫的假病例，用來測試判斷 | 300 個醫師驗證的病例 | [[omar2025multi]] |
| 單組試驗 | Single-arm trial | 只有一組受試者、沒有對照組的試驗 | Fitbit Heart Study | [[lubitz2022detection]] |
| 滑動視窗 | Sliding window | 把連續訊號切成重疊的小段分別判斷 | 5 分鐘、重疊 50% | [[lubitz2022detection]] |
| 特異度 | Specificity | 真的沒病的人，模型正確放過幾成 | 重度高鉀 91.8% | [[lin2022point]] |
| 檢定力 | Statistical power | 真的有差異時，研究能偵測出來的機率 | 80% 檢定力 | [[lubitz2022detection]] |
| 迎合傾向 | Sycophancy | AI 傾向順著使用者講，不指出錯誤 | 你說有某疾病，它就跟著解釋 | [[omar2025multi]] |
| 脈搏間隔序列 | Tachogram | 每一下脈搏之間的時間間隔排成一串 | 5 分鐘一段 | [[lubitz2022detection]] |
| 遠距醫療 | Telehealth | 透過視訊或電話看診 | 收到通知後遠距看診 | [[lubitz2022detection]] |
| 溫度 | Temperature | 控制 AI 回答隨機程度的設定；0 = 每次都一樣 | 預設約 0.7 | [[omar2025multi]] |
| 時間序列 | Time series | 依時間順序重複記錄的資料 | 每天一列監測資料 | [[kausch2024apnea]] |
| TRIPOD | Transparent Reporting of a multivariable prediction model for Individual Prognosis Or Diagnosis | 預測模型論文的報告檢查清單 | 2024 年有 AI 版 | [[kausch2024apnea]] |
