# When One GPU Isn't Enough Serving GLM-5.3 Across Two NVIDIA DGX Stations with vLLM

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-13
- **原文連結**: https://developer.nvidia.com/blog/when-one-gpu-isnt-enough-serving-glm-5-3-across-two-nvidia-dgx-stations-with-vllm/

## 核心主題
文章介紹了在兩台 NVIDIA DGX 站點上分佈運行 753B 參數 GLM-5.3 模型並進行性能測試的完整流程，展示了使用 vLLM 實現大規模模型服務的最佳實踐。

## 關鍵重點
- **模型部署架構**：模型分佈在兩台 GPU 上，透過 RoCE 網路交換部分結果，每台 GPU 持有約 218GB 權重，使用張量平行化 (TP=2) 分擔計算負載
- **技術優化策略**：採用 vLLM 分佈式服務、FP8 KV-Cache 儲存（記憶體减半）、前綴快取 (prefix caching) 和多 token 預測 (MTP) 技術
- **性能測試結果**：在 SPEED-Bench 編碼數據集測試中，C16 並行度達到最佳吞吐量 607.8 tok/s，但 C32 並行度導致延遲大幅增加至 453.5 秒
- **實施步驟**：準備兩台 DGX Station 並驗證連接、下載並複製模型檢查點、啟動分佈式 vLLM 服務、使用 AIPerf 進行性能測試

## 結論
此分佈式架構適合本地敏感數據推理、代理原型開發及提示迭代場景，無需每字元成本，為大規模模型服務提供了可擴展的解決方案。
---