# 工作紀錄 (Log)

> 只新增，不修改。格式：`## [YYYY-MM-DD] 動作 | 對象`

## [2026-11-16] schema | 建立知識庫
建立 CLAUDE.md 與資料夾骨架（doc/、wiki/、output/），以及 index、log、glossary、synthesis 初始頁。
尚未 ingest 任何文獻。

## [2026-11-16] ingest | omar2025multi
第 1 篇（單篇模式）。定位：風險／限制類背景文獻；使用者要求強調模型間比較與研究設計。
新增：papers/omar2025multi；concepts 6 頁；methods 6 頁；keywords 4 頁。
更新：glossary（+16 詞）、overview、research-gaps、index。
注意：PDF 檔名目前為 omar2025multi.pdf.pdf（多了一個副檔名），請使用者修正。

## [2026-11-16] schema | keywords 檔名加 kw- 前綴
避免與 concepts/ 同名（Obsidian 連結會衝突），keywords/ 檔名一律加 `kw-`，例如 `kw-llm-hallucination.md`。

## [2026-11-16] sync | Notion
首次同步到 Notion（閱讀用副本，本機為正本）。頁面對照表見 `notion-map.json`。

## [2026-11-16] sync | Notion 改為每篇論文一套子頁面
使用者選擇：每篇論文底下各自放概念、方法與指標、關鍵字、綜合分析、術語表。本機 wiki 結構不變（共用頁）。跨篇內容移到 Notion「跨篇綜合分析」。CLAUDE.md 7.6 已更新。

## [2026-11-16] ingest | ada2026prevention
第 2 篇（單篇模式）。臨床指引（ADA Standards of Care 2026 第 3 章）。定位：領域知識／臨床背景；使用者要求強調風險因子（預測特徵）與診斷切點（預測目標）。
新增：papers/ada2026prevention；concepts 5 頁（prediabetes、t2d-risk-factors、diabetes-prevention-program、type-1-diabetes-stages、metformin）；methods 4 頁（glycemic-tests、hazard-ratio、person-years、evidence-grading）；keywords 3 頁。
更新：odds-ratio（新增例子）、glossary（+15 詞）、overview（新增主題 2a）、research-gaps（+6）、index。
注意：授權禁止未經許可用於文字探勘／機器學習。

## [2026-11-16] sync | Notion
同步 ada2026prevention（文獻頁＋5 個子頁面＋概念 5、方法 5、關鍵字 3）與跨篇「領域全貌」。notion-map.json 已更新。

## [2026-11-16] schema | 新增文獻來源規則
對話中附上的 PDF、或 arXiv 等網址的 PDF，一律以 citekey 為檔名放進 doc/papers/（CLAUDE.md 7.0）。

## [2026-11-16] ingest | lin2022point
第 3 篇（單篇模式）。台灣三總 AI 心電圖估血鉀。定位：核心文獻；使用者要求強調研究設計（外部驗證、黑盒子實用研究）、評估指標（AUC、PPV 為何低）、AI 判錯者預後差。
新增：papers/lin2022point；concepts 4 頁（dyskalemia、electrocardiogram、ai-enabled-ecg、deep-learning）；methods 8 頁（external-validation、black-box-pragmatic-study、roc-auc、sensitivity-specificity-ppv-npv、c-index、cox-regression、mean-absolute-error、multiple-imputation）；datasets 1 頁（tsgh-ed-ecg-cohort，第一個資料集頁）；keywords 3 頁。
更新：clinical-decision-support、hazard-ratio、odds-ratio、kw-clinical-decision-support、glossary（+21 詞）、overview（填入 2b、新增跨篇觀察）、research-gaps（+6）、contradictions（第一筆）、index。

## [2026-11-16] sync | Notion
同步 lin2022point（文獻頁＋5 個子頁面＋概念 5、方法 10、資料集 1、關鍵字 4）與跨篇「領域全貌」「文獻間矛盾」。資料集頁在 Notion 放在「方法與指標」底下。notion-map.json 已更新。

## [2026-11-16] ingest | kausch2024apnea
第 4 篇（單篇模式）。使用者於對話中上傳，依 7.0 以 citekey 存入 doc/papers/。Pre-Vent 極早產兒敗血症預測。定位：核心文獻；用途：了解疾病與技術、預測特徵與目標；強調研究設計、時間序列結果標記。
新增：papers/kausch2024apnea；concepts 4 頁（late-onset-sepsis、preterm-infant、cardiorespiratory-events、continuous-physiological-monitoring）；methods 7 頁（time-series-outcome-labeling、static-vs-dynamic-risk-markers、cross-validation、calibration、pseudo-r-squared、clustered-standard-errors、tripod-reporting）；datasets 1 頁（pre-vent-cohort）；keywords 3 頁。
更新：external-validation、roc-auc、glossary（+20 詞）、overview（新增 2a-2、2b、跨篇觀察）、research-gaps（+6）、index。
注意：PDF 為 PMC 作者稿，以 PDF 頁碼標示。

## [2026-11-16] sync | Notion
同步 kausch2024apnea（文獻頁＋5 個子頁面＋概念 4、方法 8、資料集 1、關鍵字 3）與跨篇「領域全貌」。notion-map.json 已更新。

## [2026-11-16] schema | 每篇的預設定位與強調
使用者指定：每篇的用途為「了解疾病與技術、找出預測特徵與預測目標」；強調「研究設計（可模仿）」與「時間序列資料怎麼標記結果」。CLAUDE.md 文獻頁模板新增 4 個 ⭐ 區塊；ingest 不再詢問要強調什麼。
已為 omar2025multi、ada2026prevention、lin2022point 補上 4 個區塊（kausch2024apnea 已符合）。

## [2026-11-16] sync | Notion
同步三篇文獻頁新增的 4 個 ⭐ 區塊（omar2025multi、ada2026prevention、lin2022point）。

## [2026-11-16] ingest | lubitz2022detection
第 5 篇（單篇模式，預設定位與強調）。Fitbit Heart Study，穿戴裝置 PPG 偵測心房顫動。定位：核心文獻。使用者另要求補充「自己跑模型需要的技術」。
新增：papers/lubitz2022detection（含「自己跑模型」段）；concepts 4 頁（atrial-fibrillation、photoplethysmography、wearable-devices、cha2ds2-vasc）；methods 2 頁（sliding-window、ppg-af-modeling-pipeline）；datasets 1 頁（fitbit-heart-study）；keywords 3 頁。
更新：sensitivity-specificity-ppv-npv、electrocardiogram、continuous-physiological-monitoring、glossary（+15 詞）、overview（2a-3、2b、跨篇觀察）、research-gaps（+8）、index。

## [2026-11-16] sync | Notion
同步 lubitz2022detection（文獻頁＋5 個子頁面＋概念 4、方法 4、關鍵字 3）與跨篇「領域全貌」。notion-map.json 已更新。

## [2026-11-16] write | slides/omar2025multi.html
依 Notion「文獻 (Papers) › Omar 2025」內容製作 17 張 HTML 導讀投影片，存於 output/slides/。CLAUDE.md 資料夾結構新增 output/slides/。

## [2026-11-16] schema | 投影片樣式規範
使用者指定簡約優雅風：5 色色票、米色內頁、深藍封面、標題襯線體、不用色塊。寫入 CLAUDE.md 7.8；omar2025multi.html 已重新套用。

## [2026-11-16] schema | 多篇整合簡報 graph 工作流程
新增 CLAUDE.md 7.9：三階段（大綱 → 逐頁內容 → 投影片），每階段「產生 → 自動檢查 → 使用者確認」，每關一個檔案；可反覆查 Notion，數字以本機 wiki 核對。資料夾結構新增 output/slides/decks/。
建立第一份簡報 decks/health-data-x-ai/00-brief.md。

## [2026-11-16] schema | 7.9 補充紀錄位置
階段 1 也記查詢紀錄（寫在 01-outline.md）；checks.md 固定格式；階段 3 截圖存 shots/slide-NN.png。
