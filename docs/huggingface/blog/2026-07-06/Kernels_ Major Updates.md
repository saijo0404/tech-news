# Kernels: Major Updates

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-06
- **原文連結**: https://huggingface.co/blog/revamped-kernels

## 核心主題
Hugging Face Kernels 專案進行了全面重構，推出了新的儲存庫類型、大幅強化安全性措施，並重新設計了 CLI 工具，以提供更安全、易用且與 Hugging Face Hub 更整合的客製化核核解決方案。

## 關鍵重點
- **新的儲存庫類型**：推出了「kernel」儲存庫類型，使 Kernels 成為 Hugging Face Hub 的一等公民，使用者可瀏覽所有可用核核並追蹤趨勢。
- **強化安全性**：引入可信發布者機制、程式碼簽名（使用 Sigstore cosign）和來源驗證，防止惡意核核被執行。
- **重新設計的 CLI**：將 kernels 和 kernel-builder 分開，使 kernels 專注於載入和準備核核，kernel-builder 專注於構建，提供更清晰的開發體驗。
- **擴展框架支援**：新增 PyTorch Stable ABI 和 Apache TVM FFI 支援，使核核可跨框架運行，提升靈活性。
- **代理式核核開發基礎**：支援自動化工具和性能評估，讓代理能自動構建、測試和優化核核。
- **系統卡片**：每個核核都有系統卡片，提供使用說明和介面資訊，幫助使用者確認系統相容性。

## 結論
Hugging Face Kernels 的重大更新大幅提升了專案的安全性、易用性和可擴展性，為開發者和使用者提供了更完善的客製化核核解決方案，並為未來的代理式開發奠定了堅實基礎。

---