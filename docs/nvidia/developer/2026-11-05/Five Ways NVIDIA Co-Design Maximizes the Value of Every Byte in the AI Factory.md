# Five Ways NVIDIA Co-Design Maximizes the Value of Every Byte in the AI Factory

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-05
- **原文連結**: https://developer.nvidia.com/blog/five-ways-nvidia-co-design-maximizes-the-value-of-every-byte-in-the-ai-factory/

## 核心主題
NVIDIA 透過五項協同設計（NVFP4、Wide Expert Parallelism、NVIDIA Dynamo、Vera CPU、CMX 儲存層）最大化 AI 工廠中每個字元的價值，使 Vera Rubin NVL72 相比 GB300 NVL72 提升 30 倍效能。

## 關鍵重點
- **NVFP4 量化格式**：將模型記憶體 footprint 減少 3.5 倍（相比 FP16）和 1.8 倍（相比 FP8），同時保留精度，並可將 KV cache 減少最多 50%。
- **Wide Expert Parallelism**：將專家權重分散到 8 個以上 GPU，提升記憶體效率與計算強度，使 GB300 NVL72 相比 H200 NVL8 提升 10 倍效能。
- **NVIDIA Dynamo**：將 KV cache 視為 fleet-wide 資源，透過 KV-aware routing、disaggregated serving 和 KV Cache Runner 實現跨 GPU/CPU/儲存層的優化。
- **Vera CPU**：提供 88 個 Olympus 核心，單線程性能快 1.8 倍，並提供 1.5TB LPDDR5X 記憶體，可階段化閒置的 KV cache。
- **NVIDIA CMX**：新增 pod 級 G3.5 儲存層，基於 BlueField-4 STX、Spectrum-X、DOCA Memos 和 Dynamo 整合，可在節點間共享和重疊 KV cache。

## 結論
透過這五項協同設計，Vera Rubin NVL72 在相同 288GB GPU 記憶體下，實現每兆瓦 30 倍的吞吐量提升，證明記憶體效率的提升比單純增加容量更能提升 AI 工廠的效能。

---