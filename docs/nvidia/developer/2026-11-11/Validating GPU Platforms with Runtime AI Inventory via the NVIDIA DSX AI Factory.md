# Validating GPU Platforms with Runtime AI Inventory via the NVIDIA DSX AI Factory

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-11
- **原文連結**: https://developer.nvidia.com/blog/validating-gpu-platforms-with-runtime-ai-inventory-via-the-nvidia-dsx-ai-factory/

## 核心主題
NVIDIA 將 AI Cluster Runtime (AICR) 與開源專案 k8s-aibom 整合，提供 GPU 平台驗證與 AI 工作負載庫存追蹤功能。

## 關鍵重點
- AICR 新增 k8s-aibom 組件，可追蹤 Kubernetes 上運行的 AI 工作負載，並發出 CycloneDX 1.6 AIBOM 記錄
- 預設兩個食譜 (h100-gke-cos-inference 和 h100-gke-cos-inference-dynamo) 會自動選擇 k8s-aibom，其他 GKE 食譜可透過 --runtime-inventory 旗標自選啟用
- 測試顯示 AICR v1.2.0 搭配 k8s-aibom 1.6.2，API 請求約 4 次/分鐘，CPU 使用率 2.2mC，記憶體 28-34 MiB
- 命名空間自選控制，自動分類工作負載類別和服務運行時（如 vLLM 推理部署）

## 結論
此整合解決了 GPU 平台配置驗證與 AI 工作負載可視化之間的斷層，提供完整的 AI 治理解決方案。AICR 負責驗證 GPU 基礎設施配置，k8s-aibom 則追蹤實際運行的 AI 資產，兩者結合可實現從配置到運行的完整可視化。

---