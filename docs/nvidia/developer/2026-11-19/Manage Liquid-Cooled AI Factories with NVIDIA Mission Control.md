# Manage Liquid-Cooled AI Factories with NVIDIA Mission Control

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-19
- **原文連結**: https://developer.nvidia.com/blog/manage-liquid-cooled-ai-factories-with-nvidia-mission-control/

## 核心主題
NVIDIA Mission Control 軟體連接 IT 與 OT 系統，協調液冷 AI 工廠的洩漏響應並監控運算與設施狀況。

## 關鍵重點
- **可配置的 MQTT 整合**：支援與建築管理系統 (BMS) 的標準化介面，透過 MQTT 協議交換數據以協調洩漏響應策略。
- **洩漏行動策略**：基於洩漏位置與受影響設備數量定義自動化響應，包含預設模板（設備、機架、整排、房間、建築層級），可跨 BMC、集群管理器和 BMS 協調動作。
- **機架管理命令**：提供 electricaloverview、liquidcoolingoverview、leakdetectionoverview 和 leakinfo 等命令，整合液冷基礎設施數據以監控狀況並支援事件調查。
- **可觀測性整合**：透過 Prometheus 端點暴露監控數據，支援預製 Grafana 儀表板、自訂儀表板、警報規則，並可整合現有監控工作流。

## 結論
NVIDIA Mission Control 提供標準化整合框架，幫助企業在部署 NVIDIA GB200 NVL72 和 GB300 NVL72 系統時，簡化液冷 AI 工廠的 IT/OT 系統整合，提升響應時間並確保合規性。

---