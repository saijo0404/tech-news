# Q&A: How Capcom Brought Path Tracing to RE ENGINE Across PRAGMATA and Resident Evil Requiem

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-16
- **原文連結**: https://developer.nvidia.com/blog/qa-how-capcom-brought-path-tracing-to-re-engine-across-pragmata-and-resident-evil-requiem/

## 核心主題
Capcom 的 RE ENGINE 團隊在《Resident Evil Requiem》和《PRAGMATA》中成功實現了遊戲優化路徑追蹤器，大幅提升了光影一致性和視覺真實感。

## 關鍵重點
- 使用 NVIDIA RTX Kit 和 DLSS Ray Reconstruction 實現高效的路徑追蹤，直接光線追蹤取代陰影圖映射，大幅減少遊戲與電影間的光影差距
- 開發自訂的 ScreenSpaceAlphaTest 和 ReSTIR GI 技術，解決複雜場景中的透明幾何體和噪點問題，特別適用於室內環境
- 內容製作流程發生根本性變化，需要針對髮絲渲染和反射感知資產建立新的工作流，提升整體品質控制

## 結論
路徑追蹤不僅是視覺升級，更是實時渲染演進的重要轉折點，為遊戲開發帶來了更高品質的光影體驗，使場景更具空間真實感和連貫性。

---