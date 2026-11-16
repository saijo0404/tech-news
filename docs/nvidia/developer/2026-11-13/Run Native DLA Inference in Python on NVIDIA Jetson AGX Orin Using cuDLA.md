# Run Native DLA Inference in Python on NVIDIA Jetson AGX Orin Using cuDLA

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-13
- **原文連結**: https://developer.nvidia.com/blog/run-native-dla-inference-in-python-on-nvidia-jetson-agx-orin-using-cudla/

## 核心主題
這篇文章介紹如何在 NVIDIA Jetson AGX Orin 上使用 cuDLA Python API 進行原生的 DLA 推理，實現 GPU 預處理、DLA 推理和 GPU 後處理的混合模式工作流。

## 關鍵重點
- NVIDIA Deep Learning Accelerator (DLA) 在 Jetson AGX Orin 上執行支援的神經網路操作，提高電源效率並釋放 GPU 容量供其他任務使用
- cuda.bindings.cudla 模組將 cuDLA C++ API 暴露給 Python，使開發者可以無需撰寫 C++ 代碼即可整合 DLA 推理到應用程式中
- 完整的推理生命週期包含九個步驟：初始化 CUDA、創建混合模式 DLA 設備、從記憶體載入編譯後的模型、內省張量描述符、分配 GPU 緩衝區、與 cuDLA 註冊緩衝區、複製預處理輸入數據、在 CUDA 流上提交任務、同步並讀回結果
- cuDLA 呼叫失敗時會引發 Python 異常，允許使用標準的 try/finally 清理和通過 cudla.Status 枚举進行細粒度的錯誤處理
- 相同的 cuDLA Python API 也適用於 NVIDIA RTX Spark，將 DLA 推理擴展到 Windows AI 開發者筆記本電腦

## 結論
cuDLA Python API 為開發者提供了在嵌入式設備和 Windows AI 筆記本上運行 DLA 推理的簡便方法，實現了 GPU 和 DLA 硬件的高效協同工作，無需撰寫低階的 C++ 代碼即可管理推理生命週期。
---

檔案已成功儲存至指定路徑。
