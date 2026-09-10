# When to Use Encode-Prefill-Decode Disaggregation to Accelerate Multimodal Model Serving

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-09
- **原文連結**: https://developer.nvidia.com/blog/when-to-use-encode-prefill-decode-disaggregation-to-accelerate-multimodal-model-serving/

## 核心主題
NVIDIA Dynamo 框架透過 Encode-Prefill-Decode (EPD) 分散化技術，將視覺編碼階段與 LLM 預填充和編碼階段分離，以加速多模態模型服務。

## 關鍵重點
- EPD 分散化為圖像密集型提示帶來最高 5 倍的首 token 時間 (TTFT) 提升和 7 倍的全流程響應時間提升，特別適合短至中等輸出和量化混合專家模型。
- 有三種編碼器放置架構：聚合服務（所有階段在同一 GPU 上）、colocated 編碼器（與預填充-編碼工人共享 GPU）、以及分散式編碼器（在較低成本 GPU 層級運行）。
- 效益取決於輸入媒體負載、輸出序列長度、模型大小/精度和流量組合；當編碼主導延遲或大型密集模型減少視覺編碼器計算佔比時，收益會減少。
- 在混合文本和多模態流量中，EPD 透過消除頭部行阻塞，將文本請求的平均 TTFT 降低 42.2%，圖像請求降低 30.8%。
- 將 LLM 權重量化為 NVFP4 而保持視覺編碼器在 BF16，可將 colocated EPD 的 goodput 從 1.78 倍提高到 2.64 倍。

## 結論
EPD 分散化並非萬能解方，在圖像負載高、輸出序列短、模型較小或精度的場景下效益最大。使用者應根據實際工作負載、模型配置和硬體環境來選擇合適的部署策略，並結合嵌入緩存和多模態 KV 路由等技術進一步優化。

---