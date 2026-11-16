---
type: concept
aliases: [Continuous physiological monitoring, Bedside monitor, Waveform data, 床邊連續監測, 生理訊號, HeRO]
---
# 床邊連續生理監測（Continuous Physiological Monitoring）

## 白話解釋
加護病房的監視器 24 小時記錄心跳、呼吸、血氧的**波形**。平常醫護只看當下數字；若把這些長時間的資料存下來用演算法分析，可以找出人眼看不出的「快要生病」訊號。

## 在文獻中怎麼被使用
- [[kausch2024apnea]]：
  - 從胸阻抗、心率、SpO2 波形自動計算心肺事件指標（PDF p.4）。
  - 有監視器資料的住院日佔 79%（PDF p.6）。
  - 前人工具 **HeRO 心率特徵指數**：偵測心率變異度下降與短暫減速，預測 24 小時內的敗血症樣疾病（PDF p.3, p.7）。
  - 本研究以「天」為單位彙總，可能錯過幾小時內的快速變化（PDF p.8）。

## 與其他資料型態比較
- ⚠️ 推論：[[lin2022point]] 用的是**單次** 10 秒心電圖；本頁是**連續數週**的監測資料，可以看「變化趨勢」，但資料量大、需要處理遺漏與時間結構。
- [[lubitz2022detection]]：穿戴裝置的 PPG 也是一種連續監測，在日常生活（尤其睡眠中）收集資料（p.1416, p.1419）。見 [[wearable-devices]]。

## 相關頁面
[[cardiorespiratory-events]]、[[time-series-outcome-labeling]]、[[electrocardiogram]]
