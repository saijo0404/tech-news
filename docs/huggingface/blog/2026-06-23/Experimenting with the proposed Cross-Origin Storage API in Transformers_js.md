---
# Experimenting with the proposed Cross-Origin Storage API in Transformers.js

- **來源**: Hugging Face Blog（Google Chrome 團隊客座文章）
- **發布日期**: 2026-06-23
- **原文連結**: https://huggingface.co/blog/cross-origin-storage

## 核心主題
Chrome 團隊與 Hugging Face 合作實驗 WICG 提出的 Cross-Origin Storage（COS）API——以密碼雜湊而非 URL 或來源標識檔案，讓不同來源的網頁應用程式可共享大型模型權重與 Wasm 執行時間檔，解決當前瀏覽器快取隔離導致的重複下載與儲存浪費問題。

## 關鍵重點
- **快取隔離帶來的重複下載挑戰**：Transformers.js 應用在不同來源（origin）下運行時，即使下載完全相同的 AI 模型（如 Xenova/whisper-tiny.en，177 MB）或共享的 Wasm 執行時間檔（ort-wasm-simd-threaded.asyncify.wasm，4,733 kB），瀏覽器仍因 Network Isolation Key 將快取隔離而無法命中，導致重複下載與磁碟空間浪費。
- **COS API 以雜湊為鍵的跨來源共享機制**：`navigator.crossOriginStorage.requestFileHandle(hash)` 透過 SHA-256 雜湊識別檔案——若檔案已在 COS 中則直接讀取（快取命中），否則下載後寫入 COS 供後續所有來源使用。支援 `origins` 參數精細控制可見性：`'*'` 全域公開、指定來源列表限內部共享、省略則限同站來源；可見性可升級不可降級，防止惡意行為縮窄公開資源的存取範圍。
- **完整性驗證、隱私保護與實際應用**：瀏覽器在寫入時自動驗證資料與雜湊吻合，確保檔案完整性；隱私方面透過 `origins` 控制與可用性閾值（單一來源的檔案可能被隱藏以防火跡識別）緩解側信道風險。Transformers.js 已以 `env.experimental_useCrossOriginStorage = true` 旗標實驗性支援 COS，配合 Chrome 延伸模組可立即測試——相同模型跨來源僅下載一次。WebLLM、wllama 等專案也正跟進實驗。

## 結論
Cross-Origin Storage API 以「雜湊即鍵」的設計理念，在隱私與實用性之間取得平衡，讓 Web 端 AI 應用不再因來源隔離而重複下載相同的模型與執行時間資源。目前 API 仍為早期提案、尚未原生實作於任何瀏覽器，但開發者可透過延伸模組立即測試；Transformers.js 等函式庫已率先在程式庫層級導入實驗性支援，為 Web AI 的效能與成本優化開拓一條新路。

---
