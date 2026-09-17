# Translating CUDA Tile Operations from Python to Rust Using Agentic AI

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-16
- **原文連結**: https://developer.nvidia.com/blog/translating-cuda-tile-operations-from-python-to-rust-using-agentic-ai/

## 核心主題
這篇文章介紹了使用 AI 代理自動將 cuTile Python GPU 核碼翻譯到 cuTile Rust 的自動化技能系統，成功移植 24 個公共操作員並保持高性能。

## 關鍵重點
- 成功移植 24 個公共操作員，性能平均達到 cuTile Python 99.5%，幾何平均值達 0.995
- 採用有界多代理工作流，每個階段包含可機器檢查的判決，包括 IR 比對以驗證結構等效性
- 解決了 cuTile Python 隱式特化與 cuTile Rust 明確特化的轉換挑戰，需將 Python 的隱式特化轉化為 Rust 的明確類型和形狀約束
- 基於 49 條編碼規則的驗證驅動流程，錯誤歸責明確，避免浪費重試
- 轉換後的核通過 C-ABI 層與 TileGym 整合，傳遞張量描述符而不複製或分配，支援延遲編譯
- 翻譯技能在 TileGym 倉庫中提供，可應用到自定義核，編輯後自動重新編譯

## 結論
此自動化翻譯系統為 GPU 核碼跨語言移植提供了可靠、可驗證的解決方案，特別適合需要高性能和明確錯誤診斷的場景。

---