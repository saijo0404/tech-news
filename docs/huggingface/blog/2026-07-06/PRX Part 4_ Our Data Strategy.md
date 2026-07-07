# PRX Part 4 - Our Data Strategy

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-06
- **原文連結**: https://huggingface.co/blog/Photoroom/prx-part4-data

## 核心主題
PRX 模型數據集構建策略與訓練流程優化

## 關鍵重點
- 數據集構建採用混合數據源策略，使用 Mosaic Streaming + MDS 分佈式訓練格式，JPEG 質量 92 儲存以節省空間
- 圖像描述採用 Qwen3-VL-8B 模型，在 GPU 上生成單段密集描述，平衡速度與品質
- 數據處理流程包含過濾 NSFW 內容、去重機制、分辨率分級等優化措施

## 結論
PRX 數據策略強調覆蓋度與多樣性，通過技術優化提升訓練品質與效率

---