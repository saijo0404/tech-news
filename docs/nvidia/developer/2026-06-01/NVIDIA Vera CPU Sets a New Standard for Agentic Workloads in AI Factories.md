# NVIDIA Vera CPU 為 AI 工廠的代理工作負載設立新標準

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-31
- **原文連結**: https://developer.nvidia.com/blog/nvidia-vera-cpu-sets-a-new-standard-for-agentic-workloads-in-ai-factories/

## 核心主題
NVIDIA Vera CPU 針對代理式 AI 與強化學習的 CPU 執行痛點，以自研 Olympus 核心、LPDDR5X 記憶體與 SCF 互連架構，打造高單核心效能、高併發與省電頻寬的 AI 工廠 CPU，將 AI 工廠的衡量指標從「每美元核心數」轉變為「每瓦每美元 AI 產量」。

## 關鍵重點
- **代理式 AI 讓 CPU 成為關鍵路徑**：代理模型在生成工具呼叫後，CPU 需執行沙盒程式碼、資料擷取、結果運算與排程協調；代理越強，多步驟請求的 CPU 執行時間越長，CPU 直接影響延遲、加速器利用率與整體產能。
- **Olympus 核心與記憶體子系統設計**：Olympus 核心提供比 Grace 高 50% 的 IPC，搭載神經分支預測器（維持每週期兩筆分支零懲罰）、10 寬解碼與深層亂序排程；LPDDR5X 記憶體提供高達 1.2 TB/s 頻寬且負載下維持 90% 峰值，圖遍歷工作負載效能比 x86 架構快 3 倍以上。
- **系統效率與能源效益**：搭配 SOCAMM LPDDR5X 記憶體，記憶體功耗低於 30 瓦（相較 DDR5 超過 100 瓦），TDP 設定 250-450W 可彈性調整；在滿載代理工作負載下，sandbox 效能比傳統 x86 架構高出 1.8 倍，同時降低運算與冷卻成本。

## 結論
Vera CPU 以「代理優先」的 CPU 設計理念，將高單核心效能、高併發執行與省電記憶體頻寬整合於單一架構，讓 AI 工廠能完成更多工具呼叫與評估循環，持續驅動加速器運轉，為代理式 AI 時代奠定堅實的基础設施基石。
