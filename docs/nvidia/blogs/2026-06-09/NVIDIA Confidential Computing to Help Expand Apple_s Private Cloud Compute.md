# NVIDIA Confidential Computing 將協助擴展 Apple 的 Private Cloud Compute

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://blogs.nvidia.com/blog/nvidia-confidential-computing-apple-private-cloud-compute/

## 核心主題
NVIDIA 宣布搭載 Confidential Computing 技術的 GPU 現已用於 Apple Private Cloud Compute（PCC）的保密推論，隨 PCC 擴展至 Google Cloud，NVIDIA 正與 Apple 和 Google 合作支援下一代 Apple Intelligence 功能，使用 Blackwell GPU 並整合至 PCC 硬體安全架構。

## 關鍵重點
- **Apple PCC 擴展至 Google Cloud：NVIDIA Blackwell GPU 支援 Apple Foundation Models 伺服器端推論**：搭載 Confidential Computing 的 NVIDIA GPU 現已用於 Apple Private Cloud Compute 的保密推論，隨著 PCC 從 Apple 自己的資料中心擴展至 Google Cloud；在 WWDC 上公佈，NVIDIA GPU 將支援 Apple Foundation Models 的伺服器端推論——這些由 Apple 和 Google 共同客製建構的模型，運用 Gemini 系列模型背後的技術；NVIDIA 正與 Apple 和 Google 合作，使用搭載 Confidential Computing 的 NVIDIA Blackwell GPU，整合至 Google Cloud 上執行的 PCC 硬體安全架構，支援下一代 Apple Intelligence 功能。
- **Confidential Computing 提供硬體層級安全：保護資料處理過程中的隱私，連建構者都无法查看使用者資料**：NVIDIA Confidential Computing 為加速 AI 工作負載提供硬體基礎的安全層；這項技術透過將工作負載隔離在可信執行環境（TEE）中，並在任何敏感資料發送給伺服器前加密驗證基礎設施未被篡改，保護處理中的資料；對最終使用者而言，這意味著沒有人——甚至系統建構者——可以查看他們的使用者資料、聊天或對話；隨 AI 體驗結合裝置端與雲端處理，市場需要高伺服器端推論效能，同時維持強烈的隱私與安全保證。
- **四大核心能力：硬體根信任、加密通訊、遠端證明、加速 AI 推論與訓練支援**：NVIDIA Confidential Computing 反映 NVIDIA 對可信 AI 的承諾，包含四大關鍵能力——（1）硬體根信任：幫助確認系統運行於真實、未被篡改的 NVIDIA GPU 上；（2）加密通訊路徑：保護資料在元件間傳輸時的隱私；（3）遠端證明：讓軟體在釋放敏感資料前驗證平台安全狀態；（4）加速 AI 推論與訓練支援：幫助組織在不犧牲 GPU 效能的前提下運行隱私敏感工作負載；這些能力對於需要處理敏感資訊同時維持使用者隱私控制的 AI 服務日益重要。

## 結論
NVIDIA 與 Apple、Google 的三方合作標誌著 AI 基礎設施在隱私與效能之間取得關鍵平衡——Apple 的 Private Cloud Compute 擴展至 Google Cloud，意味著 Apple Intelligence 的雲端推論能力獲得了更大的基礎設施規模，同時透過 NVIDIA Confidential Computing 的硬體根級安全保護，確保使用者的敏感資料即使在雲端處理期間仍受到嚴格加密與隔離；從硬體根信任到遠端證明，NVIDIA 的 Confidential Computing 架構為企業級 AI 服務建立了新的隱私標準，證明高運算效能與強隱私保障並非互斥，而是可以透過硬體級安全設計共存；這對 Apple 而言是強化 Apple Intelligence 差異化競爭力的關鍵一役，對 NVIDIA 而言則是將 Confidential Computing 從企業級解決方案推入主流消費者 AI 應用的重要里程碑。
