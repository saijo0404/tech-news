# Mapping global methane emissions from space with deep learning

- **來源**: Google Research Blog
- **發布日期**: 2026-09-01
- **原文連結**: https://research.google/blog/mapping-global-methane-emissions-from-space-with-deep-learning/

## 核心主題
Google 與 NASA JPL 合作開發的 MAPL-EMIT 深度學習框架，利用太空衛星數據實現全球甲烷洩漏的自動檢測、量化與來源定位，為氣候行動提供可擴展的工具。

## 關鍵重點
- **深度學習框架**：MAPL-EMIT 使用視覺 Transformer 架構，能同時進行增強量化、氣流描繪與來源定位，解決傳統方法難以處理複雜場景的問題。
- **高精準度檢測**：在專家標註的甲烷氣流上達到 84% 召回率，比現有匹配濾波方法具有更高的信噪比，能識別更多潛在洩漏來源。
- **合成數據訓練**：由於缺乏百萬級真實甲烷氣流數據，團隊開發物理模擬框架生成 360 萬個合成氣流，使模型能適應多樣化的天氣與地理條件。
- **全球數據共享**：提供全球氣流數據庫（Earth Engine）、訓練模型（Kaggle）、合成氣流數據集與推論庫（GitHub），讓科學界可自由使用。
- **實際應用驗證**：成功追蹤全球 25 大垃圾場中的 24 個，並能識別更多微弱洩漏信號，提升檢測靈敏度。

## 結論
這項研究填補了太空甲烷監測的重要缺口，為政策制定者、研究人員與產業提供即時、可操作的排放追蹤工具，加速全球減溫目標的實現。

---