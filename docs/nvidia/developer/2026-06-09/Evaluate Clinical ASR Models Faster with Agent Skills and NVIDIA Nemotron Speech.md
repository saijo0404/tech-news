---
# Evaluate Clinical ASR Models Faster with Agent Skills and NVIDIA Nemotron Speech

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://developer.nvidia.com/blog/evaluate-clinical-asr-models-faster-with-agent-skills-and-nvidia-nemotron-speech/

## 核心主題
NVIDIA 提出一套結合 AI 代理技能與合成資料生成（SDG）的臨床自動語音辨識（ASR）評估流程，讓開發者能快速建立專科導向的語音測試基準，並透過結構化的品質飛輪循環持續改善模型表現。

## 關鍵重點
- **臨床語音的特殊挑戰與合成資料優勢**：一般語音模型容易在藥物名稱、手術程序、解剖術語等臨床專科用詞上失準；合成語音不含患者隱私資料（PHI），可自由版本控制與分享，且能精確控制發音，讓團隊能在數小時內建立專科基準測試，無需收集真實臨床錄音或等待 IRB 核准。
- **AI 代理技能引導的結構化評估飛輪**：透過 NVIDIA agent skills 引導五階段循環（設定 → 建構基準 → 評估 ASR → 改善模型 → 重新評估），agent 會逐項詢問專科背景、已知錯誤模式與困難詞彙，自動生成含 SSML 音標標記的合成語音，並在發音不確定時暫停等待人工審查，確保音標品質。
- **實體層級指標驅動的精準改善**：評估技能不只報告整體詞錯誤率（WER），更重點追蹤關鍵字錯誤率（KER）等實體層級指標，當發現特定類別（如藥物名稱）錯誤集中時，可針對性擴充詞彙覆蓋或進行模型微調；若發音涵蓋不足導致分數低落，系統會自動導回建構階段而非盲目微調。

## 結論
此流程將臨床 ASR 的評估從一次性資料集升級為可重複的改進循環，結合 NeMo Data Designer 的文本擴增、Magpie TTS Multilingual 的發音控制合成語音，以及 NVIDIA Nemotron Speech 的語音辨識服務，讓開發者能以對話式的方式快速建立專科基準、審查發音、生成合成語音，並根據實體層級指標做出精確的改善決策。

---
