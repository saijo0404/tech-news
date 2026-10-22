# Profiling TorchNeuron (Part 1): System-level profiling on AWS Trainium

- **來源**: Hugging Face
- **發布日期**: 2026-10-21
- **原文連結**: https://huggingface.co/blog/amazon/profiling-torchneuron-part-1

## 核心主題
這篇文章介紹了如何使用 TorchNeuron 在 AWS Trainium 晶片上進行系統層面的效能分析，並比較了三種不同的 RMSNorm 實現方式。

## 關鍵重點
- 使用 NeuronConfig 和 NeuronProfiler 配置 profiler，並透過 key_averages() 表格識別消耗 Neuron 設備時間的操作
- 使用 Neuron Explorer 追蹤操作從框架分發到硬體執行的完整流程，包括 framework dispatch、runtime scheduling 到 hardware execution
- 比較三種實現：逐個 PyTorch 操作（Naive ops）、torch.rms_norm 和 torch.compile 後的版本，發現編織（fusion）可將設備時間從 2.355ms 降至 375-403μs
- 編織能消除硬體執行間隙並避免中間值材料化，大幅降低設備時間

## 結論
透過系統化分析，可以識別效能瓶頸並決定是否使用編織操作或 torch.compile 來降低成本。此工作流程可應用於更大模型，找出熱點並驗證是否透過編織或編譯能減少成本。

---