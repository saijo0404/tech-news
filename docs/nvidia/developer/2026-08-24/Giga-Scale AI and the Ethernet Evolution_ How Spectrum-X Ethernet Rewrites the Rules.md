# Giga-Scale AI and the Ethernet Evolution: How Spectrum-X Ethernet Rewrites the Rules

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-24
- **原文連結**: https://developer.nvidia.com/blog/giga-scale-ai-ethernet-evolution-spectrum-x-ethernet-rewrites-rules/

## 核心主題
NVIDIA 推出 Spectrum-X Ethernet，以硬體加速技術解決傳統以太網在大型 AI 數據中心中的限制，確保在極端負載和多租戶環境下仍能提供可預測的低延遲和高組網利用率。

## 關鍵重點
- **硬體加速控制迴路**：Spectrum-X Ethernet 採用三個互不干擾的硬體加速控制迴路（適配路由、目標化擁塞控制、NIC 基平面負載平衡），在微秒級別內即時反應擁塞狀況。
- **多平面拓撲架構**：將單一主機的巨大頻寬分解為多個獨立平面，透過硬體加速平面負載平衡器（PLB）實現動態負載平衡和快速故障轉移，避免傳統無知噴灑方式的瓶頸。
- **多租戶隔離與效能**：在 DeepSeek-V3 訓練模擬中，傳統以太網因背景雜訊導致訓練步驟時間從 735ms 飆升至 1.18 秒（1.6 倍延遲），而 Spectrum-X Ethernet 維持穩定在 668ms，幾乎零退化。

## 結論
Spectrum-X Ethernet 透過硬體加速的多平面網路架構，重新定義了 Gigascale AI 工廠的網路設計標準，大幅降低 Time-to-AI，為未來百萬級 GPU 訓練集群提供可擴展、高可靠性的網路基礎設施藍圖。

---

*本文摘要基於 NVIDIA Technical Blog 於 2026 年 8 月 24 日發表的文章。*
