# 將最新 Gemini 模型提供給 Apple 開發者

- **來源**: Google Blog
- **發布日期**: 2026-06-08
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/bringing-gemini-models-to-apple-developers/

## 核心主題
Google 宣布 Gemini 模型現已整合至 Apple 生態系——開發者可透過 Foundation Models 框架直接呼叫雲端 Gemini 模型，並在 Xcode 中使用 Gemini 協助程式碼開發，加速智慧應用與代理式體驗的建構。

## 關鍵重點
- **Foundation Models 框架開放第三方模型：Gemini 透過 Firebase Apple SDK 原生接入**：Apple 於 WWDC 宣布開放 Foundation Models 框架（從 iOS 27、macOS 27、iPadOS 27、visionOS 27、watchOS 27 起）給第三方雲端模型提供者；Google 已透過 Firebase Apple SDK 將 Gemini 模型整合至此框架——開發者可使用相同的 API 介面在裝置端 Apple 模型與雲端 Gemini 模型之間輕鬆切換，實現靈活的代理式應用體驗並最佳化成本與延遲；Firebase AI Logic 讓開發者無需建置獨立後端伺服器，即可將 Gemini 直接整合至 iOS/macOS/iPadOS/visionOS 應用中，並透過 Firebase App Check 防護 API 免受濫用。
- **Xcode 原生整合 Gemini：在開發環境內直接進行代理式程式碼工作流**：Google 與 Apple 合作將 Gemini 整合至 Xcode 開發環境，開發者可在不切換工具或視窗的情況下執行複雜的多步驟任務；Gemini 可協助審查程式碼、修復錯誤並加速新功能開發；開發者可透過 Xcode 的 Intelligence 設定面板啟用——個人開發者可從 Google AI Studio 取得自服務 Gemini API 金鑰（含免費層），企業開發者則可透過 Gemini Enterprise Agent Platform 取得金鑰，使用組織專屬的企業配額與資料隱私參數。
- **雙軌認證模式：個人自服務與企業專屬配额兼顧不同開發需求**：針對不同規模的開發者，Gemini 提供兩種認證與授權選項——個人開發者可從 Google AI Studio 取得自服務 API 金鑰，使用免費層開始探索或付費層使用進階模型與更高用量；企業開發者可透過 Gemini Enterprise Agent Platform 取得金鑰，讓開發團隊利用組織的專屬企業配額與資料隱私保障；兩種模式讓從個人開發者到大型企業的 Apple 生態系開發者都能無縫接入 Gemini 能力。

## 結論
Google Gemini 深度整合 Apple 生態系標誌著兩大科技巨頭在開發者工具層面的策略性結合——從 Foundation Models 框架的原生模型接入，到 Xcode 開發環境內的代理式程式碼輔助，Google 提供了一條從「雲端模型呼叫」到「本地開發效率提升」的完整路徑；透過 Firebase AI Logic 免去後端建置的負擔、透過雙軌認證滿足個人到企業的不同需求，這項整合讓 Apple 開發者能以最小的程式碼變更將 Gemini 能力融入應用，同時在 Xcode 內獲得 AI 輔助開發的加速體驗；這不僅是技術整合，更是 Google 持續擴展 Gemini 生態版圖的關鍵一步。
