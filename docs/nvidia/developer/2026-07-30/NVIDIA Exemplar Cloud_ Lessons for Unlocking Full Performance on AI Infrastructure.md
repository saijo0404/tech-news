# NVIDIA Exemplar Cloud: Lessons for Unlocking Full Performance on AI Infrastructure

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-30
- **原文連結**: https://developer.nvidia.com/blog/nvidia-exemplar-cloud-lessons-for-unlocking-full-performance-on-ai-infrastructure/

## 核心主題
即使使用相同的 NVIDIA 硬體（如 H100、GB200 NVL72、GB300 NVL72），訓練吞吐量仍可能因底層配置差異（如 SMMU、CPU 狀態、NUMA、NCCL 設定）而產生 8-12% 的性能差距，並提供具體的診斷與優化方法。

## 關鍵重點
- **SMMU 虛擬化配置問題**：在 NVIDIA Grace CPU 上，缺少 CMDQV/VCMDQ 支援導致 VM 中的訓練性能比裸機慢 12-14%；解決方案是在主機核核中啟用並向客觀暴露 CMDQV/VCMDQ。
- **CPU 功率管理和 NUMA 配置錯誤**：在 H100 集群中，BIOS 將 C-state 限制在 C1 且 hypervisor 線程與訓練過程共享核心，導致性能損失 12%；解決方案是調整 C-state 至 C6 並使用 cpuset 隔離 hypervisor 線程。
- **NCCL 隊列對並發數不足**：在 GB300 NVL72 上使用 ConnectX-8 SuperNIC 時，默認 NCCL_IB_QPS_PER_CONNECTION=1 導致 31% 的性能差距；解決方案是將其提升至 4。
- **NCCL 拓扑文件未傳播到容器**：在虛擬化 B200 環境中，NCCL_TOPO_FILE 和 /etc/nccl/topo.xml 未挂载到 enroot 容器，導致 AllGather/ReduceScatter 變慢 2-4 倍；解決方案是使用 --mount 類型將拓扑文件掛載到容器內。

## 結論
基礎設施工程師應系統性地驗證 SMMU、CPU 功率管理、NUMA/過程綁定、NCCL 隊列對並發數，並確保所有拓扑/環境變量可訪問於容器化訓練環境中，以縮小性能差距並通過 NVIDIA Exemplar Cloud 驗證（95% 門檻）。

---

本文透過四個真實案例研究，說明即使使用相同的 NVIDIA 硬體，訓練吞吐量仍可能因底層配置差異而產生顯著性能差距。文章提供了具體的診斷工具（如 perf、Nsight Systems、nccl-tests）和優化方法，幫助工程師識別並解決 SMMU、CPU 狀態、NUMA 綁定、NCCL 設定等常見問題。關鍵在於系統性地驗證每個層級的配置，並確保所有環境變量和拓扑文件都能正確傳播到訓練容器內。