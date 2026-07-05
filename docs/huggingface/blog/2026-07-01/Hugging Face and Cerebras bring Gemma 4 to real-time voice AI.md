# Hugging Face and Cerebras bring Gemma 4 to real-time voice AI

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-01
- **原文連結**: https://huggingface.co/blog/cerebras-gemma4-voice-ai

## 核心主題
Hugging Face 與 Cerebras 合作展示了一套**開放式串接式語音對語音（speech-to-speech）架構**——以 Cerebras 極速推論搭配 Google DeepMind Gemma 4 31B 語言模型與阿里雲 Qwen3TTS 語音合成，打造延遲極低、體驗自然的即時語音 AI 對話系統。

## 關鍵重點
- **開放模組化語音對話架構**：系統由四層串接而成——①**語音輸入 → Parakeet（Nvidia）語音辨識** → ②**Gemma 4 VLM（Cerebras 推論）** → ③**Qwen3TTS（阿里雲）文字轉語音** → ④**語音回覆**。每一層都是開放、可獨立檢視、修改與替換的模組，開發者可自由調整為不同助手、機器人或研究專案。
- **Cerebras 解決語言模型延遲瓶頸**：許多生產系統雖然中位數延遲尚可，但 P95 仍會出現令人挫折的數秒延遲，尤其在工具呼叫或多模態步驟需要多輪交談時更明顯。Cerebras 解決了堆疊中最關鍵的瓶頸——語言模型回應時間——透過大幅提升推論速度與穩定性，讓整個 Hugging Face 管線發揮最大效能。穩定性特別重要於「長尾」表現：許多系統能提供可接受的中位數延遲，但偶發的慢速回應仍會讓人感覺不可靠。
- **從聊天室到真實世界互動**：這套語音對話管線已實際部署於 **Reachy Mini 機器人**，全球已有超過 **9,000 台機器人在運作**。對機器人、語音助手與具身 AI 而言，回應速度不是美觀上的改善——它是讓互動感覺「有生命力」的關鍵。合作的核心理念是：開放模型、開放基礎建設與突破性的推論速度共同構成下一代對話式 AI 的基礎。

## 結論
Hugging Face 與 Cerebras 的示範證明：**即時語音 AI 的關鍵不在於單一模型的品質，而在於整個堆疊的延遲控制**。透過將開放元件（Nvidia Parakeet、Gemma 4、Qwen3TTS）與 Cerebras 的極速推論整合，開發者能以模組化方式建構自然流暢的語音對話體驗——不僅限於聊天機器人，更延伸至機器人與具身 AI 等真實世界應用。這套架構與程式碼已開放於 Hugging Face Space 與 GitHub，邀請社群共同推動即時語音 AI 的下一步。

---
