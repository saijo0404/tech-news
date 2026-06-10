# 使用 NVIDIA DOCA 晶片內安全加速 AI 工廠的代理式 AI 基礎設施

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-31
- **原文連結**: https://developer.nvidia.com/blog/advancing-ai-infrastructure-for-agentic-ai-with-nvidia-doca-in-silicon-security/

## 核心主題
NVIDIA 透過 BlueField DPUs 與 DOCA 安全堆疊，將安全保護從軟體層下沉至晶片內執行，為代理式 AI 工廠提供分散式、全堆疊且加速化的安全基礎設施，確保 AI 基礎架構、工作負載、代理與資料在規模化運算下仍受保護。

## 關鍵重點
- **晶片內安全改變傳統安全架構**：BlueField DPU 建立硬體強制執行的安全層，獨立於宿主系統運作，即使宿主被攻陷仍能持續監控與執行策略，不消耗宿主運算資源，讓攻擊者無法篡改或繞過安全防護。
- **DOCA 三大核心安全能力**：DOCA Argus 提供 runtime 威脅偵測，透過零拷貝記憶體存取即時監控程式行為與完整性，偵測速度比純軟體方法快 1,000 倍；DOCA Vault 在儲存存取請求透過前執行零信任授權策略，防止未經授權的資料外洩；DOCA Flow 在晶片內執行 L4/L7 防火牆與封包檢查，支援 800 Gb/s 高速策略執行。
- **與現有安全生態系整合**：Argus 可透過 Fluent Bit 與 Vector 串流 telemetry 至 SIEM、SOAR、XDR 等平台，安全團隊無需大幅修改架構即可將既有分析與威脅intelligence延伸至 AI 環境，同時保護 PII 隱私。

## 結論
DOCA 安全堆疊將 runtime 可見性、零信任資料保護與加速網路執行整合於統一架構，為代理式 AI 提供安全由設計（security-by-design）的基礎設施，在不犧牲效能與擴展性的前提下，保護整個 AI 工廠從訓練、推論到代理執行的完整生命週期。
