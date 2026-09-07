# How Yahoo Optimizes Apache Spark with Flexible VMs

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-09-05
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/how-yahoo-optimizes-apache-spark-with-flexible-vms/

## 核心主題
Yahoo 透過在 Google Cloud Managed Service for Apache Spark 中實施靈活性 VM 配置，成功將集群配置失敗率降低 85%，確保數據管道在區域容量波動時仍能自動運行。

## 關鍵重點
- Yahoo 透過定義可接受的 VM 形狀排名列表，讓系統自動搜索區域並維持數據管道執行，無需手動干預
- 啟用 Auto-Zone 配置後，Managed Spark 可在整個區域內搜索可用容量，提高集群創建成功率
- 靈活性 VM 配置要求保持核心數和記憶體對稱性，並統一 CPU 與記憶體比例以確保容器大小一致

## 結論
靈活性 VM 配置將 Yahoo 的數據基礎設施轉化為動態資源池，使其能夠自動適應運營需求，無論供應波動如何都能可靠地獲取計算資源，同時支持硬體現代化。

---