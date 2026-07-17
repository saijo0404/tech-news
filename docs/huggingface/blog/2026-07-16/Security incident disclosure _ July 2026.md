# Security incident disclosure — July 2026

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-16
- **原文連結**: https://huggingface.co/blog/security-incident-july-2026

## 核心主題
Hugging Face 遭遇首次由自主 AI 代理系統驅動的入侵攻擊，成功識別並修復了漏洞。

## 關鍵重點
- 攻擊者利用數據處理管道中的兩個代碼執行路徑（遠端代碼數據集載入器和模板注入）進行初始入侵
- 攻擊由自主 AI 代理框架驅動，執行數千個自動化動作，並使用自適應的 C2 階段
- Hugging Face 使用 GLM 5.2 開源模型在本地進行 forensic 分析，成功識別攻擊者活動
- 已修復根本漏洞，撤銷並旋轉了受影響的憑證，並部署了額外的防護措施

## 結論
這標誌著自主 AI 驅動攻擊已成為現實，防禦方需要具備在本地運行的能力模型以應對安全事件。

---