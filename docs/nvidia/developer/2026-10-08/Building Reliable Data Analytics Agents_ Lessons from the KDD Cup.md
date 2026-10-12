# Building Reliable Data Analytics Agents: Lessons from the KDD Cup

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-08
- **原文連結**: https://developer.nvidia.com/blog/building-reliable-data-analytics-agents-lessons-from-the-kdd-cup/

## 核心主題
NVIDIA KGMON 團隊透過設計受限的約束環境，在 KDD Cup 2026 數據代理競賽中獲得第二名。文章分享了如何為小型固定 LLM 建立可靠數據分析代理的實戰經驗。

## 關鍵重點
- **統一數據訪問介面**：將 CSV、JSON 等結構化數據源統一轉換為 SQLite 數據庫，提供單一 schema() 和 sql() 接口，減少路由錯誤並保留推理能力。
- **前置模式探測**：在主要推理循環前進行 schema-scouting，提前告知代理可用的表、連接鍵和數據質量問題，減少因欄位錯誤或遺漏連接導致的錯誤。
- **小型有見解的工具集**：限制代理使用小型工具集（schema()、sql(query)、write_answer(df)、prose_helper()），配合中間件修復錯誤呼叫和持久化狀態，減少 boilerplate 錯誤。
- **文檔處理策略**：將文檔檢查與結構化分析分開，使用 prose_helper 工具針對性提取規則或表格，避免將原始文檔內容載入主代理上下文。
- **執行跡象記錄**：記錄所有提示、工具呼叫和中間結果，使專責檢查代理能分類失敗並指導改進。
- **多嘗試評估**：通過多次嘗試提高覆蓋率和可靠性，但需謹慎評估成本。
- **改進循環管理**：要求保留任務、提示審計和跡象審查，在推廣改進前加入人工審查閘門。
- **人類參與時機**：人類應定義成功標準、審計跡象並指導早期代理行為，而非監控每個工具呼叫。

## 結論
可靠性往往來自於為模型建立正確的約束環境，而非使其更開放。透過統一數據訪問、限制工具集、記錄跡象和謹慎評估，可以為小型 LLM 建立更可靠的數據分析代理系統。

---