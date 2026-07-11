# 加速端到端共摺疊性能：NVIDIA BioNeMo Agent Toolkit

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-10
- **原文連結**: https://developer.nvidia.com/blog/accelerating-end-to-end-co-folding-performance-with-nvidia-bionemo-agent-toolkit/

## 核心主題
本文介紹了 NVIDIA BioNeMo Agent Toolkit 如何透過 GPU 加速工具（MMseqs2-GPU、cuEquivariance、OpenFold3 NIM、Fold-CP）來加速生物分子結構預測和共摺疊流程，提升速度、減少記憶體需求，並支援更大規模的分子組裝預測。

## 關鍵重點
- **MSA Search NIM**: 將多序列對齊（MSA）生成從 CPU 移至 GPU，速度提升達 177 倍，大幅縮短同源性搜尋時間。
- **cuEquivariance 與 OpenFold3 NIM**: 透過 cuEquivariance 將摺疊推理時間減少 3 倍，並擴展序列長度至約 6,400 tokens，支援更長序列的預測。
- **Fold-CP**: 引入上下文並行推理，將記憶體需求降至 O(N²/P)，支援 64 張 B300 GPU 處理 32,000 tokens 的複雜組裝，突破單一 GPU 記憶體限制。

## 結論
這些工具使結構預測更快、更可擴展，並使以前無法處理的結構生物學問題（如核糖體規模的複雜體）變得可行，加速藥物發現和蛋白質設計，讓研究者能從模型預測轉化為更具用的生物學系統。

---

檔案已成功儲存至指定路徑。
