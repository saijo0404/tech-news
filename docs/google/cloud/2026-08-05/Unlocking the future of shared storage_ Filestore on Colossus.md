# Unlocking the future of shared storage: Filestore on Colossus

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-06
- **原文連結**: https://cloud.google.com/blog/products/storage-data-transfer/filestore-file-service-runs-on-colossus/

## 核心主題
Google Cloud 的 Filestore 服務現在基於 Colossus 基礎架構，提供更高的靈活性和可擴展性，以支援 AI 和代理工作負載。

## 關鍵重點
- Filestore 現在使用 Google 的 Colossus 基礎分佈式儲存系統，與 YouTube、Gmail 和 Gemini 使用相同的基礎設施 DNA
- 可以獨立擴展 IOPS 和儲存容量，支援從小型開發環境到大型數據集的廣泛工作負載
- 支援高併發 AI 代理群組，透過 NFS 檔案鎖定確保資料一致性
- 透過 Filestore CSI 驅動程式和 Filestore multishares 優化 GKE 工作負載
- 提供企業級安全性，整合 Google Cloud IAM、NFS UIDs/GIDs 和 IP ACL

## 結論
這項增強使 Filestore 能夠更好地滿足 AI 時代的工作需求，並為未來的改進奠定基礎，幫助企業以靈活和成本效益的方式最大化業務潛力。
---