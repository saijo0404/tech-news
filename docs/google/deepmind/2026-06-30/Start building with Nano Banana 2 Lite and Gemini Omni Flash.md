---
# Start building with Nano Banana 2 Lite and Gemini Omni Flash

- **來源**: Google DeepMind Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://deepmind.google/blog/start-building-with-nano-banana-2-lite-and-gemini-omni-flash/

## 核心主題
Google DeepMind 推出兩款全新生成式媒體模型——**Nano Banana 2 Lite**（超高速、低成本的圖片生成模型）與 **Gemini Omni Flash**（高品質影片生成與對話式編輯模型），讓開發者能以更低的成本與更快的速度建立從圖片到影片的端到端多媒體體驗。

## 關鍵重點
- **Nano Banana 2 Lite：速度與成本優先的圖片模型**：作為 Nano Banana 系列中最快的圖片模型，Nano Banana 2 Lite（gemini-3.1-flash-lite-image）可在 **4 秒內**完成文字轉圖片，每 1K 解析度圖片僅需 **$0.034**。它保留了可靠的提示遵循力、強角色一致性與清晰的圖片內文字渲染，適合互動式原型與大量工作流程。Nano Banana 系列現有四款模型：Lite（速度優先）、2（品質/成本平衡）、Pro（專業級）、以及已建議升級的舊版 Nano。
- **Gemini Omni Flash：高品質影片生成與對話式編輯**：Omni Flash（gemini-omni-flash-preview）結合 Gemini 的多模態推理與影片生成能力，支援文字、圖片與影片的混合輸入，每 1 秒影片輸出價格為 **$0.10**（與 Veo 3.1 Fast 相同）。其亮點包括：對話式影片編輯（以自然語言修改影片）、多模態參考輸入、結合 Gemini 世界知識（歷史、生物、敘事邏輯）以及文字與動作同步。目前支援 10 秒影片生成，長時長功能即將推出。
- **模型串接與示範應用**：真正的魔力來自兩模型串接——以 Nano Banana 2 Lite 高速生成圖片，再作為參考輸入 Omni Flash 轉為動畫影片。示範應用包括：**Anywhere**（自拍轉為各地地標再動態化）、**Space Lift**（室內設計概念生成與動態展示）、**Omni Product Studio**（靜態商品圖轉 cinematic 商業影片）。兩模型均已開放於 Google AI Studio、Gemini API 與 Gemini Enterprise Agent Platform，並整合於 Google AI Mode、Gemini app、NotebookLM、Google Photos 等消費者產品。所有生成內容均使用 SynthID 數位浮水印。

## 結論
Nano Banana 2 Lite 與 Gemini Omni Flash 的同步推出，為生成式媒體開發提供了一條完整的「圖片生成 → 影片動畫 → 對話式編輯」管道——Lite 負責快速大量產出圖片，Omni Flash 負責高品質影片生成與編輯，兩者可透過 Interactions API 串接成最多三輪的互動式體驗。這不僅降低了多媒體創作的成本與門檻，更讓開發者能以前所未有的速度將創意從概念推送到產品。

---
