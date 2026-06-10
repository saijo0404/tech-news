---
# NVIDIA Dynamo Snapshot：Kubernetes 上推理工作負載的快速啟動技術

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-27
- **原文連結**: https://developer.nvidia.com/blog/nvidia-dynamo-snapshot-fast-startup-for-inference-workloads-on-kubernetes/

## 核心主題
NVIDIA 推出 Dynamo Snapshot，利用 Checkpoint/Restore 技術解決 Kubernetes 上 AI 推理工作負載的冷啟動問題，將單一 GPU 推理節點的啟動時間從數分鐘縮短至數秒。

## 關鍵重點
- **冷啟動痛點**：Kubernetes 上冷啟動推理工作負載需數分鐘，期間 GPU 分配但處於閒置狀態，增加 SLA 違約風險。Dynamo Snapshot 結合 CRIU 與 cuda-checkpoint 實現全狀態檢查點與恢復。
- **三大優化技術**：(1) KV cache 解綁與釋放：減少檢查點大小（Qwen3-0.6B 從 190 GiB 降至 6 GiB）；(2) CRIU 效能提升：平行 memfd 恢復與 Linux 原生 AIO，使恢復速度達上游 CRIU 的 2.8–7.9 倍；(3) GPU 記憶體服務（GMS）：將模型權重從檢查點分離，實現並行恢復。
- **極致性能提升**：結合 GMS 與本地 NVMe SSD 條帶化，gpt-oss-120b 推理節點恢復時間縮短 21 倍，從 119 秒降至 5 秒以內，達到接近光速（Speed-of-Light）效能。

## 結論
Dynamo Snapshot 透過檢查點/恢復機制與多項優化技術，大幅改善 Kubernetes 上推理工作負載的彈性擴展能力，目前實驗版支援單 GPU vLLM 與 SGLang，未來將擴展至 TensorRT-LLM、多 GPU 與多節點場景。
