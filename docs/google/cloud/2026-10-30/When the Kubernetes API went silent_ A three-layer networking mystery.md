# When the Kubernetes API went silent: A three-layer networking mystery

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-30
- **原文連結**: https://cloud.google.com/blog/products/networking/the-three-layer-gke-network-mystery/

## 核心主題
Google Cloud 的 GKE 集群在歐洲西部區域發生嚴重網路故障，導致 800 名開發者無法部署。問題源於三個不同層面的錯誤共同作用，包括 Private Service Connect 資料包重排序、USPS 丟棄 Challenge ACK 以及 KCP VM 連接狀態異常。

## 關鍵重點
- **Bug #1：PIGv 資料包重排序**：Private Service Connect 的 miss-thread 處理導致資料包重排序，FIN/RST 包與 ACK 包順序混亂。
- **Bug #2：USPS 丟棄 Challenge ACK**：2026 年 2 月 USPS 更新後，錯誤地丟棄了 Challenge ACK 包，本應用於驗證舊連接狀態。
- **Bug #3：KCP VM 連接狀態異常**：KCP VM 在 FIN_WAIT_2 狀態停留超過 2 分鐘，導致端口被重複使用，觸發 Challenge ACK 機制。
- **解決方案**：短期回滾 USPS 變更，長期推出 Linux 核心补丁解決連接狀態管理問題。
- **跨團隊協同**：需要 GKE、Private Service Connect、網路、hostnet、Linux 核心團隊共同協同診斷與修復。

## 結論
此案例證明複雜系統故障往往來自多層面的協同錯誤，單一層面問題通常易於解決，但當網路層、代理層與作業系統層同時存在問題時，需要跨團隊協同診斷與修復。同時進行多點封包擷取與實驗室重現是定位問題的關鍵。
---

檔案已成功儲存至指定路徑。