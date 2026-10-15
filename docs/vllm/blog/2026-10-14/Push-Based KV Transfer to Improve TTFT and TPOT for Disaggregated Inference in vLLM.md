# Push-Based KV Transfer to Improve TTFT and TPOT for Disaggregated Inference in vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-10-14
- **原文連結**: https://vllm.ai/blog/2026-10-14-nixl-push-connector

## 核心主題
vLLM 推出基於推送的 NIXL 連接器，通過將 KV 緩存轉移從預填充階段後移至背景線程，顯著降低首字延遲（TTFT）和每輸出 token 延遲（TPOT），特別是在高請求率下可提升 3 倍 TTFT 和 30% TPOT。

## 關鍵重點
- 推送模式將 decode 節點的目標區塊預先註冊，與 prefill 計算重疊，移除後置路由往返和 decode 側轉移設置
- 使用背景線程執行 NIXL 轉移設置，避免阻塞 decode 節點的延遲關鍵路徑
- 在 AWS EC2 P5en 實例上測試，Qwen3-32B 模型在 8 QPS 和 16k 輸入長度下，推送模式 TTFT 降至 540ms（相比拉取模式的 1,744ms 降低 3 倍），TPOT 降至 7ms（相比拉取模式的 10.4ms 降低 30%）

## 結論
推送模式適合需要早期 decode 節點選擇且優先降低 TTFT 的工作負載，而拉取模式則更適合需要雙向 KV 轉移或延遲 decode 節點選擇以實現負載感知路由的工作負載。
---

檔案已成功儲存至指定路徑。