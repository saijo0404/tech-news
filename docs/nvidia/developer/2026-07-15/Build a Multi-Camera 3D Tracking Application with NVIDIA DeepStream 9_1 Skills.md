# Build a Multi-Camera 3D Tracking Application with NVIDIA DeepStream 9.1 Skills

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-15
- **原文連結**: https://developer.nvidia.com/blog/build-a-multi-camera-3d-tracking-application-with-nvidia-deepstream-9-1-skills/

## 核心主題
NVIDIA DeepStream 9.1 推出 AutoMagicCalib (AMC) 和 Multi-View 3D Tracking (MV3DT) 技能，自動化相機校準並實現跨多相機視角的物件追蹤，大幅簡化視覺 AI 管道開發。

## 關鍵重點
- **AutoMagicCalib (AMC)**：自動化相機校準流程，透過分析已追蹤物件的軌跡自動估算相機參數，減少手動設定時間與錯誤。
- **Multi-View 3D Tracking (MV3DT)**：將多個相機的檢測結果投射到共享 3D 座標系統，維持全域一致的物件 ID，支援 PeopleNetTransformer、PeopleNet v2.6.3 和 RT-DETR 2D 檢測模型。
- **13 個代理技能**：提供模組化技能系統，支援 Claude Code、Codex 等編碼代理，開發者只需透過自然語言指令即可部署多相機追蹤管道。
- **多形式輸出**：追蹤結果可透過螢幕顯示（OSD）、鳥瞰圖（BEV）和 Kafka 訊息輸出，支援下游應用整合。
- **邊緣裝置支援**：支援 NVIDIA JetPack 7.2，可在 Orin 和 Thor 等邊緣平台上加速視覺 AI 效能。

## 結論
DeepStream 9.1 透過自動化校準、模組化技能和自然語言部署，大幅降低多相機 3D 追蹤系統的開發門檻，適用於倉庫安全、零售分析與智慧建築等場景。完整程式碼與參考應用已開放於 NVIDIA DeepStream GitHub 倉庫。

---