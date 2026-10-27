# Turning Database Grading into RL Rewards: Post-Training Agents with ThinkingBox

- **來源**: Hugging Face
- **發布日期**: 2026-10-22
- **原文連結**: https://huggingface.co/blog/microsoft/thinkingbox-training

## 核心主題
Microsoft 與 Hugging Face 聯合開發的 ThinkingBox 系統，透過將資料庫狀態的可執行檢查轉化為獎勵函數，成功提升了 Qwen3.8-27B 模型在生產環境中的可靠性與成本效益。

## 關鍵重點
- **單一嘗試成功率不應單獨作為模型選擇標準**：Observed 20/20（可觀察到的 20/20 成功率）更能反映生產環境所需的可靠性
- **pass@1 提升顯著**：從 51.70% 提升至 60.78%，提升 9.08 個百分點
- **可靠性大幅提升**：Observed 20/20 成功率從 38% 提升至 21.10%，提升近 3 倍
- **成本效益改善**：每項可靠任務成本從 $24.36 降至 $8.00，下降 67.2%
- **訓練方法採用 GRPO**：使用 Group Relative Policy Optimization 進行 50 步微調，採用「offline policy-relative difficulty」策略選擇訓練任務
- **五個領域均見成效**：retail、auto insurance、travel、neobank、consulting 領域的 pass@1 均提升，零售業在 Observed 20/20 上提升最大（+24.5 個百分點）
- **訓練池篩選機制**：透過離線通过率过滤器和 Jeffreys 後驗概率模型評估任務難度，最終包含 187 個任務
- **訓練環境要求**：需 Linux、Python 3.12、Verl 0.9.0、NVIDIA GPU（24 H100 GPU，50 步訓練）

## 結論
ThinkingBox 系統證明將資料庫狀態的可執行檢查轉化為獎勵函數是訓練 AI 代理的有效方法。單一成功不等同於可靠性，Observed 20/20 更能反映生產環境所需的可靠性。訓練使模型更專注於可重複成功的任務，而非擴大覆蓋範圍，同時大幅降低訓練成本。

---