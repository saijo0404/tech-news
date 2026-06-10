# 金融機構為何集體轉向交易基礎模型，打造專屬智慧

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://blogs.nvidia.com/blog/financial-institutions-transaction-foundation-models/

## 核心主題
金融機構正從過去各自為政的專用模型，轉向基於 Transformer 的交易基礎模型，以統一、上下文感知的方式學習消費者金融行為，打破資料孤島並提升反詐、授信與推薦等任務的整體效能。

## 關鍵重點
- **從專用模型到統一基礎模型的架構轉型**：傳統統計與機器學習模型各自孤立，無法建立消費者金融行為的統一理解；交易基礎模型在數百億筆金融事件（付款、轉帳、產品互動、行為訊號）上訓練，將表格化資料轉為語意嵌入，以時間、裝置、地點與先前活動等上下文脈絡解釋行為，取代繁瑣的人工特徵工程。
- **業界領先者已取得顯著成果**：Revolut 以 NVIDIA Hopper GPU、cuDF 與 Nemotron 在 Nebius 雲端訓練 PRAGMA 模型（涵蓋 240 億事件、2600 萬用戶），在授信評分、反詐與推薦上全面超越專用模型且零特徵工程；Mastercard 訓練私有大型表格基礎模型，早期測試顯示在資安、反詐、忠誠度與投資組合最佳化表現優於傳統 ML；Adyen 處理 1 兆美元付款，0.1% 授權率提升即帶來巨大 GMV 增量；Stripe 全年阻擋近 1,120 億美元詐欺並降低 38% 詐欺率。
- **生態系與開發工具加速普及**：NVIDIA 發布「Build Your Own Transaction Foundation Model」開發者範例，可在 AWS SageMaker HyperPod 與 Nebius AI Cloud 上部署；服務夥伴 EXL（EXLerate.ai 平台）、Thoughtworks、GFT（Wynxx 代理 AI 平台與 Smaragd 合規引擎）正將此架構整合至授信風險、合規反詐與付款 servicing 等企業級場景。

## 結論
交易資料是金融機構無法被競爭對手複製的私有資產，結合已驗證的 Transformer 架構與 NVIDIA 加速運算生態系，交易基礎模型正成為金融業下一代代理式商務的智慧核心，讓機構能從孤立模型時代邁向統一、可擴展的企業級 AI 營運模式。
