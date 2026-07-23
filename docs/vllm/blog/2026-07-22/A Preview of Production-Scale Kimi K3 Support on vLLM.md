# A Preview of Production-Scale Kimi K3 Support on vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-07-22
- **原文連結**: https://vllm.ai/blog/2026-07-22-kimi-k3-preview

## 核心主題
vLLM 團隊正在為 Moonshot AI 的 Kimi K3 模型（2.8 兆參數、100 萬 token 上下文）準備 Day-0 開源服務支援，包括 KDA 感知的前綴快取和多模態整合。

## 關鍵重點
- **混合注意力架構挑戰**：Kimi K3 採用 KDA 主導的線性注意力與週期性全注意力層結合，需要 vLLM 進行核心快存架構調整，將物理 KDA 狀態塊大小與前綴匹配粒度分離，實現更精細的前綴快取匹配。
- **硬體優化進展**：NVIDIA 和 AMD 支援已就位，包含 FlashKDA 整合、AttnRes 核核融合、MXFP4 MoE 執行以及 SiTU 激活函數支援。AMD 已部署 FlyDSL MoE 核核並通過初步驗證。
- **Day-0 開源服務**：vLLM 已準備模型實現、Docker 映像、部署食譜和生產驗證，預計在模型權重發布時即可提供完整開源服務。
- **合作夥伴驗證**：已選定的可信合作夥伴（經 Moonshot AI 和 vLLM/Inferact 團隊批准）已開始使用相同代碼進行部署驗證。
- **性能優化重點**：針對 Kimi K3 的 KDA 前綴快取、Attention Residuals、MoE 路由和 MLA 模組進行了深度優化，特別針對 PD 分散部署進行了手動核核融合。

## 結論
vLLM 與 Moonshot AI 團隊緊密合作，已實現模型整合、快存優化及硬體支援，預計在權重發布時即可提供完整開源服務。這種分離式發布策略（先發布模型，後發布權重和推理引擎支援）為雙方提供了更穩定的整合窗口，值得更多模型廠商參考。

---

最後，vLLM 團隊感謝 Moonshot AI、NVIDIA、AMD 團隊以及更廣泛的開源社區的貢獻與支持。