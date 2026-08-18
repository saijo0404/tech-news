# Distributed Layerwise Offload

- **來源**: vllm.ai
- **發布日期**: 2026-08-17
- **原文連結**: https://vllm.ai/blog/2026-08-17-distributed-layerwise-offload

## 核心主題
vLLM-Omni 的 DLO 技術使大型擴散模型能跨多張 NPU/GPU 運行，最小化主機記憶體佔用。

## 關鍵重點
- **Meta-device + mmap 權重載入**：冷啟動峰值記憶體降低 73%（178GB→47GB）
- **權重分片 + AllGather**：每 rank 僅存 1/dp_size 權重，全層權重於運算時重建
- **雙緩衝預取**：HBM 僅存 2 層權重，與總層數無關
- **DP 多並行**：3.3× 吞吐量提升（vs 單請求 HSDP）
- **平台支援**：支援 NVIDIA GPU (CUDA/NCCL) 與 Ascend NPU (CANN/HCCL)
- **記憶體複雜度**：O(model_size + dp_size × constant)

## 結論
DLO 技術在 Ascend NPU 與 NVIDIA B300 GPU 平台上均驗證有效，可大幅降低記憶體佔用並提升推理吞吐量，特別適合部署大型擴散模型。
---