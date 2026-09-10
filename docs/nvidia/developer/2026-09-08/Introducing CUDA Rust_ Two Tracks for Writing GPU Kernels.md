# Introducing CUDA Rust: Two Tracks for Writing GPU Kernels

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-08
- **原文連結**: https://developer.nvidia.com/blog/introducing-cuda-rust-two-tracks-for-writing-gpu-kernels/

## 核心主題
NVIDIA 正式推出 CUDA Rust 兩個開發軌道（SIMT 與 Tile），讓開發者能用 Rust 原生編寫 GPU 核函數，解決以往 GPU 核函數必須用其他語言撰寫的痛點。

## 關鍵重點
- **cuda-oxide**：SIMT 軌道，透過自訂 rustc codegen backend 將 Rust 核函數編譯為 PTX，需 nightly Rust 與 LLVM，使用 DisjointSlice 與 launch contract 確保記憶體安全。
- **cutile-rs**：Tile 軌道，在穩定版 Rust 1.89+ 上運行，透過 CUDA Tile IR JIT 編譯，使用 Tensor 分區與 ownership 機制保證記憶體安全，已應用於 HuggingFace Grout 與 mistral.rs。
- 兩者皆提供 compile-time 記憶體安全，避免 race condition 與 aliasing 問題。
- NVIDIA 計劃支援跨語言互操作性，開發者可根據現有 stack 選擇合適的 CUDA 前端，不會被鎖定在單一生態系統。

## 結論
CUDA Rust 填補了 GPU 核函數編譯的空白，讓 Rust 開發者能直接編寫高性能 GPU 程式。Tile 軌道因使用穩定版 Rust 更適合多數開發者，而 SIMT 軌道則提供更細緻的控制權。NVIDIA 承諾持續發展 CUDA Rust 至 2027 年及以後。
---
