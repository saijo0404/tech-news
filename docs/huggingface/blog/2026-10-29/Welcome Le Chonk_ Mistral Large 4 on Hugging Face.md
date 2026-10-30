# Welcome Le Chonk: Mistral Large 4 on Hugging Face

- **來源**: Hugging Face
- **發布日期**: 2026-10-29
- **原文連結**: https://huggingface.co/blog/mistral-large4

## 核心主題
Mistral Large 4 (Le Chonk) 是一款由 Mistral AI 開發的多模態、多語言專家混合(MoE)模型，擁有約 1T 總參數和 49B 活躍參數，在網路安全分析、程式碼代理和多模態理解方面表現卓越。

## 關鍵重點
- **卓越的安全能力**：在 Artificial Analysis Cyber Index 測試中獲得 82% 分數，在 Lakera B3 攻擊抗性測試中達到 93.3%，是開源模型中防禦性安全表現最優者之一
- **強大的程式碼能力**：DeepSWE v1.1 測試得分 61.7%，SWE-Atlas-QnA 得分 59.4%，Coding Agent Index 綜合得分 49.8%，超越 DeepSeek V4 Pro 0813 和 Qwen3.8 Max
- **先進的架構設計**：72 層架構結合 Multi-head Latent Attention (MLA) 與 DeepSeek Sparse Attention (DSA)，採用 3:1 RoPE to NoPE 稀疏性設計，每 token 選取 5 位活躍專家（4 位專家 + 1 位共享專家）
- **多模態理解能力**：搭載 1.6B Pixtral 視覺編碼器，支援文字與圖片雙重輸入，可處理多模態任務
- **高效推理支援**：支援 transformers、vLLM、llama.cpp 等多種推理框架，提供 FP8、NVFP4、GGUF 等量化版本，首字時間約 0.6 秒（1K 提示）

## 結論
Mistral Large 4 以其在網路安全分析、程式碼代理和多模態理解方面的卓越表現，成為開源生態系統中的重要成員。其開源授權模式讓使用者可以自主部署和細化，特別適合需要漏洞修復、安全防禦和複雜多模態任務的場景。

---
