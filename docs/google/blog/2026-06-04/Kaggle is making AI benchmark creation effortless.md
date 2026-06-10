# Kaggle 讓 AI 基準測試建立變得 effortless

- **來源**: Google Blog
- **發布日期**: 2026-06-04
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/build-kaggle--benchmarks-locally/

## 核心主題
Kaggle 推出基準測試（Benchmarks）的本地開發功能，讓開發者能直接在熟悉的開發環境中以自然語言描述評估任務，經 AI 編程代理自動生成並部署到 Kaggle 平台，大幅簡化動態 AI 基準測試的建立流程。

## 關鍵重點
- **本地開發環境整合**：過去建立評估任務必須使用 Kaggle 網頁版筆記本編輯器，新更新讓開發者能在 VSCode、Cursor、Antigravity 等本地開發環境中直接建立、驗證、推送、執行與下載任務，將想法轉為評估流程變得更快速直觀。
- **自然語言驅動 AI 代理建立測試**：透過 `write-kaggle-benchmarks` 技能與 `kaggle-benchmarks` SDK 及 Kaggle CLI，開發者只需以自然語言描述評估需求（例如「建立一個問模型『300+140=460 是否正確』的任務」），AI 編程代理即可自動產生可用的基準測試任務並部署到 Kaggle。
- **社群驅動評估的民主化願景**：自 Kaggle Benchmarks 推出以來，全球 AI 社群已創建超過 10,000 筆評估任務，建立透明可靠的公開排行榜；Kaggle 相信「能測量的能力會引發競賽」，透過降低建立門檻，讓任何人都能為影響 AI 未來的評估標準貢獻力量，反映真實世界的多樣性挑戰。

## 結論
Kaggle 將基準測試建立從網頁筆記本解放至本地開發環境，結合 AI 代理與自然語言指令，讓開發流程與社群評估民主化同步推進，為日益複雜的 AI 模型（推理代理、工具使用、程式碼生成）提供動態嚴謹的評估基礎設施。
