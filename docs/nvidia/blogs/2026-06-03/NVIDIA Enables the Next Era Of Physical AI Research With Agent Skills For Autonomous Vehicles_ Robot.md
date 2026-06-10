# NVIDIA 以代理技能為自動駕駛、機器人與視覺 AI 研發開啟具身 AI 新時代

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-03
- **原文連結**: https://blogs.nvidia.com/blog/cvpr-physical-ai-research-agent-skills/

## 核心主題
NVIDIA 在 CVPR 2026 公布全新「具身 AI 代理技能」（Physical AI Agent Skills），搭配 Cosmos 3 基礎模型與 Isaac 生態系，將分散的物理 AI 研究工作流程（場景重建、邊際案例生成、政策訓練、行為評估）整合為端到端自動化流程，加速自動駕駛、機器人與視覺 AI 系統研發。

## 關鍵重點
- **自動駕駛研究突破：Neural Reconstruction 將車隊資料轉為 3D 模擬場景，Alpamayo 2 Super 32B 推理 VLA 模型推升 Level 4 發展**：針對 AV 研究「長尾問題」（稀有互動、特殊路況幾何、光照變化、邊緣行為），NVIDIA 推出自動駕駛代理技能——Neural Reconstruction 將車隊收集資料轉為可編輯 3D 場景供模擬與合成數據使用，結合 Omniverse NuRec、InstantNuRec、Harmonizer 與 HiGS 渲染器加速重建與提升場景真實感；AlpaGym 開源閉環強化學習框架連接政策推展與高保真模擬，跨數千 GPU 擴展；OmniDreams 動作條件生成世界模型為模擬環路增添照片級真實渲染；NVIDIA 同時發布最強大的開放駕駛基礎模型 Alpamayo 2 Super（32B 參數推理視覺語言動作模型），涵蓋完整駕駛堆疊的推理、規劃與行動，推升 L4 級別開發與部署。
- **視覺 AI 系統革新：Delta 缺陷影像生成技能結合 Cosmos 3 MoT 架構，VSS Blueprint 從海量影片萃取洞察**：視覺 AI 研究瓶頸在於缺乏足夠受控範例來研究視覺條件、物體狀態或時間事件變化時模型的行為；NVIDIA 推出全新 Metropolis 代理技能——Defect Image Generation 使用真實影像在不同表面上建立不同缺陷範例，結合 Isaac Sim、Cosmos 3 與 OSMO 進行調度與視覺語言推理，讓研究者建立罕見視覺案例並評估模型是否正確回應；針對影片 AI 代理，VSS Blueprint（影片搜尋與摘要）、TAO 與 Video Augmentation 技能幫助從海量影片資料萃取洞察、微調模型與自動化建構 - 評估迴圈，讓研究者開發能偵測事件、推理複雜場景、摘要活動並發送警報的推理視覺 AI 代理。
- **機器人學習擴展：Isaac Sim 6.0 代理友好技能自動化場景準備、模擬與學習全流程，Cosmos-H-Surgical-Simulator 推進醫療機器人研究**：機器人技能教學取決於迭代，研究瓶頸在於建構足夠受控環境與政策推展以理解行為變化；NVIDIA 機器人技能讓 AI 代理自動化大部分常見開發步驟——從場景準備、模擬到機器人學習，涵蓋 Isaac Sim 中的場景建構、模擬控制、資料捕捉與環境驗證，以及 Isaac Lab 中的強化學習設定、訓練、評估與自訂環境開發；Isaac mobility skills 支援從場景搜尋、USD 轉換、環境註冊到殘差強化學習與政策評估的完整導航工作流；Cosmos-H-Surgical-Simulator 透過從真實外科數據直接學習而非手動工程物理模型，生成真實外科機器人數據，縮小 sim-to-real 差距；物理 AI 資料集在 Hugging Face 已突破 1,500 萬次下載，GRAIL 資料集包含約 50 小時人型物體互動數據。

## 結論
NVIDIA 的具身 AI 代理技能代表了物理 AI 研究從「分散工具拼貼」到「端到端自動化流程」的範式轉移——以代理（agent）驅動的工作流程取代研究人員手動串接模擬環境、任務變化、政策訓練與評估的繁瑣步驟，大幅加速從「模型能力」到「可擴展端到端工作流」的轉換；特別是搭配 Cosmos 3 基礎模型（全球首款全功能 omni 模型，統一視覺推理、世界生成與動作生成），NVIDIA 正在建構一個完整的物理 AI 研發生態系——從自動駕駛的 Neural Reconstruction 與 Alpamayo 2 Super、視覺 AI 的缺陷生成與 VSS 影片分析，到機器人的 Isaac Sim 6.0 自動化學習與 Cosmos-H-Surgical-Simulator 醫療外科模擬，所有技能均已透過 GitHub 開源提供，部分工具更可透過 NVIDIA Brev 的 Physical AI Launchables 直接在 H100 GPU 上即時試用；加上 CVPR 期間開放的 AI City Challenge、PAI-AV Reasoning Challenge 與 AlpaSim 閉環挑戰等基準測試，NVIDIA 正以「開放模型 + 開源技能 + 基準挑戰 + 海量資料集」四位一體的策略，重新定義具身 AI 研究的開發節奏。
