# Control How Your GPU Shares Work with Green Contexts

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-06
- **原文連結**: https://developer.nvidia.com/blog/control-how-your-gpu-shares-work-with-green-contexts/

## 核心主題
NVIDIA 推出 Green Contexts 功能，允許應用程式明確分區 GPU 執行資源（如 SM 和 Workqueue），使延遲敏感型工作負載能在不等待大規模工作負載排空的情況下運行，大幅降低關鍵核延遲。

## 關鍵重點
- **SM 分區**：應用程式可指定特定 SM 子集給特定工作負載，使多個工作負載能在 GPU 上並行運行而不競爭計算單元。
- **Workqueue 分區**：透過明確分區工作隊列資源，減少因串列化造成的假依賴，提高並行度。
- **效能提升**：在 Blackwell GPU 上測試顯示，使用 Green Contexts 將關鍵核延遲從 0.140 ms 降低至 0.007 ms，提升約 20 倍。
- **輕量且可選**：Green Contexts 比傳統 CUDA 上下文更輕量，可逐步導入現有應用程式，不影響現有程式碼。
- **程式模型明確**：應用程式可明確選擇工作執行的綠色上下文，取代依賴隱式線程本地設備狀態的傳統做法。

## 結論
Green Contexts 為需要更精確控制 GPU 資源分發的應用程式提供了新的解決方案，特別適合多工作負載並行運行的場景。雖然需要犧牲部分 SM 給大規模工作負載，但能顯著降低延遲敏感型工作負載的等待時間，是提升 GPU 應用性能的重要工具。

---