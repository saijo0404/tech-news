# Introducing Google Cloud’s U4 compute: Enabling ultra-low latency trading

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-08
- **原文連結**: https://cloud.google.com/blog/topics/financial-services/ultra-low-latency-solution-with-u4-enables-high-velocity-trading/

## 核心主題
Google Cloud 推出 U4 計算機系列和超低延遲解決方案，使金融市場參與者能夠在雲端實現微秒級交易速度和確定性。

## 關鍵重點
- **U4 機器系列**：提供三種專用機器系列——U4P 和 U4C 裸金屬實例（供交易所運營商和市場參與者使用）以及 U4S 高性能 VM，均具備超低延遲和可預測性能
- **硬體級網絡功能**：包括可擴展的硬體多播數據分發、硬體級網絡可觀測性（支持市場重播和絕對交易驗證）以及確定性高性能計算
- **高性能存儲與隔離**：本地 Titanium SSD 用於實時交易日誌，Hyperdisk 用於歷史數據存儲；通過獨立 Titanium 適配器實現物理流量隔離
- **加速數據包處理**：支持 OpenOnload 和 DPDK，實現可預測的單播和多播數據包處理，最小化應用代碼變更
- **精確時間同步**：集成 Google Cloud Firefly 時間同步系統，實現小於 10 納秒的網絡級時間戳，優於金融交易所小於 100 微秒的監管要求
- **24/7 市場準備**：生產工作負載隔離在專用主區域，例行雲維護和資格測試在次級區域進行

## 結論
Google Cloud 的超低延遲解決方案使金融市場參與者能夠在雲端以傳統共置的速度執行交易，同時享有雲的靈活性。該解決方案已與 CME Group 等機構合作，成功將核心交易系統遷移至雲端，驗證了雲端計算在金融市場中的可行性。

---