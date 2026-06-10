# 使用 Hermes Agent 與 NVIDIA NemoClaw 部署自我進化代理，加速更安全的研究

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://developer.nvidia.com/blog/deploy-self-evolving-agents-for-faster-more-secure-research-with-a-hermes-agent-and-nvidia-nemoclaw/

## 核心主題
本文以 OpenSource 範例展示如何將 Hermes Agent、NVIDIA NemoClaw 與 OpenShell 安全執行環境整合，打造能同時存取內部資料（Outlook、Slack）與公開資源（GitHub）並自我學習的個人化代理，適用於銷售研究、客服排程、競爭分析等多種場景。

## 關鍵重點
- **安全沙箱與資料隔離架構**：OpenShell 將憑證管理與網路政策強制執行於沙箱層級，Hermes Agent 本身無法直接接觸 Slack/Outlook Token，認證由沙箱代理處理；代理被禁止直接存取公開網路，GitHub 與 NVIDIA 論壇資料透過 ETL 流程取得後以唯讀方式提供，即使代理被攻陷亦無法外洩資料。
- **一次教學、全域記憶的自我進化機制**：Hermes Agent 能從聊天對話中識別模式並自動寫入 SKILL.md（YAML frontmatter 加上格式模板），透過 snapshot/tear-down/rebuild/restore 流程可將技能、記憶、會話與排程任務完整保存，重建沙箱後仍維持學習成果。
- **可觀察性與模型/運行時三層架構**：代理由 Nemotron 3 Super 120B 模型驅動推理、Hermes Agent 提供技能/會話/記憶層、OpenShell 負責檔案與網路政策；所有決策以 ATIF 格式記錄並由 NeMo Relay 預設追蹤，可串流至 Arize Phoenix 即時除錯；網路政策以 policy.yaml 宣告而非提示詞，違例直接返回 403。

## 結論
NemoClaw 結合 Hermes Agent 與 OpenShell 提供了一套完整、可觀察、自我進化的代理開發框架，讓開發者以單一指令快速部署具備安全沙箱的長期代理，並在生產環境重建時保留已學技能，大幅降低代理式 AI 的維護成本與安全風險。
