# NVIDIA Cosmos3-H-Dreams: Bringing Clinical Surgery to Life Through Generative Simulation

- **來源**: Hugging Face
- **發布日期**: 2026-10-20
- **原文連結**: https://huggingface.co/blog/nvidia/cosmos3-h-dreams

## 核心主題
NVIDIA Cosmos3-H-Dreams 是基於 Cosmos 3 和 FlashDreams 的即時生成式手術模擬器，首次將臨床膽囊切除手術的複雜場景帶入生成式模擬，實現了高度逼真的體內影像。

## 關鍵重點
- **從桌面任務到臨床場景**：Cosmos3-H-Dreams 專為臨床膽囊切除手術設計，能處理複雜的解剖結構、組織運動和遮擋，相比之前的桌面suturing任務有了重大突破。
- **教師到學生的訓練流程**：使用 Cosmos 3 基礎模型（160 億參數），通過教師到學生的訓練流程，將雙向教師模型轉化為因果學生模型，並使用 Self-Forcing 技術減少錯誤累積。
- **FlashDreams 加速**：使用 NVIDIA 的 FlashDreams 加速庫，可在單一 NVIDIA RTX PRO 6000 GPU 上實現即時運行，支持 28 個動作維度（姿勢、夾爪、能量控制等）。
- **支持未見軌跡**：能生成不同膽囊切除場景，適應不同的手術動作序列，即使面對未見過的動作也能產生物理準確的組織變形。
- **可自適應**：可根據自己的數據集和控制器進行訓練和調整，提供完整的教師微調和 Self-Forcing 蒸馏指南。

## 結論
Cosmos3-H-Dreams 是研究模擬器，而非經過驗證的臨床系統，但為研究手術互動提供了更真實的環境基礎。未來研究方向包括完整程序建模、結合數值模擬、與外科醫生評估、支持更多器械以及開發自主手術策略。

---

檔案已成功儲存至指定路徑。