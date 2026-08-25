# How NVIDIA Groq 3 LPX Unlocks Ultrafast Interactivity at Long Context on NVIDIA Vera Rubin

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-24
- **原文連結**: https://developer.nvidia.com/blog/how-nvidia-groq-3-lpx-unlocks-ultrafast-interactivity-at-long-context-on-nvidia-vera-rubin/

## 核心主題
NVIDIA Groq 3 LPX 與 Vera Rubin NVL72 平台合作，在長上下文場景下實現了世界級的互動速度，為多代理系統和超大模型服務提供強大支援。

## 關鍵重點
- **世界級互動速度**：在 Artificial Analysis 100K 上下文測試中，使用 Gemma 4 31B 模型達到 3,431 tokens/秒的輸出速度，遠超一般服務標準。
- **確定性編譯器調度**：Groq 3 LPX 採用確定性執行模型，編譯器可預先規劃晶片間數據傳輸至時鐘週期級別，大幅降低首比特延遲。
- **細粒度計算 - 通信重疊**：編譯器可在 320 字節向量級別上重疊計算與通信，使數據傳輸與計算工作負載最大化重疊。
- **多配置協同服務**：支援與 Vera Rubin NVL72 的多種協同配置，包括預填充 - 解碼分散、注意力-FFN 分散和推測外部草稿解碼，可擴展至多兆比爾參數模型。

## 結論
NVIDIA Groq 3 LPX 透過其獨特的確定性架構和先進的晶片間通信技術，成功解決了長上下文高互動性推理的挑戰，使 Vera Rubin 平台能夠服務多代理系統，支持 2T+ 參數模型的高互動性服務，為 AI 工廠和用戶體驗帶來革命性提升。

---