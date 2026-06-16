---
# Building AI Agents for AR Glasses and XR Devices with NVIDIA XR AI

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://developer.nvidia.com/blog/building-ai-agents-for-ar-glasses-and-xr-devices-with-nvidia-xr-ai/

## 核心主題
NVIDIA XR AI 進入公共測試版，提供開源開發者建構 AR 眼鏡與 XR 裝置上多模態 AI 智能體的基礎架構，整合即時感測器串流、視覺理解、語音互動與企業工具調用。

## 關鍵重點
- **模組化 XR Agent 架構**：XR AI 將 XR 裝置的相機幀、麥克風音訊與資料訊息透過 XR Media Hub 路由至 AI 模型與工具，採用 Cosmos VLM 進行視覺錨定、Nemotron 模型處理語音與推理、MCP（Model Context Protocol）連接企業資料與工具，支援多用戶與多智能體情境，並可透過 CloudXR 串流 3D 空間內容。
- **六步驟開發流程**：（1）克隆 GitHub 開源倉庫取得範例與核心基礎設施；（2）啟動包含 Parakeet 語音轉文字、Cosmos-Reason1 視覺語言推理、Llama Nemotron 快速語言回應與 Nemotron-3 深度工具調用的模型服務堆疊；（3）運行最簡 VLM 智能體驗證即時多模態互動；（4）透過 MCP 伺服器（vlm-mcp、video-mcp、oxr-mcp 等）連接企業系統與 RAG 流程；（5）使用 NeMo Agent Toolkit 實現工具發現與多智能體協調；（6）可選加入 CloudXR 空間渲染。
- **從感知到企業行動的應用藍圖**：除了即時感知環境，XR Agent 能觀察 Procedures、檢查、維護活動，並利用 NVIDIA VSS 建立可搜尋的視覺知識庫，支持報告、培訓、合規審查與 RAG 流程；開發者還能採用混合模型策略——小模型處理即時回應、大模型進行深度推理，兼顧延遲與品質。

## 結論
NVIDIA XR AI 以模組化設計解決了 AR/XR 裝置上 AI 體驗的基礎設施缺口，讓開發者能從單一基礎架構擴展出從即時感知、語音互動、企業工具調用到空間渲染的完整智能體能力。搭配 NeMo Agent Toolkit 與 CloudXR，開發者不僅能建構現場服務、醫療研究、製造維護等行業應用，更能將物理世界的視覺資訊轉化為組織知識資產，開啟空間 AI 的新篇章。

---
