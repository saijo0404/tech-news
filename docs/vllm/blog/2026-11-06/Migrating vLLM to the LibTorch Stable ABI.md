# Migrating vLLM to the LibTorch Stable ABI

- **來源**: vLLM Blog
- **發布日期**: 2026-11-06
- **原文連結**: https://vllm.ai/blog/2026-11-06-stable-abi-cuda

## 核心主題
vLLM 團隊成功將項目遷移至 LibTorch Stable ABI，使 vLLM 可以無需重新編譯即可升級 PyTorch，大幅降低維護成本。

## 關鍵重點
- **什麼是 LibTorch Stable ABI**：通過穩定二進位介面（ABI），vLLM 可以獨立於 LibTorch 版本更新而運作，無需重新編譯。
- **遷移步驟**：包括評估現狀、將 AutogradFunctions 和 meta functions 遷移至 Python、建立架構、註冊 op 通過 dispatcher、遷移每個源檔案使用穩定 API、驗證測試。
- **挑戰與解決**：遷移過程中遇到 DeepGEMM 等依賴項目的挑戰，通過轉換註冊機制（從 pybind11 到 TORCH_LIBRARY）解決。
- **驗證方法**：使用 torch-abi-audit 工具確保所有依賴項目的穩定性，確保整個 vLLM 輪子完全符合 LibTorch ABI 穩定標準。

## 結論
vLLM 團隊成功完成整個遷移，使 vLLM 可以與更新的 PyTorch 版本兼容，同時保持性能無明顯退步。這不僅提升了開發者升級 PyTorch 的便利性，也大幅降低了分佈式包商的重新編譯成本。

---