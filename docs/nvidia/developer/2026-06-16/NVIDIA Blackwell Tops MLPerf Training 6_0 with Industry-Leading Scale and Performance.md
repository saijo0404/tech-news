---
# NVIDIA Blackwell Tops MLPerf Training 6.0 with Industry-Leading Scale and Performance

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://developer.nvidia.com/blog/nvidia-blackwell-tops-mlperf-training-6-0-with-industry-leading-scale-and-performance/

## 核心主題
NVIDIA Blackwell 平台在 MLPerf Training v6.0 中拿下全部七項基準測試的冠軍，是唯一提交所有新舊測試結果的平台，涵蓋 DeepSeek-V3 671B 等 MoE 模型至 8,192 顆 GPU 的超大規模生產級雲端部署，展現訓練速度、規模與可靠性三大優勢。

## 關鍵重點
- **GB300 NVL72 硬體升級與網路協同**：GB300 憑藉更大記憶體容量、電源預算與 NVFP4 低精度支援，較 GB200 最高提升 1.6 倍訓練效能。Spectrum-X 乙太網路的進階適配路由與擁塞控制有效解決 MoE 突發流量問題，使 all-to-all 通訊延遲隱藏於計算之後；雲端合作夥伴成功擴展至 8,192 顆 GPU 同步運作。
- **六大軟體創新消除微瓶頸**：（1）首次為 token-dropless MoE 實現完整 CUDA Graph，消除 CPU-GPU 同步；（2）CuTe DSL 核心融合為 GPT-OSS 帶來 93% 端到端加速；（3）MXFP8 注意力區塊與 Router 運算融合分別提供加速與 5 倍 kernel 效能；（4）1F1B all-to-all 重疊達近 100%；（5）Pipeline 不平衡降至 1% 以下。
- **持續全堆疊協同設計帶來即時效能紅利**：僅透過 Megatron Bridge、cuDNN、Transformer Engine 等軟體層優化，DeepSeek-V3 在三個月內訓練效能提升 1.3 倍（1,298 至 1,648 TFLOPS/GPU），無需更動硬體。8,192 GPU 大規模部署驗證平台能可靠地將數月訓練週期壓縮至數分鐘。

## 結論
NVIDIA Blackwell 在 MLPerf Training 6.0 中展現的「最快、最大、最強」不僅是基準測試的胜利，更是全堆疊方法論成為業界加速複雜生成式 AI 工作負載之標準的證明——硬體僅是基礎，真正決定企業 AI 進展速度的是持續軟體創新、極致全堆疊優化，以及在大規模生產環境中可靠交付效能的能力。

---
