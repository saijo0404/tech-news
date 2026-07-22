# Setting a World Record for MoE Pre-Training on NVIDIA GB300 NVL72

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-21
- **原文連結**: https://developer.nvidia.com/blog/setting-a-world-record-for-moe-pre-training-on-nvidia-gb300-nvl72/

## 核心主題
NVIDIA GB300 NVL72 在預訓練 DeepSeek-V3 671B 模型時創下世界紀錄，達到每 GPU 1,648 TFLOPs，展現了硬體、通訊與軟體全平台協同設計的強大效能。

## 關鍵重點
- **世界紀錄突破**：使用 256 GPU 在 DeepSeek-V3 671B 模型預訓練中，GB300 NVL72 平台達到每 GPU 1,648 TFLOPs，相比前代 GB200 NVL72 提升 3 倍。
- **MoE 架構挑戰**：混合專家（MoE）架構透過全網格通訊模式進行訓練，通訊效率成為關鍵限制因素，需要低延遲、高頻寬的通訊架構。
- **第五代 NVLink 技術**：提供每 GPU 1.8 TB/s 頻寬和 130 TB/s 非阻塞所有到所有頻寬，確保 GPU 間通訊在單一跳數內完成。
- **軟體優化成果**：Megatron Core、TorchTitan 和 JAX 框架的優化帶來 3-10 倍效能提升，從 256 到 1,024 GPU 擴展時仍能保持 97% 以上的每 GPU 吞吐量。
- **全平台協同設計**：從矽晶片到網路到軟體的完整優化，使訓練效率持續提升，即使硬體不變，軟體優化也能帶來顯著性能增長。

## 結論
NVIDIA GB300 NVL72 平台透過硬體、通訊與軟體的全方位優化，成功在 MoE 架構預訓練中創下世界紀錄。這不僅證明協同設計的重要性，也顯示軟體持續優化能帶來顯著性能提升，為未來更大規模模型訓練奠定基礎。

---