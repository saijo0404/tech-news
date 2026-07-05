# CCCL Runtime: A Modern C++ Runtime for CUDA

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://developer.nvidia.com/blog/cccl-runtime-a-modern-c-runtime-for-cuda/

## 核心主題
NVIDIA 於 CUDA 13.2 推出 CCCL Runtime——一組基於現代 C++ 的 CUDA 基礎 API 抽象層，以強型別、顯式依賴、預設非同步等設計原則，取代傳統 CUDA Runtime API 的隱式狀態與 C 語言相容限制，讓 CUDA 開發更安全、更現代化。

## 關鍵重點
- **強型別與顯式依賴**：以 `cuda::device_ref`、`cuda::stream` 等專屬型別取代原始整數與不透明指標，Stream 建立需明確傳入 device 引數，不再依賴全域「當前 device」狀態，使程式碼可當地推理、多函式庫更容易組合；沿用 `std::string` / `std::string_view` 模式，為多數物件提供擁有型別與參考型別兩型，方便與既有 API 互動。
- **預設非同步與 Stream-ordered 記憶體管理**：首參為 stream 的 API 一律依 stream 順序操作，不提供同步版本；記憶體配置以 memory pool 與 stream-ordered 分配為預設，`cuda::make_buffer` 自動提交配置、初始化、釋放至 stream，未初始化需明確以 `cuda::no_init` 選擇退出，避免隱含 bug。
- **編譯時期配置流動與 Kernel Functors**：block size 等配置資訊以模板引數編碼至型別中，經 `cuda::launch` 自動傳入 kernel，裝置端可於編譯時期取得靜態資訊（如以 `static_assert` 驗證維度）；Kernel Functors（具 `__device__ operator()` 的 struct）取代傳統 `__global__` 函式，模板引數由 `cuda::launch` 自動推導，無需明確範例化。
- **自動參數轉換**：`cuda::buffer` 傳入 kernel 時自動轉換為 `cuda::std::span`，無需手動提取指標，kernel 簽章可直接反映裝置端資料的使用方式。

## 結論
CCCL Runtime 融合強型別、顯式依賴、預設非同步、編譯時期型別流動與自動參數轉換等設計，讓現代 CUDA C++ 程式碼更清晰、更安全、更易於組合；同時提供相容協助函式，讓開發者可增量採用，無需重寫整個程式碼庫。

---
