# Bringing gVisor sandboxes to distributed Ray clusters

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-26
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/gvisor-sandboxes-for-ray-clusters-on-gke/

## 核心主題
Google 與 Anyscale 合作推出實驗性 Ray 庫，將原生高績效沙盒直接帶入分布式 Ray 集群，以解決強化學習工作負載的安全隔離問題。

## 關鍵重點
- Ray Sandboxing 將沙盒作為 Ray 原語，使用 Ray Actor 管理沙盒生命周期，與現有 Ray 編程模型自然整合
- 使用 gVisor 作為沙盒運行時，提供比普通容器更强的隔離性，且無需暴露 Docker 代碼或主機 Docker socket
- 沙盒 API 涵蓋基本生命週期：從 OCI 容器映像創建環境、設定資源限制、執行命令、讀寫上傳下載文件、檢查狀態、終止環境
- gVisor 提供次秒級沙盒啟動速度和低記憶體佔用，使沙盒可作為細粒度分布式資源使用

## 結論
這項技術為強化學習和代理工作負載提供了更安全的執行環境，特別適合處理模型生成的代碼，未來 Ray 將擴展支持其他沙盒運行時如 Agent Substrate 或 Kata Containers。
---