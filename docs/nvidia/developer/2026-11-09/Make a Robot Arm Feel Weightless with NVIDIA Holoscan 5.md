# Make a Robot Arm Feel Weightless with NVIDIA Holoscan 5

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-09
- **原文連結**: https://developer.nvidia.com/blog/make-a-robot-arm-feel-weightless-with-nvidia-holoscan-5/

## 核心主題
這篇文章介紹如何使用 NVIDIA Holoscan 5 建立一個重力補償迴路，讓機器人手臂感覺無重，並展示其低延遲控制和高吞吐量感知的能力。

## 關鍵重點
- 使用三個自訂 Holoscan 操作員（JointStateSourceOp、PinocchioGravityOp、MotorCommandSinkOp）建立 400 Hz 的重力補償迴路
- 利用 Pinocchio 進行逆動力學計算，並通過 motorbridge 庫向 Seeed Studio reBot Arm B601-DM 發送力矩指令
- Holoscan 的 partition 機制將操作員分組在同一線程執行，避免跨線程交接，並使用 drop-oldest 隊列策略防止過時樣本累積
- 使用 Nsight Systems 和 NVTX 標註進行效能分析，將控制分區固定到 CPU 核心可將 p99.99 延遲降低約 5 倍（C++）或 9.6 倍（Python）

## 結論
這是一個實用的教學範例，展示了如何將 Holoscan 5 應用於實際的機器人控制場景，並提供了完整的 Python 和 C++ 實作代碼。

---