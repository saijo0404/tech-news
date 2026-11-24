# RoboTrack: Point tracking for real-world robotic manipulation

- **來源**: Hugging Face
- **發布日期**: 2026-11-23
- **原文連結**: https://huggingface.co/blog/allenai/robotrack

## 核心主題
本文介紹了 RoboTrack 基准测试和训练数据集，用于现实世界机器人操作中的点跟踪，并发布了两个新的点跟踪模型以改进跟踪性能。

## 關鍵重點
- **RoboTrack-Bench** 包含 307 个视频，来自 DROID、Ego-Exo4D、MolmoAct 2 和 EgoVerse，涵盖不同的机器人和人手操作，以及杂乱场景和第一人称/第三人称视角，总共有 2,522 个经人工验证的点跟踪轨迹。
- **现有跟踪器在 RoboTrack-Bench 上的表现显著低于现有机器人基准测试**，表明现有基准测试不能完全反映现实世界操作中的跟踪性能，所有评估的跟踪器在 RoboTrack-Bench 上的分数都比在 RoboTAP 上低 3.0 到 6.6 个平均 Jaccard (AJ) 分数。
- **RoboTrack-15M 合成训练数据集** 基于 Ai2 的 MolmoSpaces 机器人模拟环境生成，包含 3,000 个视频、1500 万条跟踪轨迹，专注于机器人抓取和移动物体的交互，训练使用该数据集的跟踪器可以显著改进在现实世界操作视频上的性能。
- **发布了两个新模型**：RoboTracker（基于 AllTracker 微调）和 RoboTracker-Warp（基于 CoWTracker 训练），其中 RoboTracker-Warp 在五个基准测试中的四个达到最先进水平，平均 AJ 分数提升了 2.1。
- **实际应用**：团队在真实机器人上部署了点跟踪系统，用于指导湿实验室任务中的移液器操作，展示了点跟踪在现实世界机器人操作中的实用价值。

## 結論
RoboTrack 项目通过创建更真实的基准测试数据集和改进的跟踪模型，显著提升了现实世界机器人操作中的点跟踪性能，为机器人感知和规划提供了更可靠的工具，同时也揭示了现有基准测试在评估现实世界操作能力方面的局限性。
---
