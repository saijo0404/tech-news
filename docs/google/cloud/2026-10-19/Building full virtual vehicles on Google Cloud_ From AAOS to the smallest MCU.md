# Building full virtual vehicles on Google Cloud: From AAOS to the smallest MCU

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-20
- **原文連結**: https://cloud.google.com/blog/topics/manufacturing/building-full-virtual-vehicles-on-google-cloud-from-aaos-to-the-smallest-mcu/

## 核心主題
這篇文章介紹了 Google Cloud 如何幫助汽車製造商將整輛車（從 AAOS 到最小 MCU）都虛擬化，以實現軟體定義車輛的完整開發流程。

## 關鍵重點
- 目前汽車製造商只在數位娛樂系統上實現雲端開發，但大多數控制模組仍依賴實體硬體，導致開發效率受限
- Google 透過 Cuttlefish 環境讓 AAOS 在雲端運行，並擴展到其他領域，實現「代表性軟體、代表性架構、雲端部署」
- RemotiveTopology 作為虛擬車輛的「Harness」，將 AAOS 與完整的 E/E 架構連接起來，實現 vehicle-as-code 的虛擬車輛
- 透過雲端完整模擬車輛，開發者可以在整合階段之前就發現跨領域整合問題，大幅縮短開發週期
- Google Axion 提供 C4A metal 裸機 Arm 實例，讓雲端軟體能直接運行在車輛控制模組上，實現雲端與車輛的軟體一致性
- 客戶案例顯示整合週期可縮短 10 倍以上，AI 輔助工作流可快速生成、測試和優化車輛軟體

## 結論
透過將車輛視為程式碼並移至雲端開發，汽車製造商可以大幅縮短開發週期，實現真正的軟體定義車輛，並降低硬體依賴帶來的開發瓶頸。

---