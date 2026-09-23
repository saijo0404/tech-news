# Simplifying Model Serving Across Multiple GPUs with NVIDIA TensorRT Multi-Device Integration in NVIDIA Dynamo-Triton

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-21
- **原文連結**: https://developer.nvidia.com/blog/simplifying-model-serving-across-multiple-gpus-with-nvidia-tensorrt-multi-device-integration-in-nvidia-dynamo-triton/

## 核心主題
NVIDIA Dynamo-Triton 26.07 版本整合了 TensorRT 多裝置推理功能，允許單一模型實例跨多個 GPU 執行，大幅降低延遲並提升生成式 AI 推理效率。

## 關鍵重點
- **TensorRT 11.0 起支援多裝置推理**：單一 TensorRT 網路可透過 NCCL 背後的分散式集合在多個 GPU 上執行，同時保留 TensorRT 推理優化。
- **Dynamo-Triton 26.07 啟用多裝置功能**：單一 KIND_MODEL 實例可擁有多個 GPU，透過單一 gRPC 端點提供分散式推理服務，無需客戶端協調 GPU 實例。
- **Ulysses 上下文並行技術**：在 NVIDIA Cosmos 3 Nano 視頻生成案例中，將 44,160 個視頻 token 分佈到最多 8 個 GPU，延遲從單 GPU 的 156.6 秒降至 8 GPU 的 34.2 秒。
- **Transformer RPC 速度提升 6.09 倍**：8 GPU 配置下，Transformer RPC 速度提升 6.09 倍，延遲佔比從 93.4% 降至 70.2%。
- **輸出品質驗證通過**：CP2、CP4 和 CP8 配置均通過設定標準（MAE ≤ 25，PSNR ≥ 18 dB），視覺驗證確認輸出品質符合預期。

## 結論
NVIDIA Dynamo-Triton 與 TensorRT 多裝置整合為生成式 AI 部署提供了實用解決方案，特別適合延遲敏感型工作流。團隊可透過增加 GPU 資源來縮短請求延遲，同時保持應用介面和工作流程穩定。建議團隊根據資源與延遲的權衡決策，並評估並發請求吞吐量、每生成視頻成本及總擁有成本等指標。

---