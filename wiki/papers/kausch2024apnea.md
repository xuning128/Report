---
type: paper
citekey: kausch2024apnea
title: "Apnea, Intermittent Hypoxemia, and Bradycardia Events Predict Late-Onset Sepsis in Extremely Preterm Infants"
title_zh: 呼吸暫停、間歇性低血氧與心跳過慢事件可預測極早產兒的晚發性敗血症
authors: [Kausch, S. L., Lake, D. E., Di Fiore, J. M., Weese-Mayer, D. E., Claure, N., Ambalavanan, N., Vesoulis, Z. A., Fairchild, K. D., Dennery, P. A., Hibbs, A. M., Martin, R. J., Indic, P., Travers, C. P., Bancalari, E., Hamvas, A., Kemp, J. S., Carroll, J. L., Moorman, J. R., Sullivan, B. A., Pre-Vent Investigators]
year: 2024
journal: The Journal of Pediatrics
volume: 271
article: 114042
doi: 10.1016/j.jpeds.2024.114042
source_file: doc/papers/kausch2024apnea.pdf
source_version: PMC 作者稿（author manuscript），頁碼以 PDF 頁碼標示
role: 核心文獻
purpose: 了解疾病與技術、找出可當預測特徵與預測目標的變項
study_design: 前瞻性觀察世代（Pre-Vent）的次級分析；預測模型開發＋內部驗證
dataset: [pre-vent-cohort]
outcome: 未來 3 天內確診晚發性敗血症（每日二元標記）
models: [多變項邏輯斯迴歸]
metrics: {cvAUC_僅PMA: 0.739, cvAUC_完整: 0.783, pseudoR2_完整: 0.094}
validation: 內部驗證（10 折交叉驗證）；無外部驗證
keywords: [kw-neonatal-sepsis, kw-preterm-infant, kw-physiological-monitoring-prediction]
conflict_of_interest: 兩位作者持有 Medical Prediction Sciences Corporation 股票（PDF p.1）
ingested: 2026-11-16
---

# 呼吸暫停、間歇性低血氧與心跳過慢可預測極早產兒晚發性敗血症（Kausch et al., 2024）

**APA 7：** Kausch, S. L., Lake, D. E., Di Fiore, J. M., Weese-Mayer, D. E., Claure, N., Ambalavanan, N., Vesoulis, Z. A., Fairchild, K. D., Dennery, P. A., Hibbs, A. M., Martin, R. J., Indic, P., Travers, C. P., Bancalari, E., Hamvas, A., Kemp, J. S., Carroll, J. L., Moorman, J. R., Sullivan, B. A., & the Prematurity-Related Ventilatory Control (Pre-Vent) Investigators. (2024). Apnea, intermittent hypoxemia, and bradycardia events predict late-onset sepsis in extremely preterm infants. *The Journal of Pediatrics, 271*, Article 114042. https://doi.org/10.1016/j.jpeds.2024.114042

> 在本知識庫的定位：**核心文獻**。用途：了解疾病與技術、找出可當**預測特徵**與**預測目標**的變項。
> 使用者想強調：**研究設計（可模仿）**、**時間序列資料怎麼標記結果（未來 3 天內是否確診）**。
> ⚠️ 本 PDF 為 PMC 作者稿，頁碼以「PDF p.」標示；正式引用以期刊版書目為準。

## 一句話摘要
從新生兒加護病房床邊監視器的連續訊號，算出呼吸暫停、週期性呼吸、低血氧持續時間、心跳過慢次數，可以在醫師確診前預測極早產兒的[[late-onset-sepsis|晚發性敗血症]]；完整模型 AUC 0.783（PDF p.2, p.18）。

## 研究目的（PDF p.3）
1. 在考慮「是否插管使用呼吸器」的情況下，探討心肺事件指標與敗血症的關聯。
2. 觀察敗血症發生前，心肺指標隨時間的動態變化。
3. 建立結合心肺特徵的多變項模型，預測血液培養陽性的晚發性敗血症。

## ⭐ 疾病與技術背景
### 疾病
- **[[preterm-infant|極早產兒]]**：本研究定義為懷孕未滿 29 週出生（WHO 定義為 28 週，作者為延續先前研究採 29 週）（PDF p.3）。
- **[[late-onset-sepsis|晚發性敗血症]]**：出生 72 小時後的血液細菌感染；極早產兒中最多約 15% 會發生，可能致命（PDF p.2）。
- 感染引起的全身發炎會干擾自律神經對心跳與呼吸的控制，表現為呼吸暫停、心跳過慢（PDF p.2）。
- 難處：這些事件在沒有敗血症的早產兒身上也常見（呼吸控制未成熟、肺病），所以要分辨「平常就有」和「快要生病」（PDF p.3）。

### 技術
- **[[continuous-physiological-monitoring|床邊連續生理監測]]**：NICU 寶寶整天接著監視器，記錄心電、胸阻抗（呼吸）、血氧（SpO2）波形（PDF p.2–4）。
- 前人工具：HeRO 心率特徵指數，偵測心率變異度下降與短暫心跳減速，預測 24 小時內的敗血症樣疾病（PDF p.3, p.7）。
- 本研究的特色：用醫師在床邊認得、但通常無法自動量化的**事件型指標**（PDF p.3, p.8）。

## ⭐ 預測特徵（PDF p.4）
詳見 [[cardiorespiratory-events]]。

| 特徵 | 定義 | 資料來源 | 插管時可用？ |
|---|---|---|---|
| 呼吸暫停 (apnea) | 每天停止呼吸 ≥20 秒的平均次數 | 胸阻抗波形 | ❌ |
| 週期性呼吸 (periodic breathing) | 每天處於週期性呼吸的分鐘數（小波轉換＋5 次呼吸模板） | 胸阻抗波形 | ❌ |
| IH80 每次持續時間 | SpO2 <80% 持續 10–300 秒事件的平均時長 | 血氧 | ✅ |
| IH90 每次持續時間 | SpO2 <90% 持續 10–300 秒事件的平均時長 | 血氧 | ✅ |
| 心跳過慢 (bradycardia) | 每天心跳 <80 下且 ≥5 秒的平均次數 | 心率 | ✅ |
| 臨床：矯正年齡 (PMA) | — | 病歷 | ✅ |
| 臨床：是否插管 | 每天二分：有／無氣管內管侵入性呼吸器 | 病歷 | — |

- 插管時呼吸由機器設定，會掩蓋呼吸暫停，所以呼吸暫停與週期性呼吸**只在未插管時計算**（PDF p.4, p.8）。
- IH90 對模型幫助很小，最後排除（PDF p.7）。
- 選「持續時間」而非「次數」，因為原始 Pre-Vent 研究中持續時間更能預測呼吸結果（PDF p.8）。

## ⭐ 預測目標（PDF p.4）
- **晚發性敗血症**：出生 72 小時後血液培養陽性，且接受 ≥5 天抗生素（若治療中死亡則可少於 5 天）；各中心由臨床醫師審查確認。
- 同一位寶寶的多次敗血症，間隔 ≥10 天才算不同事件。
- 致病菌：凝固酶陰性葡萄球菌 36%、金黃色葡萄球菌 15%、大腸桿菌 10%、其他革蘭氏陽性 7%、其他革蘭氏陰性 32%（PDF p.6）。

## ⭐ 時間序列資料怎麼標記結果（PDF p.5）
詳見 [[time-series-outcome-labeling]]。

```
日期（相對確診日）： ... -5  -4  -3  -2  -1   0  +1 ... +10  +11 ...
標記：               ...  0   0   0   1   1   1  [排除 10 天] 0  ...
                              ↑──── 敗血症 ────↑ ↑── 治療與恢復期 ──↑
```
- **分析單位是「天」**：每位寶寶每天一列資料（當天的心肺指標 + 臨床變項）。
- **結果 = 未來 3 天內是否確診**：血液培養陽性當天與前 2 天標為「敗血症」（1）。
- **確診後 10 天排除**：避開治療與恢復期。
- 其他所有日子標為「無敗血症」（0）。
- **事件率很低**：每天的敗血症率，插管時 1.88%、未插管時 0.36%（PDF p.13–14）。
- **重複測量**：同一寶寶（含雙胞胎等手足）每天的資料彼此相關，以 [[clustered-standard-errors|Huber-White 法]]校正（PDF p.5）。

## ⭐ 研究設計與分析方法
### 資料（PDF p.2–3, p.6）
- [[pre-vent-cohort|Pre-Vent 前瞻性觀察研究]]（NCT03174301），美國 5 家第 IV 級 NICU。
- 737 位寶寶有臨床資料（平均 GA 26.4 週、出生體重 870 g）；719 位有監視器資料。
- 47,512 個有監視器資料的住院日（佔 NICU 住院日的 79%），其中 26% 為插管日。
- 監視器資料可分析的敗血症：123 次（109 位寶寶）。
- 倫理：各中心 IRB 審查；3 個中心免除知情同意、2 個中心需知情同意（PDF p.3）。
- 依 [[tripod-reporting|TRIPOD]] 報告規範撰寫（PDF p.4）。

### 分析步驟（PDF p.5）
1. **比較兩組**：有／無敗血症寶寶的特徵（Wilcoxon、卡方檢定）。
2. **單變項邏輯斯迴歸**：插管與未插管分開，畫出每個特徵的「相對風險曲線」，標出信賴區間不跨 1 的範圍（紅線）。
3. **時間軌跡圖**：畫確診前後各 5 天的特徵中位數，檢定確診前 3 天是否逐日上升 → 區分[[static-vs-dynamic-risk-markers|持續型與變化型風險訊號]]。
4. **多變項模型逐步加入變項**：看每加一組變項，AUC 提升多少。
5. **驗證與評估**：[[cross-validation|10 折交叉驗證]] AUC、[[pseudo-r-squared|McFadden's pseudo R²]]（模型配適）、[[calibration|校準圖]]、特徵重要性（拿掉某特徵後 AUC 下降多少）。
- 工具：R 4.2.3、rms 套件（PDF p.5）。

## 主要結果

### 單變項（PDF p.6）
- **矯正年齡 (PMA) 是最強的單一預測因子**：越小越容易敗血症。
- 呼吸支持越高、吸入氧氣濃度 (FiO2) 越高，風險越高。
- **未插管時**：心跳過慢與呼吸暫停越多、IH80 與 IH90 越長、週期性呼吸越久 → 風險越高。
- **插管時**：IH80 越長、心跳過慢越多 → 風險越高。
- 插管時較常發生敗血症，且發生時的矯正年齡較小（28.4 vs. 30.6 週）（PDF p.17）。

### ⭐ 持續型 vs. 變化型風險訊號（PDF p.6, p.8）
| 類型 | 特徵 | 意義 |
|---|---|---|
| **變化型**（確診前 1–2 天上升） | 呼吸暫停、週期性呼吸、心跳過慢（未插管） | 即將發病的警訊 |
| **持續型**（一直偏高，不在確診前上升） | 低血氧持續時間（IH80） | 本來就屬高風險族群 |

- 插管寶寶的 IH80 從確診前一天到當天有統計上升，但作者認為臨床意義不大（PDF p.6）。
- 作者推測低血氧可能破壞腸道屏障與菌叢，讓細菌進入血液；也可能只是反映「未成熟」（PDF p.8）。

### ⭐ 多變項模型逐步加入變項（PDF p.18, Table 3）
| 模型 | 變項 | cvAUC | pseudo R² |
|---|---|---|---|
| 1 | PMA | 0.739 | 0.067 |
| 2 | + IH80 + 心跳過慢 | 0.763 | 0.081 |
| 3 | + 是否插管 | 0.782 | 0.092 |
| 4 | + 呼吸暫停 + 週期性呼吸 | 0.783 | 0.094 |

- 完整模型校準良好（PDF p.7）。
- 插管與未插管分開建模，沒有比合併模型更好（PDF p.7）。
- ⚠️ 推論：光靠 PMA 就有 0.739，心肺特徵只多加約 0.04；但心肺特徵能提供「快要發病」的時間資訊，這是 PMA 做不到的。

## 作者自述的限制（PDF p.8）
1. 沒有納入所有影響心率與血氧的臨床變項（如呼吸器模式與設定）。
2. 特徵切點是依母研究事先固定的，其他切點可能表現更好。
3. 以「天」為單位分析，可能錯過快速惡化的敗血症。
- 作者強調：模型是用來**檢驗假設**，不是直接拿到床邊使用（PDF p.8）。

## 評析
- 優點：多中心（5 家）、大量高解析度監視器資料、特徵是醫師熟悉的事件、遵循 TRIPOD、有處理重複測量、報告校準度。
- ⚠️ 推論：**只有內部驗證**（交叉驗證），沒有外部驗證；與 [[lin2022point]] 的外部驗證設計形成對照。
- ⚠️ 推論：**利益衝突**：兩位作者持有 Medical Prediction Sciences Corporation 股票，另有作者擔任醫材公司顧問（PDF p.1）。
- ⚠️ 推論：未報告敏感度、特異度、PPV；事件率很低（每天 0.36–1.88%），實際應用時 PPV 可能很低（參考 [[sensitivity-specificity-ppv-npv]]）。
- ⚠️ 推論：資料公開方式原文未提及。

## 與其他文獻的關係
- 與 [[lin2022point]]：都用**常規生理訊號**做預測（Lin：單次 12 導程心電圖；Kausch：連續監視器）。設計差異：Lin 有外部驗證、用深度學習；Kausch 只有內部驗證、用邏輯斯迴歸與醫師熟悉的特徵（可解釋性高）。
- 與 [[ada2026prevention]]：兩篇都提供「預測目標的定義」與「風險因子／特徵」，但疾病不同（成人糖尿病 vs. 新生兒敗血症）。
- 作者引用自己團隊先前在 3 家 NICU 開發並驗證的敗血症預測模型（PDF p.7–8，參考文獻 18，尚未收錄）。

## 對我的研究有什麼用
- **時間序列標記範本** ⭐：「每天一列、未來 N 天內是否發生、事件後排除治療期、校正重複測量」可直接套用到其他連續資料（如穿戴裝置、血糖監測）。
- **研究設計範本** ⭐：單變項風險曲線 → 時間軌跡圖 → 逐步加入變項的多變項模型 → 交叉驗證 + 校準。
- **持續型 vs. 變化型風險**：論文討論段可用的概念框架。

## 本篇新增術語（已加入 glossary）
極早產兒、懷孕週數、矯正年齡、出生後天數、晚發性敗血症、NICU、呼吸暫停、週期性呼吸、間歇性低血氧、血氧飽和度、心跳過慢、侵入性呼吸器、吸入氧氣濃度、血液培養、交叉驗證、校準度、pseudo R²、群集穩健標準誤、TRIPOD、時間序列
