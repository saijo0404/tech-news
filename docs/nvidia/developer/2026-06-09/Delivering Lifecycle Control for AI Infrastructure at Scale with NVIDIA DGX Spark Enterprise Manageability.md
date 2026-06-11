# 以 NVIDIA DGX Spark 企業級管理功能，大規模提供 AI 基礎設施的生命週期控制

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://developer.nvidia.com/blog/delivering-lifecycle-control-for-ai-infrastructure-at-scale-with-nvidia-dgx-spark-enterprise-manageability/

## 核心主題
本文介紹 NVIDIA DGX Spark 新增的「企業級管理功能」（Enterprise Manageability），提供企業 IT 團隊從設備採購到報廢的全生命週期管理框架，讓 AI 基礎設施能像其他關鍵基礎設施一樣，具備可部署、可觀察、安全且易於管理的企業級運營能力。

## 關鍵重點
- **無代理 SSH 整合**：採用無代理（agentless）SSH 執行方式，以標準 JSON 格式回傳結果，可直接融入企業現有的 CMDB、SIEM 與監控系統，並支援 Progress Chef、Puppet、Canonical Landscape 等第三方工具。
- **六大生命週期階段**：涵蓋採購接收、初始設定、持續監控、維護窗口、事件回應，到設備報廢與重新部署，各階段均有對應的生產級工具與腳本。
- **診斷與更新管理**：提供 `spark_diagctl.py`（L1 健康檢查 / L2 深度證據包）與 `reset_reason_reporter.py`（重新啟動原因分析）等診斷工具，以及 `spark_updatectl.py` 協調多層更新（核心、驅動程式、韌體、容器運行時等），支援階段性部署與滾動回退。
- **企業級安全能力**：包含驗證開機、加密狀態回報、APT 套件簽名驗證、帶有鏈條證據的工廠重置，以及可選的 UEFI 資產標籤，並遵循最小權限原則區分只讀收集器與狀態變更控制器。
- **離線（Air-gapped）部署支援**：透過 DGX Spark Custom Installation 與 Cloud-Init，IT 團隊可在設備首次啟動前預先配置軟體，支援純內網環境，無需額外自建基礎設施。

## 結論
NVIDIA DGX Spark 企業級管理功能將 AI 基礎設施的運營標準提升至企業級水準，讓 IT 團隊能以熟悉的工具和流程，安全、可靠地管理大規模 AI 系統的生命週期，無論是線上還是完全離線的部署環境皆適用。
