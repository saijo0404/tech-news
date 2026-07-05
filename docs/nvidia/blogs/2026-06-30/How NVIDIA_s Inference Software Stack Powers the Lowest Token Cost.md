# How NVIDIA's Inference Software Stack Powers the Lowest Token Cost

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://blogs.nvidia.com/blog/inference-software-lowest-token-cost/

## 核心主題
NVIDIA 解釋其推理軟體堆疊如何與 Blackwell 硬體協同優化，將 DeepSeek V4 等模型的 token 成本降低高達 **5 倍**，並透過分散式服務、大型專家平行處理、NVFP4 精度和多 token 預測等技術組合，將 Blackwell GPU 的 token 吞吐量提升高達 **20 倍**。

## 關鍵重點
- **從晶片規格到 token 成本的范式轉移**：AI 企業已從「峰值晶片效能」轉向「每 token 成本」作為基礎設施決策的核心指標——即每美元、每瓦特能在要求的延遲目標內產生多少有價值的 token。NVIDIA 軟體堆疊與 GPU、CPU、網路和系統共設計，在僅一個月內就將 DeepSeek V4 的 token 成本降低達 5 倍。Baseten 使用 TensorRT-LLM 在 Blackwell 上提供 DeepSeek V4 Pro，額外提升 50% token/秒；DigitalOcean 協助 Hippocratic AI 將推理吞吐量提升 30% 並維持不到 0.5 秒的首次回應時間。
- **軟體堆疊的三層架構驅動系統級效益**：推理軟體堆疊連接三個層次——**生產操作層**（分散式服務、編排、自動擴展和記憶體管理）、**應用程式加速層**（運算與通訊重疊、kernel 融合等執行時期最佳化）和**基礎設施存取層**（暴露 GPU、網路和記憶體能力，無需開發者管理每個裝置指令集）。當這些層級協同運作時，分散式服務、大型專家平行處理、NVFP4 精度和多 token 預測單獨帶來顯著增益，組合後吞吐量提升高達 **20 倍**。Agentic AI 的分布式、有狀態工作流讓複雜性成為分散式運算問題，而軟體堆疊決定這種複雜性是轉化為浪費還是更低成本。
- **開放原始碼生態系的加速飛輪**：CUDA 原生框架（如 PyTorch、vLLM、SGLang）讓新研究能快速轉為生產效能。PyTorch 自 2016 年推出以來與 NVIDIA 架構共同演進，讓 Tensor Cores、Transformer Engine 和 NVFP4 等創新直接可用。當 DFlash 預測解碼（現有硬體吞吐量提升 15 倍）或 FastVideo（五秒內生成 1080p 影片）進入 PyTorch 後，可立即在 NVIDIA 上執行。DeepSeek V4 在 Blackwell 上從發布日起，vLLM 和 SGLang 框架的效能約一個月內提升 5 倍，token 成本降至約原先的五分之一。

## 結論
NVIDIA 的推理軟體堆疊證明：AI 基礎設施的競爭不僅取決於硬體規格，更取決於軟體如何將硬體潛力轉化為實際的 token 經濟效益。透過三層協同設計的軟體架構加上開放原始碼生態系的正向循環，NVIDIA 正在重新定義 AI 推理的成本曲線——讓更複雜的 Agentic AI 工作流以可負擔的成本運行於生產環境。

---
