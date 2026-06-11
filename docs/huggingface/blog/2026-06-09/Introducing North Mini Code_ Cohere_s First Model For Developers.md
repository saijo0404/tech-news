---
# Introducing North Mini Code: Cohere's First Model For Developers

- **來源**: Hugging Face Blog (CohereLabs)
- **發布日期**: 2026-06-09
- **原文連結**: https://huggingface.co/blog/CohereLabs/introducing-north-mini-code

## 核心主題
Cohere 推出首款專為開發者設計的字元模型——North Mini Code，一款 30B 總參數、3B 活躍參數的 MoE 架構模型，在代理式軟體工程與程式碼生成任務上表現卓越，並以 Apache 2.0 授權在 Hugging Face 開放。

## 關鍵重點
- **跨工具框架的魯棒性訓練**：North Mini Code 在第二階段 SFT 中接觸 SWE-Agent、mini-SWE-agent、OpenCode 與 Terminus 等多種工具框架，僅以 6% 額外界面資料即達成 10% 的跨框架提升，並透過少量純文字格式數據實現 Terminus 2 的無縫泛化，證明不同框架所需技能互補而非衝突。
- **異步 RLVR 與多環境訓練**：採用 CISPO 目標與 FIFO 隊列解耦取樣與學習，以 512 rollouts 同時訓練終端任務與軟體工程任務，RLVR 在 Terminal-Bench v2 提升 7.9%、SWE-Bench 提升 3.0%，並顯著減少無效工具呼叫、迴圈重複與冗長軌跡。
- **內部人類評估與全面基準**：在程式碼解釋、編輯、資料視覺化與從零實作四項功能上，RLVR 模型在程式碼編輯任務獲得 66.1% 的偏好勝率；在 Artificial Analysis Coding Index 以 33.4 分數超越 Qwen3.5、Gemma 4、Devstral 乃至 Nemotron 3 Super（120B）等更大模型。

## 結論
North Mini Code 是 Cohere 邁向開發者模型的開端，透過精心設計的「長上下文 SFT 先導 → RLVR 強化」串聯、多框架魯棒性訓練與異步 RL，在 3B 活躍參數下展現出與更大模型匹敵的代理程式碼能力；模型以 BF16 與 FP8 量化版本開放於 OpenCode、Cohere API 與 Hugging Face。

---
