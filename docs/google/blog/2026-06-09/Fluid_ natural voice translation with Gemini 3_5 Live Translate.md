# 以 Gemini 3.5 Live Translate 實現流暢自然的語音翻譯

- **來源**: Google Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-live-3-5-translate/

## 核心主題
Google 發布 Gemini 3.5 Live Translate 最新語音模型，支援超過 70 種語言的近即時語對語翻譯，能自動偵測語言、保留說話者的語調與節奏，並以流暢連續的輸出取代傳統輪流式翻譯系統，已在 Google Translate、Google Meet 與 Gemini Live API 中逐步推出。

## 關鍵重點
- **連續流暢翻譯取代輪流模式：在等待上下文與即時同步之間取得平衡**：傳統輪流式翻譯系統需等待說話者說完才回應，Gemini 3.5 Live Translate 則能連續生成翻譯語音，在等待更多上下文以提升品質與即時同步之間取得平衡；模型自動偵測 70 種以上語言，生成的翻譯語音保留說話者的語調、節奏與音高，全程僅落後說話者幾秒鐘，實現無尷尬停頓的流暢音訊體驗；同時具備噪音健壯性，可應對嘈雜、不可預測的環境。
- **多層級推出：開發者公開預覽、企業 Google Meet 私網預覽、大眾 Google Translate App**：（1）開發者：即日起透過 Gemini Live API 與 Google AI Studio 公開預覽，Agora、Fishjam、LiveKit、Pipecat 與 Vision Agents 等開發者平台已整合，Grab 正測試讓司機與乘客在接送時實現多語言近即時溝通（每月超過 1,000 萬通語音通話）；（2）企業：本月起在 Google Meet 以私網預覽推出，語言支援從 5 種擴展至 70 種以上、會話支援超過 2,000 種語言組合（從僅翻譯至/自英語擴展）、介面更新為即時存取語音翻譯；（3）大眾：Google Translate 行動應用程式（Android 與 iOS）全球推出，連線耳機即可體驗跨 70 種語言的流暢翻譯；Android 用戶還可使用新「聆聽模式」，將手機貼近耳朵即可透過手機聽筒直接接收翻譯音訊，無需耳機。
- **合成音訊以 SynthID 隱形浮水印防範誤導資訊**：所有由模型生成的音訊均搭載 SynthID 隱形浮水印，直接編織於音訊輸出中，確保 AI 生成內容可被檢測以防止誤導資訊；詳細安全與責任方針可參考模型卡（model card）。

## 結論
Gemini 3.5 Live Translate 標誌著 Google 自二十年前翻譯實驗以來的重大跨越——從每月處理超過一兆字的翻譯，到如今能連續、自然、跨 70 種語言進行近即時語對語翻譯；它不僅在技術上以連續生成取代輪流等待、在體驗上保留說話者語調節奏、在應用上涵蓋開發者 API 到企業視訊會議再到大眾翻譯 App，更以 SynthID 浮水印確保 AI 內容的安全性；從 Grab 的 1,000 萬月通話量測試到 Google Meet 超過 2,000 種語言組合支援，這項技術正在將語言障礙從「可管理的不便」轉為「幾乎消失的障礙」，重新定義人與人之間的跨語言溝通方式。
