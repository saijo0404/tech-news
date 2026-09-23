# Turn Your Latest Observations Into Timely Weather Decisions With NVIDIA Earth-2

- **來源**: developer.nvidia.com
- **發布日期**: 2026-09-21
- **原文連結**: https://developer.nvidia.com/blog/turn-your-latest-observations-into-timely-weather-decisions-with-nvidia-earth-2/

## 核心主題
NVIDIA Earth-2 利用 AI 資料同化工具處理觀察數據，發布更頻繁且與即時狀況一致的預報，幫助能源、風險管理等產業做出更及時的天氣決策。

## 關鍵重點
- **Score-Based Data Assimilation (SDA)**：利用 CorrDiff 和 StormCast 擴散模型的約束式資料同化，風速 RMSE 分別降低 54% 和平均 7.2%，無需重新訓練即可納入觀察數據
- **HealDA 技術**：可在數秒內估算全球大氣狀態，使用觀察編碼器和視覺 Transformer 背骨，將異質遙感與原位觀察數據映射至 1° HEALPix 網格
- **Earth2Studio 平台**：提供預訓練的全球數據同化模型（CorrDiff 歐洲版、StormCast 美國版），整合多源觀測數據（微波探測器、無線電隱沒、地面站、飛機、浮標等），支援 1° HEALPix 網格
- **應用場景**：能源管理（風力/太陽能資產）、緊急管理（雷達與本地感測器）、衛星提供商、資本市場、保險、農業、物流等領域

## 結論
NVIDIA Earth-2 通過 AI 資料同化工具，使能源、風險管理等產業能獲得更具準確性與時效性的預報，加速太陽能採集、冷卻過程及水庫入流等預測，並可透過 Earth2Studio 平台快速部署自訂觀察數據和區域性預報模型。
---