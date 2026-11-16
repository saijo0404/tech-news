# Faster Scientific Simulations with New FP64 Algorithms in NVIDIA cuBLAS

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-13
- **原文連結**: https://developer.nvidia.com/blog/faster-scientific-simulations-with-new-fp64-algorithms-in-nvidia-cublas/

## 核心主題
NVIDIA cuBLAS 在 CUDA Toolkit 13.4.2 中引入 Ozaki-II 和 2M 演算法，透過整數 Tensor Core 加速雙精度矩陣乘法（DGEMM/ZGEMM），同時保持完整的 FP64 精度，大幅提升科學模擬效率。

## 關鍵重點
- **Ozaki-II 演算法**：使用中國剩餘定理（CRT）減少整數乘法次數，比 Ozaki-I 效率提升約 2 倍，DGEMM 在 NVIDIA VR NVL72 上達 5.5 倍加速。
- **2M 複雜矩陣乘法演算法**：將傳統 4M 方法（4 次實數乘法）優化為 2M 方法（僅 2 次實數乘法），ZGEMM 在 NVIDIA GB200 上達 5 倍加速。
- **實際應用驗證**：CCSD 量子化學計算（全精度 2-1.4 倍加速，混合精度 5-3.5 倍加速）和 BerkeleyGW 材料模擬（6.6-3.9 倍加速）均驗證精度與速度兼得。
- **NVIDIA Rubin GPU 支援**：引入 TI16 數值格式與 tcgen05.mma 指令，進一步加速 Ozaki-I/Ozaki-II 計算。

## 結論
透過 cuBLAS 的自動動態精度（ADP）框架，應用程式無需修改程式碼即可自動獲得加速，且精度保證不低於原生 FP64。這解決了以往在精度與速度間的取捨問題，為科學模擬帶來顯著性能提升。

---

最後，完整的摘要已成功儲存至指定檔案路徑。
