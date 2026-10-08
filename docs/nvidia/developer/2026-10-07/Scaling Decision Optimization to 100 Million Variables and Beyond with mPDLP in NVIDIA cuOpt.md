# Scaling Decision Optimization to 100 Million Variables and Beyond with mPDLP in NVIDIA cuOpt

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-07
- **原文連結**: https://developer.nvidia.com/blog/scaling-decision-optimization-to-100-million-variables-and-beyond-with-mpdlp-in-nvidia-cuopt/

## 核心主題
NVIDIA cuOpt 推出多 GPU 原始對偶混合梯度線性規劃求解器 (mPDLP)，將大型 LP 問題分佈至 NVLink 連接的 GPU，顯著提升求解速度並降低記憶體使用。

## 關鍵重點
- **性能提升**：大型問題求解時間顯著縮短，非零項超過 10^7 時速度提升明顯，最大達 11.4 倍
- **記憶體優化**：每 GPU 峰值記憶體使用量降低最多 6 倍，支援 21 億非零項
- **通訊優化**：透過最小割分區化 (min-cut partitioning) 減少跨 GPU 通訊，利用連續 SpMV 間的依賴關係
- **實際應用**：Kinaxis 供應鏈模型 (1.35 億變量) 達 3.3x 速度提升，PSR 能源模型 (1.85 億變量) 達 5x 以上速度提升

## 結論
mPDLP 技術有效解決大型規劃問題在時間與記憶體限制下的瓶頸問題，並提供 cuOpt 教程與 MPS 檔案範例供開發者使用。

---