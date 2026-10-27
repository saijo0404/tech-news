# Does Your Model Run on AWS Trainium? Look It Up

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://huggingface.co/blog/torch-neuronx-model-support

## 核心主題
這篇文章介紹了如何使用 Hugging Face 的 torch-neuronx 工具來檢查模型是否可以在 AWS Trainium 上運行，並提供了模型支援資訊和運行腳本。

## 關鍵重點
- 提供了 torch-neuronx model support Space，可以查詢熱門模型是否在 Trainium 上運行，顯示運行結果、核心數、運行時間等資訊
- 每個模型測試結果包含完整的運行腳本和安裝指令，包括如何從公共 NEFF cache 桶同步編譯圖
- 測試標準：在 trn2 實例上運行，模型權重分佈到最小核心數，生成 32 個 token 並驗證結果
- 所有測試結果儲存在公開數據集 aws-neuron/torch-neuronx-model-support 中，可用 Pandas 直接查詢
- 目前僅測試 Transformers 模型（text-generation 和 image-text-to-text 任務），未來將擴展到其他任務

## 結論
這是一個實用的工具，幫助開發者快速了解哪些模型可以在 AWS Trainium 上運行，並提供完整的運行解決方案，包括模型分佈、編譯和運行腳本。

---