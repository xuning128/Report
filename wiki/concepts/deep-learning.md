---
type: concept
aliases: [Deep Learning, DLM, CNN, 卷積神經網路, 深度學習模型]
---
# 深度學習（Deep Learning）

## 白話解釋
一種機器學習方法，用很多層的「人工神經網路」從大量資料中自己找規則。**卷積神經網路 (CNN)** 擅長處理圖片和波形，例如心電圖。

## 在文獻中怎麼被使用
- [[lin2022point]]：ECG12Net 是 82 層卷積神經網路，以 66,000 張已標註心電圖訓練（p.1, p.10）。
- 深度學習在大型已標註心電圖資料集上可達到人類專家水準（p.1）。

## 優點／限制
- 限制：黑盒子，難以解釋判斷依據；作者用 class activation mapping 與注意力機制輔助呈現（[[lin2022point]] p.10）。

## 相關頁面
[[ai-enabled-ecg]]、[[large-language-model]]
