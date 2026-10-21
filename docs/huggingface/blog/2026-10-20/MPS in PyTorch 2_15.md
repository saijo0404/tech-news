# MPS in PyTorch 2.15

- **來源**: Hugging Face
- **發布日期**: 2026-10-20
- **原文連結**: https://huggingface.co/blog/mps-pytorch-2-15

## 核心主題
PyTorch 2.15 為 Mac 的 MPS（Metal Performance Shaders）後端帶來重大改進，包括 FP8 支援、更快的語言模型解碼、更小的記憶體佔用以及更多操作支援。

## 關鍵重點
- **FP8 支援**: 引入 `float8_e4m3fn` 張量，記憶體佔用僅為 BF16 的一半，並支援 `F.scaled_mm` 進行縮放矩陣乘法。
- **語言模型解碼加速**: MoE 模型解碼速度提升 5–6.5 倍（Qwen3.6-35B-A3B 從 9.4 提升至 61.3 tokens/s），softmax 加速約 8 倍。
- **記憶體優化**: Wan2.2 視頻 VAE 解碼記憶體峰值從 270GB 降至 8GB，透過常數填充（constant padding）改進實現。
- **更多操作支援**: 複雜數值計算（LU 分解、三角解）、小矩陣逆矩陣、QR 分解等更多線性代數操作支援 MPS。
- **系統要求更新**: MPS 需要 macOS 15 或更高版本，PyTorch 2.15 需要 Python 3.11 或更高版本。

## 結論
PyTorch 2.15 顯著提升了 Mac 上運行和訓練 PyTorch 模型的能力，特別是在記憶體效率和性能方面，使 Mac 成為更可靠的 PyTorch 模型運行和訓練平台。
---
