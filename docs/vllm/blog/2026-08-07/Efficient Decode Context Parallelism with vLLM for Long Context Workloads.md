# Efficient Decode Context Parallelism with vLLM for Long Context Workloads

- **來源**: vLLM Blog
- **發布日期**: 2026-08-07
- **原文連結**: https://vllm.ai/blog/2026-08-07-decode-context-parallelism

## 核心主題
這篇文章介紹了 vLLM 實現的解碼上下文並行（Decode Context Parallelism, DCP）技術，解決長上下文推理時 KV Cache 記憶體不足的問題，大幅提升高併發場景下的吞吐量。

## 關鍵重點
- **傳統 TP 的瓶頸**：在長上下文推理中，傳統張量並行（TP）會將 KV Cache 按注意力頭切分，但當 TP 大於 KV 頭數量時，會導致 KV Cache 複製，消耗大量 GPU 記憶體，限制系統能處理的併發請求數量。
- **DCP 的解決方案**：DCP 將 KV Cache 沿序列維度切分，每個 GPU 只存儲同一序列中的一部分 token 的 KV 數據。例如，200K token 的請求可被分為 4 份，每個 GPU 負責 50K token。這大幅降低每個 GPU 的記憶體佔用，使系統能支援更高併發。
- **實驗結果**：在 8×B200 節點上測試 Kimi K2.6 模型，DCP 在 512 併發時達到 6,091 tok/s/GPU，而傳統 TP 在 64 併發時就達到記憶體上限（1,863 tok/s/GPU）。DCP 即使在 512 併發時仍僅使用 82% KV 記憶體。
- **支援模型類型**：DCP 支援 MLA（Multi-head Latent Attention）和 GQA（Grouped-Query Attention）兩種後端模型。MLA 模型因 KV 被壓縮為單一潛在向量，最適合 DCP；GQA 模型則利用原本會複製的 KV 頭數量來決定 DCP 的最大分割度。
- **使用方式**：只需在 vLLM 配置中加入 `--decode-context-parallel-size` 參數即可啟用，例如：`vllm serve model --tensor-parallel-size 2 --decode-context-parallel-size 2`。
- **未來發展**：vLLM 團隊正擴展 DCP 支援更多模型（如 Kimi K3），優化通訊核，並開發 Prefill Context Parallelism（PCP）以支援預填充階段。

## 結論
Decode Context Parallelism 代表了一種根本性的重新思考，如何組織 GPU 以處理長上下文推理。它不再強迫 GPU 複製 KV Cache 或閒置，而是將每個 GPU 充分利用，在注意力階段切分序列，並在 FFN 權重載入階段進行優化。結果是一個能隨上下文長度優雅擴展而非退化的系統。vLLM 原生支援 DCP，已準備好為下一代長上下文代理應用（如文檔推理、多會話代理流程）提供符合生產需求的吞吐量與延遲。

---