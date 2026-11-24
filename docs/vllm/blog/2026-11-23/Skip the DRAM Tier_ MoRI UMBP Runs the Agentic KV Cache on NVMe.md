# Skip the DRAM Tier - MoRI UMBP Runs the Agentic KV Cache on NVMe

- **來源**: vllm.ai
- **發布日期**: 2026-11-23
- **原文連結**: https://vllm.ai/blog/2026-11-23-skip-the-dram-tier

## 核心主題
vLLM 在 AMD Instinct MI355X GPU 上測試顯示，1.8 TB NVMe KV 池與 DRAM KV 池在吞吐量上幾乎相同，即使沒有 DRAM 緩存層。

## 關鍵重點
- 1.8 TB NVMe KV 池與 DRAM KV 池吞吐量差異在 1% 以內，即使沒有 DRAM 緩存層
- NVMe 池成本更低：$59,000 即可支撐一天 KV 寫入（DRAM 需 $76,000 僅存 31 分鐘）
- 小檔案段（256 MiB）可提升 NVMe 池效能，從 DRAM 池的 12.8% 落後提升至 0.8% 領先
- 使用 touch 機制可提升吞吐量 2.1%~3.9%
- 70 會話配置下，NVMe 池性能略高於 DRAM 池（+0.8%）
- DeepSeek-V4-Pro 使用視窗檢查點後，KV 緩存命中率從 78.4% 提升至 89.9%
- 96 個會話時，64 GB DRAM 寫入緩存可確保 NVMe 與 DRAM 表現一致

## 結論
在 AMD MoRI 的 UMBP 庫架構下，使用 NVMe SSD 儲存 KV 緩存可大幅降低成本，同時保持與 DRAM 緩存相當的效能，特別適合高流量場景。

---