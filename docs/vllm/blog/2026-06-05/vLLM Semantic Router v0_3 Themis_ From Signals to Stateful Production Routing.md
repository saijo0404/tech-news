---
# vLLM Semantic Router v0.3 Themis: From Signals to Stateful Production Routing

- **來源**: vLLM Blog
- **發布日期**: 2026-06-05
- **原文連結**: https://vllm.ai/blog/2026-06-05-v0.3-vllm-sr-themis-release

## 核心主題
vLLM Semantic Router 發布 v0.3 Themis 版本，將語義路由從單純的請求分類升級為具備狀態記憶、可稽核與生產環境可用的完整路由控制平面，透過 350+ commits 整合信號、投影、決策、演算法與模型選擇的穩定契約。

## 關鍵重點
- **統一配置契約與信號－投影－決策管道**：v0.3 引入標準化 `config.yaml` 結構（`version: v0.3`），消除 Docker、Dashboard、Helm 與 CRD 間的重疊配置語言；新增信號（從請求抽取證據）與投影（將證據轉換為策略概念如 `support_fast`、`support_escalated`）的分層架構，使政策撰寫可測試、可回溯且無需隱蔽邏輯。
- **會話感知代理路由（SAAR）**：首次實作生產級 SAAR，為多輪代理會話加入路由器專屬記憶、工具迴路硬鎖定、提供者狀態可攜性檢查、前缀本地化權重與切換經濟學，使編碼代理與長程工具迴路的模型切換決策兼顧品質與串流穩定性。
- **協議相容、操作控制台與硬體路徑擴充**：原生支援 Anthropic `/v1/messages` 與 streaming SSE 轉譯、Dashboard 升級為包含拓撲乾跑、Replay 洞察、政策版本生命周期的操作控制台、CLI 更明確，並新增 Intel OpenVINO 分類器/嵌入推論與 AMD ROCm 完整驗證；RouterArena 排名重返 #1，以 75.4 加權得分、$0.11/1K 查詢成本與 73.1 魯棒性展現競爭力。

## 結論
Themis 不是一個單一功能的版本，而是將過去兩個版本的野心收束為一條穩定、可稽核的生產級路由管線；團隊已將 v0.4 Hermes 列為自改進化路由器，預期透過 GPU 規模效能研究、DSL 食譜調校與編碼器微調形成閉環，持續推動語義路由的自動化與可靠性。

---
