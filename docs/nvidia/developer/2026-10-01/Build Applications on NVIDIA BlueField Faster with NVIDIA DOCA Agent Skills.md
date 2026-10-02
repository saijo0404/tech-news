# Build Applications on NVIDIA BlueField Faster with NVIDIA DOCA Agent Skills

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-01
- **原文連結**: https://developer.nvidia.com/blog/build-applications-on-nvidia-bluefield-faster-with-nvidia-doca-agent-skills/

## 核心主題
NVIDIA DOCA AI 代理技能為 AI 代理提供驗證的 API 簽名、硬體能力要求和構建約束，使其能夠像有經驗的 DOCA 開發者一樣推理，大幅減少開發錯誤循環並提高代碼穩定性。

## 關鍵重點
- **效能提升顯著**：在 65 個提示的評估中，沒有技能的代理僅滿足 19% 的檢查表項目，而有技能的代理在所有提示中滿足 100%。
- **涵蓋完整 DOCA 庫**：技能涵蓋 Flow、GPUNetIO、PCC 和 RDMA 等完整功能，使代理能在編寫代碼前驗證設備支持並應用固件級別更改前的檢查。
- **開發效率大幅提升**：並行演示顯示，有技能的代理在構建 Go 基於的 RDMA 應用時，使用的代碼少 73%（189 行 vs 695 行），硬體命令少 46%（20 vs 37）。

## 結論
DOCA AI 代理技能通過提供驗證的 API 簽名、硬體能力要求和構建約束，解決了一般目的 AI 代理在 NVIDIA DOCA 開發上的不足，使開發者能夠更快地構建應用並部署更穩定的代碼。

---