# Start and Restore GPU Workloads in Seconds with NVIDIA Snapshot

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://developer.nvidia.com/blog/start-and-restore-gpu-workloads-in-seconds-with-nvidia-snapshot/

## 核心主題
NVIDIA Snapshot 是一個開源檢查點與恢復系統，可將 GPU 推理工作載體從冷啟動的數分鐘縮短至數秒。

## 關鍵重點
- 恢復時間為 3.6 至 42.7 秒，比冷啟動快 8 至 36 倍，大幅縮短推理副本上線時間
- 支援多 GPU 工作負載，包括張量平行化、資料與專家平行化，可處理達 1 TB 檢查點的混合專家模型
- 檢查點建立時間為 15 秒至 5.5 分鐘，視模型大小而定，且檢查點加恢復總時間短於單一冷啟動
- 測試環境使用 NVIDIA B200 GPU 與 VAST NFS 儲存，GPU 狀態恢復佔比大於 CPU 過程恢復

## 結論
NVIDIA Snapshot 為 AI 工廠操作提供了快速啟動與恢復 GPU 工作負載的解決方案，特別適合處理推理需求尖峰或副本失敗的情況，可顯著提升系統彈性與服務可用性。

---