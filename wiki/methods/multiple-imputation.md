---
type: method
aliases: [Multiple imputation, MICE, 多重插補, missing data, 遺漏值]
---
# 多重插補（Multiple Imputation）

## 白話解釋
病歷資料常有缺漏（例如某項檢驗沒做）。多重插補是根據其他資料，**合理猜測**缺漏值好幾次，分別分析後再合併結果，比直接刪掉有缺漏的人更不容易產生偏誤。

## 在文獻中怎麼被使用
- [[lin2022point]]：多變項分析中的遺漏值以多重插補處理（引用 R 的 mice 套件）（p.10）；同時重新設計電子病歷欄位為必填，從源頭減少遺漏（p.10）。

## 相關頁面
[[black-box-pragmatic-study]]
