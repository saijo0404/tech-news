# Dense vs MoE Models: Active Parameters, Throughput, and When to Choose Each

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-15
- **原文連結**: https://developer.nvidia.com/blog/dense-vs-moe-models-active-parameters-throughput-and-when-to-choose-each/

## 核心主題
這篇文章深入探討了 Dense 模型與 Mixture-of-Experts (MoE) 模型架構的差異，解釋了它們在參數激活、記憶體成本與吞吐量方面的不同表現，並提供選擇建議。

## 關鍵重點
- **記憶體與運算解耦**：MoE 模型將記憶體成本（總參數）與運算成本（活躍參數）解耦，使記憶體成本固定而運算成本隨每個 token 的活躍參數變化。
- **吞吐量優勢**：在相同總參數下，MoE 模型（如 Nemotron 3.5 Lightning）因只激活部分參數（如 30B 模型只激活 3B），在單 token 處理時具有更高的吞吐量。
- **高併發時的延遲差異**：在高併發場景下，MoE 模型的延遲優勢會縮窄，因為路由決策和記憶體搬移會增加複雜度。
- **微調風險**：MoE 模型微調需特別小心，避免路由不平衡（某些專家過熱或完全停用），建議使用 LoRA/PEFT 或特定模型食譜。
- **量化影響差異**：MoE 模型中路由器和重投影層對量化的敏感度與 Dense 模型不同，需特別注意。

## 結論
選擇 Dense 還是 MoE 模型取決於部署限制：若追求簡單部署和可預測延遲，Dense 模型更適合；若追求高吞吐量且能管理複雜度，MoE 模型更具優勢。記憶體預算、併發需求、微調計劃和量化行為都是關鍵考量因素，而非單純比較參數數量。

---