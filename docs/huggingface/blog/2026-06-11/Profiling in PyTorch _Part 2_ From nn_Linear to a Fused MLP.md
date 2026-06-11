---
# Profiling in PyTorch (Part 2): From nn.Linear to a Fused MLP

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-11
- **原文連結**: https://huggingface.co/blog/torch-mlp-fusion

## 核心主題
這是 PyTorch 效能分析系列的第二篇，作者從手寫 matmul-add 邁向 nn.Linear，再堆疊成 GeGLU MLP，並對比 eager 模式、torch.compile 與自訂 Triton 核函式的追蹤結果，揭示 PyTorch 如何透過 epilogue、fuse 與 hand-tuned 核函式減少 HBM 記憶體頻寬瓶頸。

## 關鍵重點
- **nn.Linear 的隱藏優化**：nn.Linear 的 bias 加法已透過 GEMM epilogue 融入 cuBLAS addmm 核函式，不需單獨的 add kernel；torch.compile 在此情境下幾乎無法再 fusion，因為單一 linear 已是最小單位。compile 的實際貢獻在於消除 CPU 端 view 轉派（如 aten::t 的 metadata 重寫），而非改變 GPU 運算。
- **MLP 的 eager vs compiled 追蹤**：在 eager 模式下，GeGLU MLP 會產生 5 個 GPU kernel（3 個 GEMM + GeLU + mul），其中 GeLU 與 mul 的 50 MB 中間結果需完整寫回並讀取 HBM；啟用 torch.compile 後，這兩個點核函式與 reshape 被融合為單一 Triton kernel，中間結果保留在暫存器中，省下一次完整的 HBM 往返。
- **手寫 tuned kernel 的 trade-off**：LigerGEGLUMLP 將融合邏輯直接寫入 Triton kernel，無需 Dynamo guards 或編譯開銷，且 launch 參數針對硬體最佳化；雖然比 Inductor 針對特定 shape 生成的 kernel 略慢數微秒，但它對任意輸入 shape 通用、無 recompilation 風險，是「快速通用核函式 vs 單一 shape 最佳化核函式」的務實選擇。

## 結論
這篇文章以實際追蹤數據示範了 PyTorch 效能分析的關鍵思維：先提出預期、再驗證，並理解每一層優化（epilogue 融合、compile fusion、手寫 tuned kernel）各自的優劣與適用情境；下一篇文章將從 MLP block 延伸到 attention block 與完整模型。

---
