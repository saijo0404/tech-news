# 模型量化：以 NVIDIA TensorRT 將 FP8 檢查點轉化為高效能推論引擎

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://developer.nvidia.com/blog/model-quantization-turn-fp8-checkpoints-into-high-performance-inference-engines-with-nvidia-tensorrt/

## 核心主題
NVIDIA 詳細說明如何將 ModelOpt 產生的 FP8 量化檢查點經 ONNX 匯出並編譯為 NVIDIA TensorRT 引擎，完成從模型最佳化到生產部署的端到端流程；以 CLIP 模型為實例，FP8 量化在 RTX 6000 Ada GPU 上帶來最高 48% 的引擎體積縮減與 1.45 倍推論加速。

## 關鍵重點
- **ModelOpt → ONNX → TensorRT 端到端部署流程：六階段量化與編譯，產出生產級推論引擎**：完整工作流程包含五個階段——（1）以 ModelOpt 產出高品質 FP8 量化 CLIP 檢查點；（2）將檢查點匯出為 ONNX 格式，利用 ModelOpt 內建輔助函式將權重端的量化 - 反量化（Q-DQ）配對摺疊為僅反量化的 FP8 儲存鏈，使文字編碼器 ONNX 檔從 237 MB 縮至 156 MB（~34%）、影像編碼器從 582 MB 縮至 292 MB（~50%）；（3）以 trtexec 將 ONNX 編譯為 TensorRT 引擎，使用 `--stronglyTyped` 確保 FP8 權重與激勵實際以 FP8 執行，並需預先將 FP32 縮放常數與 Cast 運算轉回 FP16 以避免型別不符錯誤；（4）以 trtexec 或 Nsight Deep Learning Designer 進行效能分析；（5）將引擎儲存至磁碟供獨立推理或 Triton Inference Server 部署。
- **RTX 6000 Ada GPU 實測結果：引擎體積縮減最高 48%、影像側加速 1.39 倍、文字側加速 1.45 倍**：在 NVIDIA RTX 6000 Ada GPU（FP8 支援起步架構）上以靜態批次 128 執行基準測試——（1）引擎體積：影像編碼器從 588 MB 降至 306 MB（-48%）、文字編碼器從 238 MB 降至 156 MB（-34%），整體磁碟佔用近乎減半；（2）推論延遲：影像編碼器從 166.2 ms 降至 119.8 ms（1.39x 加速）、文字編碼器從 13.2 ms 降至 9.1 ms（1.45x 加速）；（3）逐層剖析顯示 FP8 加速來源：GEMM 從約 1.8 ms 降至 0.84 ms（超過 2 倍加速，由 FP8 Tensor Core 核心帶來）、FP16 中的「融合」層類別在 FP8 中消失（整個注意力區塊路由至專門的 FP8 MHA 核心）、精度甜甜圈圖從大半橙色（FP16）轉為大半紫色（FP8），證實量化權重與激勵確實在 FP8 Tensor Core 上運行。
- **TensorRT 量化機制：Q/DQ 節點融合消除往返轉換，以低精度核心提升運算吞吐量並降低記憶體頻寬**：匯入 ONNX 時，TensorRT 尋找 QuantizeLinear / DequantizeLinear（Q/DQ）節點標記張量從全精度轉為低精度（如 FP8）的點；在建置時，最佳化器將 Q/DQ 節點融合至相鄰層，以專門核心取代原始層，直接操作低精度張量——消除不必要的量化 - 反量化往返轉換，讓引擎以更高運算吞吐量與更低記憶體頻寬執行；圖例以 FP8 GEMM 展示：ONNX 中激勵與權重皆被 Q/DQ 對包覆，TensorRT 最佳化器融合後剩下一個單一 FP8 GEMM 核心，直接接收 FP8 量化激勵與預存 FP8 權重張量。

## 結論
這篇技術文章完整呈現了 NVIDIA ModelOpt 與 TensorRT 的協同威力——從 FP8 量化檢查點到生產級推論引擎的端到端流程，不僅提供了可直接執行的程式碼範例（含 ONNX 匯出、型別修正、trtexec 編譯），更以 CLIP 模型的實測數據具體展示了量化帶來的實質效益：引擎體積近乎減半、推論速度提升 40% 以上、GEMM 層超過兩倍加速；更重要的是，文章深入剖析了加速背後的機制——Q/DQ 節點融合讓 FP8 張量直接流入 Tensor Core，消除了傳統量化中昂貴的往返轉換開銷；對於需要大規模部署 AI 模型的團隊而言，這條 ModelOpt → ONNX → TensorRT 的標準化路徑提供了可驗證、可複製的高效能部署藍圖。
