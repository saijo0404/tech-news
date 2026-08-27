# CUDA Python 1.0: Stable APIs, One Foundation, Full Platform Access

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-25
- **原文連結**: https://developer.nvidia.com/blog/cuda-python-1-0-stable-apis-one-foundation-full-platform-access/

## 核心主題
NVIDIA 正式推出 CUDA Python 1.0，將 Python 提升為使用 CUDA 平台的一等公民，提供穩定 API 承諾與單一基礎架構，讓開發者能透過 Python 完整訪問 CUDA 平台功能。

## 關鍵重點
- **cuda.core 1.0.0**：提供 Python 語法介面，將 CUDA 基礎設施（裝置、串流、記憶體）轉化為標準 Python 物件，成為所有 GPU 庫的共同基礎
- **cuda.compute 1.0.0**：將 CCCL 平行演算法（排序、掃描、歸約等）以 Python 函式形式提供，支援 Python lambda 自訂
- **Numba 與 Numba CUDA MLIR**：允許開發者用 Python 撰寫 SIMT 核函式，MLIR 後端提供更快編譯與更低延遲
- **cuda.bindings 13.3.0**：提供對 CUDA C API 完整 1:1 覆蓋，供建立 GPU 庫的開發者使用
- **生態系整合**：CuPy、PyTorch 等主流 GPU 庫現在都建立在共享的 cuda.core 基礎之上，減少版本衝突與互操作性問題

## 結論
CUDA Python 1.0 解決了過去 Python GPU 開發者面臨的碎片化問題，透過單一官方維護的基礎架構，讓不同庫之間能共享資源、協同工作，大幅降低開發門檻並提升生態系穩定性。

---

檔案已成功儲存至指定路徑。