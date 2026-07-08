# Run AI workloads on any cloud, store on Hugging Face: zero-egress storage with SkyPilot

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-07
- **原文連結**: https://huggingface.co/blog/skypilot-hf-storage

## 核心主題
Hugging Face 與 SkyPilot 合作，讓 AI 工作負載可以在任何雲端運行，而資料始終儲存在 Hugging Face Hub，消除跨雲端資料傳輸費用。

## 關鍵重點
- 使用 `hf://` URL 將 Hugging Face Bucket 或 Hub 倉庫直接掛載到 SkyPilot 任務中，支援 MOUNT（緩存模式）和 COPY（完整下載）兩種模式
- Hugging Face Storage 無輸出流量（egress）費用，無論 GPU 在哪個雲端，讀取資料都免費，解決跨雲端資料傳輸成本問題
- Xet 儲存引擎支援內容定義的區塊化與去重，自動優化檢查點與模型變體的儲存與傳輸，大幅降低儲存空間與傳輸成本
- 單一 HF_TOKEN 即可在所有雲端（AWS、GCP、Azure、Lambda、Nebius 等）使用，無需管理多個雲端倉庫金鑰

## 結論
這項技術讓 AI 團隊不再受資料儲存位置的限制，可以靈活使用任何雲端的 GPU 資源（包括 AWS、GCP、Lambda 等），同時大幅降低跨雲端資料傳輸的成本。檢查點與模型變體的 Xet 去重機制進一步提升了儲存效率。

---

## 技術實作範例
```yaml
# qwen-sft.yaml
resources:
  accelerators: H100:1

file_mounts:
  /base-model:
    source: hf://Qwen/Qwen3.5-4B
    store: hf
    mode: MOUNT  # 讀取-only，懶加載
  
  /checkpoints:
    source: hf://buckets/my-org/qwen-sft
    store: hf
    mode: MOUNT  # 讀寫檢查點

run:
  python train.py --model /base-model --output_dir /checkpoints
```

## 主要優勢
- **零輸出流量費用**：Hugging Face 儲存不收取 egress 費用，從任何雲端讀取資料都免費
- **靈活性**：SkyPilot 自動將工作負載分配到有 GPU 資源的雲端
- **去重優化**：Xet 儲存引擎自動識別重複區塊，減少儲存空間與傳輸量
- **單一認證**：使用現有 HF_TOKEN，無需管理多個雲端倉庫金鑰
- **即時訓練**：懶加載機制讓 GPU 立即開始訓練，無需等待完整資料下載

## 性能測試結果
- 模型加載速度：~500 MB/s（30 秒內完成）
- 檢查點寫入速度：AWS L40S ~168 MB/s，GCP L4 ~123 MB/s，Lambda H100 ~112 MB/s
- 8.43 GB 檢查點重上傳：僅需 8 秒（首次上傳需 24 秒）

## 開始使用
```bash
pip install "skypilot[huggingface]"
hf auth login  # 或 export HF_TOKEN=<your-token>
```