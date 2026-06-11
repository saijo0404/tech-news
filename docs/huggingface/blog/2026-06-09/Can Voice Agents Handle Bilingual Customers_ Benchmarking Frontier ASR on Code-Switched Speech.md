---
# Can Voice Agents Handle Bilingual Customers? Benchmarking Frontier ASR on Code-Switched Speech

- **來源**: Hugging Face Blog (ServiceNow-AI)
- **發布日期**: 2026-06-09
- **原文連結**: https://huggingface.co/blog/ServiceNow-AI/code-switching

## 核心主題
ServiceNow 與 Hugging Face 團隊針對企業客服中常見的跨語交錯（code-switching）現象，建立並公開首個專為雙語語音辨識測試的基準與資料集，評估七種前沿 ASR 模型在四組語言對上的表現，發現最佳模型的代碼切換懲罰遠低於預期。

## 關鍵重點
- **基準與資料集設計**：涵蓋西班牙語-英語、法語-英語、加拿大法語-英語與德語-英語四組語言對，利用 GPT-5 產生 918 筆 HR 與 ITSM 場景的交錯語句，並經 ElevenLabs Multilingual V2 合成語音、母語語言學家人工審查；評估使用 WER（字元準確度）、SWER（語義字元錯誤）與 AER（下游任務回答錯誤）三項指標。
- **頂尖模型與代碼切換成本**：ElevenLabs Scribe V2、Google Gemini 3 Flash 與 AssemblyAI Universal 3-Pro 整體表現最佳；與單語語音相比，最佳模型僅增加約 1-2% 的 WER，而較差模型如 Whisper 在德語-英語情境下則惡化達 85%。值得注意的是，錯誤集中於語句中的「英語部分」而非母語部分，且切換次數影響錯誤發生率、語料混合密度（CMI）則決定錯誤幅度。
- **語義指標揭示模型差異**：在 WER 排名第三的 AssemblyAI 在 AER 上敗給 Gemini 3 Flash，因 Gemini 作為大型語音語言模型（LALM），在保留語意與推理方面具優勢；Deepgram Nova-3 雖 SWER 中等，但 AER 墊底，顯示其在關鍵細節上的語義錯誤比例較高。

## 結論
跨語交錯正從「壓力測試」轉變為「正常條件」；企業應根據自身客戶實際使用的語言對來選擇 ASR 系統，因為不同語言組合的最佳模型差異顯著。研究團隊已公開資料集（ServiceNow-AI/asr_codeswitched）與評估工具（AU-Harness）供社群使用。

---
