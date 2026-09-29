# Unlock 3x QPS and microsecond latency with Memorystore for Valkey 9.1

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-26
- **原文連結**: https://cloud.google.com/blog/products/databases/memorystore-for-valkey-9-1-3x-qps-caching/

## 核心主題
Google Cloud 正式推出 Memorystore for Valkey 9.1，相比 Memorystore for Redis Cluster 實現最高 3 倍 QPS（每秒查詢數）並達到微秒級延遲，為處理百萬級並發用戶的 AI 和微服務架構提供強大性能支援。

## 關鍵重點
- **底層架構重構**：採用無鎖多隊列通訊架構，取代靜態分發機制，透過動態工作平衡消除跨線程 CPU 浪費，並引入 CPU 驅動啟動與隊列深度自動擴展引擎。
- **新開發者功能**：
  - 細粒度資料庫級別存取控制 (ACLs)：支援多資料庫隔離與集中管理
  - CLUSTERSCAN 命令：支援集群感知游標，實現高效全域鍵掃描
  - HGETDEL、MSETEX 等原子性命令：提升資料一致性與過期管理效率
- **六種新節點尺寸**：新增 Custom-Pico/Micro/Mini 小型節點與 HighCPU-Medium/Standard-Large/Highmem-XXLarge 大型節點，滿足不同規模工作負載需求。
- **簡化遷移工作流**：提供四步驟線上遷移方案，支援從自管理 Redis/Valkey 平滑遷移至完全托管的 Memorystore for Valkey。

## 結論
Memorystore for Valkey 9.1 透過底層性能優化與新功能擴展，為需要極致延遲與高併發能力的組織（如 MLB、Target 等）提供強大支援，同時降低自管理成本並提升安全性。
---
