# Maximizing Apache Spark availability: Mitigating compute stockouts with flexible VMs and other best practices

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-09-22
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/maximize-apache-spark-availability-with-flexible-vms/

## 核心主題
這篇文章介紹了如何利用 Google 的 Managed Service for Apache Spark 中的靈活性虛擬機（flexible VMs）來應對計算資源短缺問題，確保數據處理管道持續運行。

## 關鍵重點
- **靈活性虛擬機**：允許團隊建立可接受的機器類型清單，而非將集群綁定到固定的機器類型，從而提高集群創建成功率
- **多家族混合**：可在單一配置中混合使用不同世代和類型的機器（如 N2、N2D、N4、C4），擴大可用容量池
- **排名策略**：實施有意識的排名策略，在最高優先級（Rank 0）中指定至少兩個機器類型，自動降低短缺風險
- **Hyperdisk Balanced**：採用現代存儲架構可最大化靈活性 VM 的可用性，新機器類型（如 N4、C4）依賴此存儲提供可預測的性能
- **資源配額管理**：不再只需單一機器類型配額，需確保所有定義的機器類型和磁碟（包括 Hyperdisk）都有足夠配額
- **靈活性承諾使用折扣**：採用 Compute 靈活性承諾使用折扣（CUDs）可跨多個 VM 家族和區域應用節省
- **其他建議**：實施 AutoZone 路由、使用較小機器形狀、部署自動縮放、部分集群創建和建立區域回撥

## 結論
通過採用優先回撥策略和靈活性 VM，可以保護工作負載免受區域硬件短缺的影響，並保持關鍵數據處理管道持續運行。建議立即為 Managed Spark 集群配置靈活性 VM 以提升工作負載的韌性。

---