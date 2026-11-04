# StateBench: Testing how language models track state changes over long documents

- **來源**: Hugging Face
- **發布日期**: 2026-11-03
- **原文連結**: https://huggingface.co/blog/allenai/statebench

## 核心主題
介紹 StateBench 基准测试，评估语言模型在长文档中追踪实体状态变化的能力，并比较不同架构的表现。

## 關鍵重點
- StateBench 包含四个难度级别的状态追踪问题，从简单的不可变赋值到复杂的引用赋值，帮助研究人员理解不同架构的能力边界。
- 研究发现，循环和混合模型（如 Gated DeltaNet）在直接训练后比 Transformer 模型能更好地泛化，尤其在处理长序列时表现更优。
- 前沿模型（如 Gemini 3.8 Flash、Claude Opus 5.5 和 GPT-6）在更长的输入上仍然会在更难的状态追踪问题上失败，准确率降至 13% 或更低。
- Gated DeltaNet 模型在最长序列上表现最好，能处理约 10 倍于训练长度的序列，证明了训练而非架构本身是限制因素。

## 結論
StateBench 为研究人员提供了更细粒度的方法来发现模型失效点，并作为开发具有更强状态追踪能力的未来架构的指南星，帮助指导未来系统的开发方向。
---
