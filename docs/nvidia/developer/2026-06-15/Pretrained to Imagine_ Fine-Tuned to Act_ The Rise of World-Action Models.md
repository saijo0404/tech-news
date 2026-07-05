# Pretrained to Imagine, Fine-Tuned to Act: The Rise of World-Action Models

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-06-15
- **原文連結**: https://developer.nvidia.com/blog/pretrained-to-imagine-fine-tuned-to-act-the-rise-of-world-action-models/

## 核心主題
本文系統性探討機器人基礎模型領域的兩大競爭範式——VLM 基礎的 VLA 與影片基礎的 WAM（World-Action Model），整理 WAM 的設計空間、訓練成本、推論速度與長期趨勢，預測兩者最終將融合為更強大的混合架構。

## 關鍵重點
- **WAM 的核心思路與設計空間**：VLA 面臨「語言到動作錨定差距」瓶頸，WAM 則利用預訓練影片模型的先驗知識——影片模型已在文字條件下學習過場景如何隨時間變化（包含人手伸縮、工具操作等有意義的行為），從而縮小從視覺到動作的學習差距。WAM 的三大設計維度包括預測範式（逆向動力學、聯合預測、純表示學習）、動作整合方式（動作 Token、動作即影像、潛在動作與計畫）與架構風格（分層、單一巨型 Transformer、MoT 混合架構），代表性工作包括 UniPi、DreamZero、LingBot-VA、Being-H0.7 等。
- **訓練成本與推論速度的實務挑戰**：WAM 需要預測約比 VLA 長 10 倍的影片潛在序列，訓練成本大幅上升——DreamZero 風格微調約 8.6–9.0 ZFLOPs，加上完整影片預訓練可達 51 ZFLOPs（對比 VLA Foundry 的 6.9 ZFLOPs 差距約 7.4 倍）。推論速度方面，WAM 每動作區塊需 590–800 毫秒，比 Pi-0.5 的 190 毫秒慢 3–4 倍。WAM 快速興起的关键在於 DiT 基底影片模型（Wan、Cosmos）開源可用，大幅降低了早期 WAM 需從頭訓練 CNN 的門檻。
- **融合路線已經出現**：最新研究顯示兩大路線正在 convergence——VLA 開始使用世界模型改善目標跟隨（如 Pi-0.7 的 BAGEL 世界模型生成視覺子目標），WAM 則借鑑 VLA 的 MoT 配方。Being-H0.7 結合 V-JEPA2.1 視覺編碼器與 Play-LMP 風格潛在介面；Sereact 的 Cortex 2.0 在產業部署中引入 WAM 式 foresight 作為規劃層。作者預測最終勝出方案可能是 VLA 與 WAM 的混合架構，或第四條路徑——機器人第一基礎模型（RFFM）。

## 結論
WAM 代表了一個值得押注的新方向：以影片世界模型的時空理解能力為先驗，再微調為可靠的機器人控制政策。目前兩大範式各有所長——VLA 訓練便宜、推論快但受困於語言錨定差距；WAM 利用影片先驗可縮小此差距、在模擬環境中展現強大魯棒性，但成本高昂且推論緩慢。未來最有潛力的方案很可能不是純 VLA 或純 WAM，而是融合兩者的混合架構。關鍵挑戰在於計算成本與尚未明確的「哪些設計要素對機器人最重要」。

---
