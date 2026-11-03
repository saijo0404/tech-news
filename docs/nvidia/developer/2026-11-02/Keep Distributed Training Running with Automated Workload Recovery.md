# Keep Distributed Training Running with Automated Workload Recovery

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2024-11-02
- **原文連結**: https://developer.nvidia.com/blog/keep-distributed-training-running-with-automated-workload-recovery/

## 核心主題
NVIDIA Recovery 是 NVIDIA DSX OS 套件中的開源工作負載級別服務，透過自動化機制實現集群訓練工作負載的全天候恢復，大幅降低中斷影響。

## 關鍵重點
- **四階段恢復循環**：透過應用日誌、GPU 指標和排程器訊號偵測中斷，執行「偵測異常→歸因失敗→隔離受影響節點→根據策略重啟或停止工作負載」的完整流程
- **生產環境驗證**：在2024年7月至10月監控期間，成功處理近200個工作負載/天，累計約8,550次異常檢測，平均檢測延遲69秒、恢復動作延遲94秒
- **彈性部署方案**：支援 Slurm 排程器，提供 Helm 圖表部署（集群模式或 SSH 模式），可透過配置器快速入門
- **新版本功能擴展**：新增 Slurm 工作恢復、Slurm 工作陣列恢復（hyperparameter sweeps）及原生 Kubernetes 恢復（JobSet、Kubeflow PyTorchJob）
- **實際採用案例**：IBM Research 與 NVIDIA Cloud Partner Verda 已率先部署，驗證其生產環境效能
- **開源授權**：屬於 DSX OS 套件，採用 Apache 2.0 授權，可自由修改與分發

## 結論
NVIDIA Recovery 提供了一套完整且經過生產驗證的自動化工作負載恢復解決方案，透過開源模式降低導入門檻，並持續擴展對不同排程器與工作負載類型的支持，為分布式訓練環境提供高可靠性的基礎設施保障。

---