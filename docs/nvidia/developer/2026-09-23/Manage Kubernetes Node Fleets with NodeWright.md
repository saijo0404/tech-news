# Manage Kubernetes Node Fleets with NodeWright

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-23
- **原文連結**: https://developer.nvidia.com/blog/manage-kubernetes-node-fleets-with-nodewright/

## 核心主題
NodeWright 是一個開源、Kubernetes 原生的套件管理工具，可宣告式地配置和更新 GPU 集群中的主機作業系統，同時不中斷工作負載。

## 關鍵重點
- NodeWright 操作員會執行六個步驟：鎖定節點、等待關鍵容器、排空、應用套件、必要時中斷、然後解除鎖定，並尊重 PodDisruptionBudgets 和非中斷工作負載標籤。
- DeploymentPolicy 資源允許使用固定、線性或指數批次策略，在集群隔間中進行逐步滾動，並可配置成功和失敗閾值。
- 套件可處理主機級操作，如内核參數調優、CVE 修復、安全代理安裝和崩潰轉錄配置，並具有內建驗證檢查，通過 Kubernetes 顯示失敗。
- NodeWright 與 NVIDIA AI Cluster Runtime 集成，應用版本鎖定食譜的主機級部分，並與 NVCRE 和 NVSentinel 一起用於工作負載預驗證和運行時故障監控。

## 結論
NodeWright 通過 Kubernetes 原生方式解決 GPU 集群節點管理挑戰，使團隊能夠安全地更新和配置節點，而不影響正在運行的訓練工作負載。
---
