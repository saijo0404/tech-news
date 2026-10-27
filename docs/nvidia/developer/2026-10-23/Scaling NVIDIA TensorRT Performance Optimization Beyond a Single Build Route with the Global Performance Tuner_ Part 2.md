# Scaling NVIDIA TensorRT Performance Optimization Beyond a Single Build Route with the Global Performance Tuner, Part 2

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://developer.nvidia.com/blog/scaling-nvidia-tensorrt-performance-optimization-beyond-a-single-build-route-with-the-global-performance-tuner-part-2/

## 核心主題
TensorRT 11.1 推出的 Global Performance Tuner 功能透過可搜尋的編譯器路徑（build routes）實現精度感知的端到端性能優化，在十個工作負載上帶來 1.14x 至 1.63x 的性能提升。

## 關鍵重點
- **可搜尋的編譯器路徑**：TensorRT 提供超過 200 個可調整的編譯器開關（knobs），每個開關都有預設值和允許的值集合，使用者可以透過 C++ API 設定或檢查編譯器路徑。
- **精度感知的優化**：Global Performance Tuner 將精度視為篩選條件，性能作為排名標準，在滿足精度要求的候選路徑中選擇性能最佳的路徑，解決性能與精度的糾纏問題。
- **trtexec 調優工具**：實現自動調優循環，將路徑表達式展開為具體路徑，建立並測量每個候選引擎，排除失敗或精度不達標的路徑，選擇性能最佳的引擎。
- **最佳實踐**：根據搜尋空間選擇搜尋策略（快速搜尋、混合搜尋、完整搜尋）、使用 --dryRun 預覽路徑、使用 --tuningCacheFile 和 --continue 實現增量和可恢復的調優過程。

## 結論
Global Performance Tuner 透過系統化的受限優化過程，將性能與精度的角色明確分離：使用者定義精度邊界，調優工具在該邊界內找出最佳性能路徑。這使性能優化變得可測量、可重複且符合應用需求，而非隨機在速度與精度之間做選擇。

---