# Fine-Tuning NVIDIA Nemotron for Saudi Arabic Dialects with a Path to Other Languages

- **來源**: developer.nvidia.com
- **發布日期**: 2026-10-01
- **原文連結**: https://developer.nvidia.com/blog/fine-tuning-nvidia-nemotron-for-saudi-arabic-dialects-with-a-path-to-other-languages/

## 核心主題
這篇文章介紹了如何使用 NVIDIA NeMo 框架微調 NVIDIA Nemotron 3.5 ASR 模型以支援沙特阿拉伯方言（Najdi 和 Hijazi），並提供擴展到其他語言方言的路徑。

## 關鍵重點
- **微調流程**：使用 133.7 小時語料，權重回放混合（90% 目標方言 + 7% 英文 + 3% 阿拉伯語），防止災難性遺忘
- **準確性提升**：全方言 WER 從 55.05% 降至 29.96%，英語表現從 11.04% 降至 10.42%
- **推理優化**：擴大注意力上下文至 13 幀 + beam-8 解碼，WER 降低 2.71 分
- **上下文大小影響**：將預覽上下文從 3 增加到 13 個框架，WER 降低 1.31%，但延遲增加約 800ms
- **使用場景建議**：批處理转录（電話錄音、會議記錄）適合，即時字幕延遲過高不適合
- **最佳平衡點**：MALSD beam 4 提供最佳速度-準確性平衡（WER 28.81%）
- **多語言應用**：工作流程相同，但需調整語料元數據、正字化、分詞器覆蓋率等
- **說話者識別整合**：結合細化 ASR 輸出與說話者識別，可產生說話者歸屬的字幕
- **重要設定**：無論使用何種策略，都應設定 `strip_lang_tags=True`，避免語種標籤被計入錯誤

## 結論
此工作流程適用於資源有限但需保留其他語言能力的場景，並可擴展至其他語言方言。通過權重回放混合和推理優化，可在提升方言準確性的同時保持多語言能力。

---