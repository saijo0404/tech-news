# How NVIDIA Mission Control 2_5 Brings Autonomous Recovery to Kubernetes

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-26
- **原文連結**: https://developer.nvidia.com/blog/how-nvidia-mission-control-2-5-brings-autonomous-recovery-to-kubernetes/

## 核心主題
NVIDIA Mission Control 2.5 將自主恢復引擎擴展到 Kubernetes 工作負載，實現 AI 工廠的自癒合系統，使故障檢測、診斷與恢復自動化。

## 關鍵重點
- **三層控制迴路架構**：Kubernetes 排程器負責工作負載分發，自主工作恢復服務根據工作上下文分類故障類型，自主硬體恢復服務隔離並診斷有問題的基礎設施。
- **硬體故障處理**：當發生硬體故障時，工作恢復服務立即重啟或重新排程工作，同時硬體恢復服務隔離問題節點並進行診斷，減少工作負載中斷時間。
- **軟體錯誤處理**：對於暫時性軟體錯誤，系統會根據工作歷史記錄重試工作，避免不必要的硬體修復，降低操作噪音。
- **硬體退化早期檢測**：自主硬體恢復服務可提前檢測到節點退化跡象（如 GPU 健康警告、連接問題），主動將有風險節點從排程池中移除，預防故障發生。

## 結論
Mission Control 2.5 的擴展使 AI 工廠從被動維護轉向主動自癒合，無論使用 Kubernetes 還是 Slurm，都能獲得一致的恢復模型，提升加速器容量利用率並減少故障時間。
---