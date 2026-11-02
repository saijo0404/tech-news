# Run AI Models for Edge Application Development with Just a Few Commands

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-30
- **原文連結**: https://developer.nvidia.com/blog/run-ai-models-for-edge-application-development-with-just-a-few-commands/

## 核心主題
NVIDIA 透過 TensorRT Edge-LLM 和 trtedge CLI，讓開發者能在 DGX Spark 平台上僅用幾行命令即可運行 AI 模型，並支援從開發到部署的完整流程。

## 關鍵重點
- **DGX Spark 64GB 平台**：提供嵌入式開發者原型設計、微調和測試 AI 模型與代理的完整平台。
- **TensorRT Edge-LLM**：提供輕量級 C++ 推理運時，支援從 DGX Spark 開發到 Jetson Thor、DRIVE AGX Thor 和 IGX Thor 部署。
- **trtedge CLI**：可下載模型並建立優化後的 TensorRT 引擎，啟動聊天介面或 API 伺服器。
- **DSpark 猜測解碼**：使用三個草稿 token 加速生成速度，HumanEval 提示從 73.4 提升至 126.9 tokens/秒，峰值記憶體仍為 27.9GB。

## 結論
透過 NVIDIA 的嵌入式 AI 解決方案，開發者可以大幅降低 AI 模型部署門檻，在資源受限的邊緣設備上實現高效能、低延遲的 AI 應用。

---