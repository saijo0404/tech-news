# Open models, global networks: How AT&T and GSMA are accelerating telecom innovation with Gemma

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://cloud.google.com/blog/topics/telecommunications/open-models-global-networks-how-att-and-gsma-are-accelerating-innovation-with-gemma/

## 核心主題
GSMA 啟動 Open Telco AI 平台，由 AT&T 基於 Google 開源 Gemma 模型後訓練出 OTel 系列電信領域模型，以解決電信產業缺乏專業知識數據、通用 AI 模型難以精準理解網路操作的挑戰，推動電信自動化與代理式工作流的發展。

## 關鍵重點
- **電信領域專用模型的必要性**：現代行動網路具備多供應商、異構且常為專有結構的資料，而電信領域知識極少公開可取得，僅有 16% 的 AI 部署落於網路端。通用前沿模型缺乏管理關鍵基礎設施所需的基本脈絡，難以處理高度專門術語、複雜網路拓撲與供應商專屬遙測數據；而領域專用模型能透過訓練於特定數據集，精確解讀技術日誌、診斷網路瓶頸並理解標準產業協定。
- **Gemma 作為開源基礎與 OTel 成果**：GSMA 與 AT&T、網路設備供應商與學術界合作，以 Google Gemma 開源模型為基礎，訓練出涵蓋不同架構與大小的 30 個 OTel 模型。AT&T 測試顯示：gemma-4-E4B-it 模型正確回應率高達 91.74%，為所有測試模型中整體準確度最高；27B 參數的 Gemma 3 基線版本在初期訓練中表現最強；300M 參數且含電信嵌入的 Gemma 3 在檢索方面也有顯著提升。模型內建安全設計，使用 RAG 訓練 abstention 能力以大幅減少幻覺，符合電信業嚴格的合規需求。
- **Google Cloud 全堆疊解決方案與未來展望**：OTel 模型迄今已下載超過 1,1800 萬次，在 Open Telco Benchmarks 中名列前茅，證明針對特定領域優化的較小模型能超越龐大前沿模型。Google Cloud 承諾提供涵蓋 AI 優化基礎設施、開發工具與開源模型的完整解決方案，協助全球電信營運商以自有數據進一步微調模型，將程式碼與推理領域的進展延伸至自動網路設定與自癒合系統等關鍵電信子領域。

## 結論
AT&T、GSMA 與 Google 的跨界合作展現了開源模型在垂直產業的強大潛力——透過 Gemma 的靈活架構與電信領域數據的結合，OTel 不僅達成了高準確度與低幻覺率，更證明了「專精小模型勝過通用大模型」的領域 AI 路徑。隨著 Google Cloud 持續提供全堆疊工具與基礎建設，電信產業有望重現編碼與推理領域的突破，將 AI 帶入關鍵基礎設施的每一個環節。

---
