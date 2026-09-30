# Graph Workflows in ADK: Everything You Need to Know

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-09-30
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/graph-workflows-in-adk-everything-you-need-to-know/

## 核心主題
這篇文章介紹了如何使用 Google 的 Agent Development Kit (ADK) 構建圖形化工作流 (Graph Workflows)，透過退款流程範例說明如何實現並行執行、路由決策、人工介入暫停以及批量處理等功能。

## 關鍵重點
- **節點與邊設計**: 將任務分解為節點 (nodes)，用邊 (edges) 連接，決定由程式碼、模型或人員控制下一步
- **Fan-out 與 Fan-in**: 並行執行獨立步驟，然後匯總結果再繼續
- **兩種路由器**: 確定性路由器 (基於規則) 與代理路由器 (基於模型解讀需求)
- **人工介入暫停**: 當需要人工審查時，工作流會暫停並等待回覆
- **並行工作員**: 使用 parallel_worker=True 對批量案例應用同一個節點
- **動態編排**: 讓 Python 根據結果動態決定下一步執行

## 結論
ADK 提供了靈活的圖形工作流框架，開發者可以根據需求選擇靜態圖形或讓 Python 動態決定下一步執行，實現從單一案例到批量處理的完整自動化流程。

---