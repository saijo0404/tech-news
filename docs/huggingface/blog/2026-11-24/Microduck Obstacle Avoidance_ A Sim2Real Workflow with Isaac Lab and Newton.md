# Microduck Obstacle Avoidance: A Sim2Real Workflow with Isaac Lab and Newton

- **來源**: Hugging Face
- **發布日期**: 2026-11-24
- **原文連結**: https://huggingface.co/blog/nvidia/microduck-obstacle-avoidance

## 核心主題
這篇文章介紹了一個完整的模擬到真實（Sim2Real）工作流程，展示如何使用 NVIDIA Isaac Lab 和 Newton 框架，為 Microduck 機器人訓練避障能力，並成功部署到真實機器人上。

## 關鍵重點
- **保留行走策略不變**：沿用原有的 Microduck 行走策略（backlash walking policy），只訓練一個專門的避障控制器，避免重新訓練平衡控制。
- **使用 SimReady 資產構建多樣化場景**：利用 Hugging Face 上的 SimReady 中央資產庫，下載紙箱、垃圾桶、床邊櫃等物件，自動生成各種障礙物佈局。
- **基於 ToF 感測器的避障訓練**：使用 Newton 的射線追蹤器模擬 VL53L5CX 時距測距感測器，訓練控制器根據感測數據調整速度命令以避開障礙物。
- **並行環境訓練與 ONNX 導出**：在 Isaac Lab 中進行大規模並行模擬訓練（最多 16,384 個環境），訓練完成後將策略導出為 ONNX 格式，方便部署。
- **真實機器人測試**：在真實 Microduck 機器人上進行測試，通過遊戲控制器發送避障指令，驗證策略在現實環境中的有效性。

## 結論
這個工作流程為開發者提供了一個可複製的框架，展示了如何將模擬訓練的機器人避障策略成功部署到真實機器人上。通過分離平衡控制和避障控制，並利用 Isaac Lab 的大規模並行訓練能力，可以高效地訓練出可靠的避障策略，為未來開發機器人避障能力提供了寶貴的參考。

---