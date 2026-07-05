# NVIDIA Blackwell 在金融 LLM 推理創下 STAC-AI 紀錄

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-27
- **原文連結**: https://developer.nvidia.com/blog/nvidia-blackwell-sets-stac-ai-record-for-llm-inference-in-finance/

## 核心主題
NVIDIA Blackwell 架構在 STAC-AI LANG6 基準測試中創下金融業 LLM 推理新紀錄，使用 Llama 3.1 8B/70B 模型搭配 NVFP4 量化技術，展現高達 2.8 倍效能提升。

## 關鍵重點
- **STAC-AI 基準測試**：測試 Llama 3.1 8B 與 70B 模型在 EDGAR4（中等長度上下文）與 EDGAR5（長上下文）金融報告摘要任務，涵蓋批處理模式（吞吐量）與互動模式（反應時間與每用戶吞吐量）。
- **Blackwell 顯著性能提升**：HGX B200（8 顆 B200 GPU）在批處理模式下相比 GH200 達 2.8 倍吞吐提升；互動模式下同時維持更高吞吐量與更低延遲（95% 百分位 RT 與 IWL 皆更優）。
- **多平台部署彈性**：GH200 單一伺服器、HGX B200 雲端叢集、RTX PRO 6000 Blackwell 雙 GPU 工作站皆能展現 Blackwell 效能，且 Red Hat OpenShift 容器平台對 GPU 密集型 LLM 推理無額外延遲。

## 結論
NVIDIA Blackwell 憑藉 NVFP4 量化與 TensorRT LLM 框架，在金融業 RAG 與 LLM 推理工作負載上達到前所未有的吞吐量與互動性平衡，為即時金融分析與投資策略生成奠定強大基礎。
