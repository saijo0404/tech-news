# Securing AI at Enterprise Scale: The Google Kubernetes Engine Blueprint

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-07-17
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/securing-ai-at-enterprise-scale-the-google-kubernetes-engine-blueprint/

## 核心主題
這篇文章介紹了 Google Kubernetes Engine (GKE) 的 AI 工作載體安全藍圖，提供三層安全架構來保護大規模 AI 工作負載，幫助企業在 AI 生產化過程中建立安全基準。

## 關鍵重點
- **基礎設施層安全**：透過硬體驗證執行（Confidential GKE Nodes）保護敏感資料，包括對高績效加速器（如 NVIDIA H100 和 TPU）的記憶體加密與驗證能力，防止底層入侵。
- **模型安全**：整合 Google Cloud 供應鏈工具，使用 k8s-aibom（AI Bill of Materials for Kubernetes）生成模型、資料集和框架的全面清單，提供供應鏈可見性。
- **應用程式層防禦**：使用 Model Armor 檢查提示注入和敏感資料洩漏，GKE Inference Gateway 提供會話管理，以及 GKE Sandbox (gVisor) 提供安全隔離以執行 AI 代理。
- **三階段安全方法**：建議分階段實施安全策略，包括部署（基礎配置）、營運（強化措施）和治理（企業級自動化合規）。

## 結論
通過在 GKE 上構建並整合 Google Cloud，平台團隊可以繼承 Google 十多年來不斷完善的基礎設施安全基準，並配備專門的 AI 防禦措施，使 AI 部署不再是安全底線的競賽。

---