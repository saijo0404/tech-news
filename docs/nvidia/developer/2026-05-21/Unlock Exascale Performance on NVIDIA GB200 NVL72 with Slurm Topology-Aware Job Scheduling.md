# Unlock Exascale Performance on NVIDIA GB200 NVL72 with Slurm Topology-Aware Job Scheduling

- **來源**: developer  
- **發布日期**: 2026-05-21  
- **原文連結**: https://developer.nvidia.com/blog/unlock-exascale-performance-on-nvidia-gb200-nvl72-with-slurm-topology-aware-job-scheduling/  

## 核心主題  
NVIDIA GB200 NVL72透過Slurm拓撲感知排程技術，優化GPU資源配置以提升AI與HPC工作負載效能。  

## 關鍵重點  
- GB200 NVL72具備72個Blackwell GPU與130TB/s NVLink帶寬，支援即時 trillion-parameter 模型運算。  
- Slurm新拓撲(Block)插件可對齊工作排程與NVLink領域邊界，減少碎片化並提升GPU使用率。  
- 推薦根據工作負載大小調整段大小（如64 GPU以上使用16節點段，小規模使用2-8節點段）。  

## 結論  
透過拓撲感知排程與動態段大小調整，可最大化GB200 NVL72集羣效能，確保高利用率與穩定性能。  
---