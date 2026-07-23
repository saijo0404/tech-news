# Make Long-Running NVIDIA TensorRT Engine Builds Observable and Cancelable in Python or C++

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-22
- **原文連結**: https://developer.nvidia.com/blog/make-long-running-nvidia-tensorrt-engine-builds-observable-and-cancelable-in-python-or-c/

## 核心主題
TensorRT 引擎建置過程可能持續數秒至數分鐘，透過 IProgressMonitor API 可實現進度和取消功能，讓開發者能即時掌握建置狀態並及時終止冗長建置。

## 關鍵重點
- **IProgressMonitor API**：TensorRT 提供的抽象基類別，開發者需實作三個方法（phase_start、step_complete、phase_finish）來追蹤建置階段和進度。
- **跨語言一致性**：Python 和 C++ 版本的介面設計相同，僅方法名稱拼寫不同，方便開發者移植。
- **取消機制**：透過 step_complete 方法返回 false 即可請求取消，支援 Ctrl-C 或程式化停止信號。
- **多層級進度顯示**：支援巢狀進度條，可顯示 Building Engine、Tactic Selection 等階層化建置階段。
- **實際整合場景**：可應用於終端機、IDE 擴充套件、FastAPI/HTTP 服務或 AI 代理運行時等各種環境。

## 結論
透過實作 IProgressMonitor，開發者可以將 TensorRT 引擎建置過程轉化為可觀察、可取消的互動體驗，大幅減少無效的 GPU 時間浪費，並提升 AI 代理工作流的穩定性。此解決方案已包含在 NVIDIA 的開源範例中，可立即應用於專案。
---
