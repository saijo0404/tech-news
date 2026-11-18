# Integrating QPUs into Supercomputing Centers Using Slurm HRES Plugins

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-17
- **原文連結**: https://developer.nvidia.com/blog/integrating-qpus-supercomputing-centers-using-slurm-hres-plugins/

## 核心主題
Slurm 26.11 引入 HRES (Hybrid Resource) 插件，首次允許將量子處理器 (QPU) 作為原生集群級資源進行排程，解決現有 GRES 模型將設備綁定至單一節點的限制。

## 關鍵重點
- **架構創新**：使用短 Lua 腳本實現，資源配置與設備邏輯分離，提升可移植性且獨立於 Slurm 版本週期
- **設備管理**：提供每 30 秒的設備健康檢查與任務准入控制，避免節點閒置
- **開源方案**：QRMI 和 QDMI 兩個開源插件支援多個量子電腦供應商，用戶腳本無需修改
- **應用場景**：適用於化學模擬、天氣模擬、工程模擬等領域的量子加速應用

## 結論
HRES 插件為量子電腦原生整合到排程器提供了開源解決方案，通過 Lua 插件設計實現通用性與可重複使用性，大幅提升量子加速應用在超級計算中心的部署效率。
---