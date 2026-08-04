# NVIDIA Vera Storage Benchmarks: Faster Encryption, Compression, Integrity Checking, and Recovery for AI-Native Storage

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-03
- **原文連結**: https://developer.nvidia.com/blog/nvidia-vera-storage-benchmarks-faster-encryption-compression-integrity-checking-and-recovery-for-ai-native-storage/

## 核心主題
NVIDIA Vera BlueField-4 STX Storage Processor 在加密、壓縮、完整性檢查和數據恢復等存儲處理任務上，相比 x86 CPU 展現出顯著的性能優勢，為 AI 原生數據平台提供更高效的存儲解決方案。

## 關鍵重點
- **加密/解密加速**：Vera 在 AES-128 加密上比 x86 CPU 快 1.43 倍，解密快 1.29 倍，使存儲系統能處理更多安全數據而不受寫入限制。
- **數據恢復加速**：Reed-Solomon 編碼在恢復工作負載上快 3.26 倍，加快數據保護和重建速度，縮短重建時間。
- **完整性檢查加速**：CRC32C 完整性檢查快 3.67 倍，允許存儲系統在更多數據上驗證數據完整性而不受 CPU 限制。
- **壓縮/解壓縮加速**：壓縮快 3.29 倍，解壓縮快 1.72 倍，減少存儲容量需求和帶寬壓力。
- **多階段管道優化**：多階段存儲管道操作快 3.21 倍，提升整體存儲處理吞吐量。

## 結論
NVIDIA Vera CPU 架構通過將高性能存儲處理直接集成到存儲數據路徑中，使 AI 基礎設施能在更低的 CPU、功耗和散熱環境下擴展代理執行和存儲處理能力，支持更高服務密度和更多並行數據流，為 AI 原生存儲平台提供更高效率、更安全的數據保護方案。

---

檔案已成功儲存至指定路徑。