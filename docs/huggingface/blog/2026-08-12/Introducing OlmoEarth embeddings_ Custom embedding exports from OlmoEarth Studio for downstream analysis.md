# Introducing OlmoEarth embeddings: Custom embedding exports from OlmoEarth Studio for downstream analysis

- **來源**: Hugging Face Blog
- **發布日期**: 2026-08-12
- **原文連結**: https://huggingface.co/blog/allenai/olmoearth-embeddings

## 核心主題
OlmoEarth Studio 平台現在支援計算和導出嵌入向量，這些是地球觀測數據的緊湐數值表示，可支援多種下游任務。

## 關鍵重點
- 嵌入向量可支援相似性搜尋、分割和無監督探索等任務，相似的地表特徵會產生相似的向量
- 提供三種編碼器變體（Nano、Tiny、Base），可根據需求選擇不同參數規模的模型
- 輸出為輕量化的 Cloud-Optimized GeoTIFF (COG) 格式，可與 QGIS、GDAL、rasterio 等地理空間工具兼容
- 支援自適應計算，可根據用戶需求生成特定區域和時間範圍的嵌入，而非從預計算的全球存儲庫中獲取
- 可進行相似性搜尋、少樣本分割、變化檢測和主成分分析等應用，無需訓練數據或標籤即可實現

## 結論
OlmoEarth 嵌入為地球觀測數據提供了快速、成本效益高的入口點，可通過簡單的 Python 代碼實現多種分析任務，並支援更高性能的自適應微調。

---