# Watermarking in vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-09-24
- **原文連結**: https://vllm.ai/blog/2026-09-24-watermarking-in-vllm

## 核心主題
vLLM 實現了基於 Gumbel-max 算法的無失真文本水印技術，利用大語言模型的隨機性來標記內容來源，同時保持生成品質和效率。

## 關鍵重點
- **無失真水印**：使用 Gumbel-max 技巧，在不改變模型輸出分佈的前提下嵌入可檢測的水印信號
- **高效實現**：將偽隨機數生成、Gumbel 轉換和 argmax 合併為單一 GPU 核函式，性能影響極小（-1.1% 到 +2.0%）
- **雙鍵機制**：支援 speculative decoding，使用不同鍵分別處理草稿 token 和目標 token，保持檢測信號
- **檢測機制**：只需秘密鍵和分詞器即可檢測，無需模型權重或 logits，長文本檢測準確度高
- **輸出多樣性**：透過上下文去重和雙鍵路由解決重複上下文導致的輸出多樣性降低問題

## 結論
vLLM 現在支援基於 Gumbel-max 的無失真水印，具有高效的 GPU 生成和 speculative decoding 支援。評估顯示性能過載極小，同時保持輸出品質和多樣性。使用者可透過 `--watermark-config` 參數啟用此功能。

---
