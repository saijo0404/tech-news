# Boost Inference Performance up to 15x on NVIDIA Blackwell Using DFlash Speculative Decoding

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://developer.nvidia.com/blog/boost-inference-performance-up-to-15x-on-nvidia-blackwell-using-dflash-speculative-decoding/

## 核心主題
NVIDIA 介紹 DFlash——一款專為推論加速設計的開源輕量級區塊擴散模型，透過區塊平行草稿取代傳統自回歸單詞生成，在 NVIDIA Blackwell 平台上將 gpt-oss-120b 推論效能提升高達 15 倍，且已整合至 vLLM、SGLang 與 TensorRT-LLM，開發者無需重構程式碼即可部署。

## 關鍵重點
- **區塊擴散草稿帶來 15 倍效能躍升**：DFlash 以區塊擴散草稿器取代傳統自回歸草稿模型，可在單一前向傳遞中平行預測多個未來 token，將循序草稿轉換為平行 GPU 工作。在八張 NVIDIA DGX B300 上運行 gpt-oss-120b 的測試中，於 500-600 tokens/sec 的高互動性範圍內，DFlash 相較自回歸解碼提升超過 15 倍吞吐量，較 EAGLE-3 推論解碼提升 1.5 倍。Blackwell Ultra 的 15 PFLOPS NVFP4 密集運算完美匹配 DFlash 的平行工作負載，可在相同互動率下服務高達 15 倍用戶。
- **多模型與框架支援，無縫整合**：研究團隊已在 Hugging Face 發布 20 個 DFlash 權重檢查點，涵蓋 Qwen、Kimi K2.6、Llama、Gemma 與 gpt-oss 等模型家族。在 vLLM 中，開發者僅需替換 EAGLE-3 檢查點與更新設定即可使用 DFlash（Gemma 4 31B 於單張 Blackwell Ultra 上吞吐量提升高達 5.8 倍）；在 SGLang 中，將草稿模型替換為 DFlash 檢查點即可（Qwen3-8B 於單張 B200 上吞吐量提升高達 5.1 倍），無需任何應用程式重構。
- **DFlash 三大核心技術**：（1）區塊擴散草稿（Block-diffusion drafting）——平行預測多個未來 token；（2）目標模型隱藏狀態條件化（Target hidden-state conditioning）——草稿器使用從目標模型提取的上下文特徵；（3）KV 注入（KV injection）——將目標上下文特徵注入草稿模型的各層 KV 投影，維持高接受率。這三者結合使草稿器兼具速度與效果，同時保留目標模型的輸出分佈品質。

## 結論
DFlash 將推論解碼中的草稿階段從循序推進至平行，充分發揮 Blackwell 架構的平行運算潛力——在相同互動延遲下大幅提升吞吐量，或在相同吞吐量下提供更低的延遲。透過與 vLLM、SGLang 與 TensorRT-LLM 的深度整合，以及 Hugging Face 上多模型檢查點的快速開放，NVIDIA 生態系讓開發者能零門檻引入這項推論優化，為代理式 AI、程式碼生成與多語言推理等低延遲場景提供強大的效能基礎。

---
