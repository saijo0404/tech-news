---
# Scaling Ray Serve LLM on GKE: Performance without losing the developer experience

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-18
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/improving-ray-serve-llm-on-gke-throughput-latency/

## 核心主題
Google 與 Anyscale 合作，透過三項架構優化將 Ray Serve LLM 在 GKE 上的效能大幅提升——提供高達 5 倍吞吐量和 8 倍更低的延遲，讓開發者能在不犧牲 Python 原生開發體驗的前提下，進行大規模分散式 LLM 推論部署。

## 關鍵重點
- **三大架構優化**：（1）HAProxy 整合——Ray Serve 內建 HAProxy 管理內部請求路由與負載平衡，大幅降低代理程式開銷並防止 Python 執行階段在高流量下飽和；（2）直接 Token 串流架構——將初始請求路徑與串流回傳解耦，Token 直接從模型複本串流回 Proxy，繞過入口路由器以降低延遲；（3）vLLM 的 v2 Ray 執行器後端——將 Ray 從資料平面移除以啟用非同步排程，統一與原生 vLLM 執行器的程式碼路徑，確保 Ray 使用者能享有最新引擎層級的優化。
- **GKE 效能基準測試結果**：與 Anyscale 在 GKE 集群（搭載 NVIDIA HGX B200 的 A4 VM）上進行測試，使用 Gemma 4 E2B 小型模型隔離編排與路由瓶頸。結果顯示：相比之前 Ray Serve 配置，吞吐量提升高達 5 倍、延遲改善 8 倍；在八個複本的分發集群上，擴展模式遠超前代性能，且表現與原生 vLLM 相當。
- **開發者體驗與靈活性的平衡**：Ray Serve 結合 GKE 提供從初始模型開發到線上生產部署的統一平台，透過上述優化，開發者不再需要為了效能犧牲 Python 原生 API 的易用性——Ray 提供的編排彈性、分散式能力與 GKE 的 Kubernetes 整合，讓開發者能以熟悉的開發流程達成企業級推論效能。

## 結論
Google 與 Anyscale 的聯合工程合作證明了「魚與熊掌可以兼得」——Ray Serve LLM 在 GKE 上達成的 5 倍吞吐量與 8 倍延遲改善，打破了以往靈活性與效能之間的取捨迷思，讓開發團隊能同時擁有開發者友善的 Python API 與符合生產環境嚴苛要求的分散式推論效能。

---
