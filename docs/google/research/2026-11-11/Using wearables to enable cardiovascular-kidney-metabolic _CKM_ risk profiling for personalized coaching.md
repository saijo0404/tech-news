# Using wearables to enable cardiovascular-kidney-metabolic (CKM) risk profiling for personalized coaching

- **來源**: Google Research Blog
- **發布日期**: 2026-11-11
- **原文連結**: https://research.google/blog/using-wearables-to-enable-cardiovascular-kidney-metabolic-ckm-risk-profiling-for-personalized-coaching/

## 核心主題
Google Research 開發了一個實驗性機器學習框架，將被動可穿戴設備信號轉換為可修改的「可教練健康年齡」，並使用行動條件世界模型模擬個人化的12週習慣軌跡，擴展至常規血液生物標記以追蹤早期心血管-腎臟-代謝（CKM）健康。

## 關鍵重點
- **可教練健康年齡模型**：完全基於可修改的日常行為和生理學，整合靜息心率、每日步數、睡眠時長和每週活躍區分鐘四個核心信號，由消費級可穿戴設備被動測量。
- **SensorWM世界模型**：基於228萬人週的匿名數據訓練，模擬不同步數、睡眠和有氧習慣下12週的生理變化，表現優於通用時間序列基礎模型。
- **反事實教練計劃**：結合可行性約束優化器和語言模型教練代理，生成臨床驗證的安全且可執行的12週教練計劃，在盲測中獲得了71.4%的教練和99.2%的醫生評分。
- **CKM健康擴展**：結合可穿戴信號和血液生物標記（膽固醇/HDL比率、eGFR、HOMA-IR），可追蹤多器官系統的早期衰減，發現腎臟衰減常獨立於代謝和心血管壓力。

## 結論
這項研究展示了消費級可穿戴設備和機器學習如何幫助個人健康從回顧過去轉向面向未來的規劃。雖然這些模型是實驗性研究原型而非臨床診斷工具，但為未來測試互動「如果」教練如何幫助人們建立持久習慣並改善長期健康奠定了基礎。

---