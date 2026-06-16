---
# NVIDIA Blackwell Tops MLPerf Training 6.0 with Industry-Leading Scale and Performance

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://developer.nvidia.com/blog/nvidia-blackwell-tops-mlperf-training-6-0-with-industry-leading-scale-and-performance/

## 核心主題
NVIDIA Blackwell 平台在 MLPerf Training v6.0 中拿下全部賽事的冠軍，是唯一提交所有新舊測試結果的平台，展現從 512 顆至 8,192 顆 GPU 的超大規模訓練能力，並透過 DeepSeek-V3 等 MoE 模型驗證生產級雲環境的可靠性。

## 關鍵重點
- **六大軟體創新驅動效能突破**：（1）首次為 token-dropless MoE 實現完整迭代 CUDA Graph，消除 CPU-GPU 同步瓶頸；（2）CuTe DSL 實現記憶體帶寬限制層與 grouped GEMM 融合，為 DeepSeek-V3 帶來超過 8% 端到端加速、GPT-OSS 達 93%；（3）MXFP8 注意力區塊在不影響模型品質前提下提供加速；（4）MoE Router 元素運算融合帶來 5 倍 kernel 加速；（5）1F1B all-to-all 重疊優化達成接近 100% 通訊重疊；（6）pipeline 不平衡降至 1% 以下。
- **硬體規模與網路協同**：GB300 NVL72 系統以 72 顆 Blackwell Ultra GPU 加上 36 顆 Grace CPU 組成單一運算節點，雲端合作夥伴在分散式資料中心擴展至 8,192 顆 GPU。Spectrum-X 乙太網路的進階適配路由與擁塞控制有效解決 MoE 模型的突發流量問題，使 all-to-all 通訊延遲被隱藏於計算之後。GB300 相比 GB200 提供更大記憶體與電源預算，進一步降低跨 GPU 通訊等待。
- **持續全堆疊協同設計帶來即時效能紅利**：僅透過軟體優化（cuDNN、Transformer Engine、Megatron Core 等），DeepSeek-V3 在短短三個月內訓練效能提升 1.3 倍（從 1,298 至 1,648 TFLOPS/GPU），無需更動硬體。現有基礎設施投資可隨著軟體生態成熟持續獲得訓練效率紅利。

## 結論
MLPerf Training 6.0 不僅是一場基準測試的胜利，更是 NVIDIA 全堆疊方法論成為業界加速複雜生成式 AI 工作負載之標準的證明——硬體能力僅是基礎，真正決定企業 AI 進展速度的是持續的軟體創新、極致的全堆疊優化，以及在大規模生產環境中可靠交付效能的能力。

---
