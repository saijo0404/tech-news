# The Rise of LLMJacking: How Threat Actors Monetize Compromised Cloud and Model Resources

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-02
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/llmjacking-monetizing-compromised-cloud-models/

## 核心主題
這篇文章探討了 LLMJacking 攻擊趨勢，即攻擊者劫持企業大語言模型服務以進行詐騙和獲利，並提供雲端 LLM 服務的安全防護指南。

## 關鍵重點
- **LLMJacking 攻擊模式**：攻擊者利用暴露的雲端身份憑證（IAM 憑證、服務帳戶金鑰、GitHub PAT 等）、權限提升和未授權啟用來劫持 LLM 服務，包括啟用 managed 生成式平台、使用「burn and rotate」策略繞過速率限制
- **獲利模式**：包括 LLM Mixers 作為非法轉送閘道轉售未授權 LLM 訪問、代幣化服務（如 Jet Night 提供每月約 60 美元的無限代碼服務）、通過地下商店銷售工具並轉嫁費用給受害者
- **防護策略**：強化身份存取管理 (IAM) 與供應鏈安全、實施多因素認證 (MFA)、限制 API 金鑰範圍與使用限制、監控異常請求、部署 VPC 防火牆規則與 API 預算限制
- **雲端平台監控指標**：AWS 監控 CloudTrail 中的 Converse、InvokeModel 等 API 操作；Azure 監控 Azure Activity/Diagnostic Logs 中的模型調用事件；GCP 監控 Gemini Enterprise Agent Platform 的預測服務操作

## 結論
企業整合高階模型時應特別注意 LLMJacking 風險，透過強化身份存取管理、集中式秘密管理、最小權限原則及定期審計來降低風險，並建立受信任模型倉庫以確保雲端 LLM 服務的安全。

---