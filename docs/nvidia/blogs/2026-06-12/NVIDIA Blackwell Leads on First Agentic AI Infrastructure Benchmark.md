# NVIDIA Blackwell 領先首個 AI 代理基礎設施效能基準測試

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-12
- **原文連結**: https://blogs.nvidia.com/blog/nvidia-blackwell-agentperf-artificial-analysis/

## 核心主題
Artificial Analysis 推出的 AgentPerf 是業界首個 AI 代理（Agentic AI）基準測試，首批結果顯示 NVIDIA Blackwell Ultra NVL72 平台在代理工作負載上表現最佳，每兆瓦可支援的代理數量比 NVIDIA Hopper 高出 20 倍。

## 關鍵重點
- **代理工作負載的獨特挑戰**：與單次對話式 AI 不同，AI 代理需要將目標拆解為多步驟，串接數十至數百次 LLM 呼叫與工具呼叫（如編譯、資料庫查詢、網頁瀏覽），且上下文逐步增長，這種「乘數效應」的複雜度使既有基準測試無法準確衡量代理效能。
- **AgentPerf 以真實代理軌跡為基礎**：基準測試基於來自 12 種以上程式語言的真實程式碼代理軌跡，模擬完整的代理工作流程（讀取檔案、編寫與編輯程式碼、執行指令並根據結果迭代），同時以代表性 CPU 處理時間模擬工具呼叫延遲，確保結果反映的是加速器運算效能而非 CPU 差異。
- **NVIDIA 全堆疊極致協同設計**：GB300 NVL72 將 72 張 GPU 連結為單一機架級系統，使 DeepSeek V4 Pro 等大型 MoE 模型能有效分散運算；CUDA 核心透過重疊通訊與運算吸收專家協調成本；TensorRT LLM 則在代理會話擴展時維持效率，搭配 Baseten、DeepInfra、Together AI 等生態夥伴已投入生產應用。

## 結論
AgentPerf 確立了代理 AI 基礎設施效能衡量的新標準，NVIDIA Blackwell 透過硬體與軟體的深度協同設計，為大規模代理部署提供前所未有的每瓦代理數量與整體效能，而即將量產的 Vera Rubin 架構將進一步擴展此一優勢。
