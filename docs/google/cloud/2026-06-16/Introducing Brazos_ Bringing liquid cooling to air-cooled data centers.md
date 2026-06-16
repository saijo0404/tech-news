---
# Introducing Brazos: Bringing liquid cooling to air-cooled data centers

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://cloud.google.com/blog/topics/systems/brazos-liquid-cooling-system-for-air-cooled-data-centers/

## 核心主題
Google 推出 Brazos 機櫃式封閉迴路液對氣散熱系統，讓企業能在既有風冷資料中心內部署高密度液冷設備，無需耗資大量資本與時間改造整座設施的冷凍水回路。

## 關鍵重點
- **即插即用液冷架構**：Brazos 由三個獨立散熱單元與整合式機櫃匯流排組成，每套模組佔用 11 OU 機櫃高度，可支援每台機櫃 60 kW 熱負載，將元件級液冷採熱轉換為高效液對氣熱交換器排入熱通道，相容於任何具有足夠電力與標準空氣處理的既有設施。
- **技術規格與安全設計**：使用去離子（DI）水或 25% 丙二醇混合液（PG25）作為冷卻劑，運行於 40–60 V DC 輸入並直接連接標準機櫃匯流排；通過 UL/CSA/IEC 62368-1 認證，內建洩漏偵測與洩壓閥。泵浦與風扇均設計為熱插拔可現場更換模組（FRU），搭配低摩擦滑軌便於快速維護，最大化可用率。
- **快速部署與開放原始碼**：Brazos 打破資料中心更新需耗時數月的傳統，允許以單一機櫃為單位逐步安裝；Google 即將透過 Open Compute Project 論壇正式開放 Brazos 技術規格、設計原則與視覺資產，邀請系統架構師、製造商與熱工程師共同擴展機櫃級散熱基礎建設。

## 結論
Brazos 在液冷效能與風冷操作簡便性之間取得平衡，為面臨千瓦等級 AI 與 HPC 晶片散熱挑戰的企業提供了一條無縫遷移路徑，同時以開放原始碼策略促進整個產業生態圈的創新與規模化。

---
