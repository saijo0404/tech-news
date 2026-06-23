---
# Build an AI Scientist for Life Science Discovery with NVIDIA BioNeMo Agent Toolkit

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://developer.nvidia.com/blog/build-an-ai-scientist-for-life-science-discovery-with-nvidia-bionemo-agent-toolkit/

## 核心主題
NVIDIA 推出 BioNeMo Agent Toolkit——將 NVIDIA 加速生物分子運算堆疊轉化為可呼叫的 AI Agent 工具，讓開發者能建構自主進行蛋白質摺疊、分子生成、配體对接與基因組分析的「AI 科學家」，推動生命科學研究的自動化迭代循環。

## 關鍵重點
- **BioNeMo Skills 將模型轉化為 Agent 工具**：BioNeMo NIM 將蛋白質結構預測（OpenFold3、Boltz-2）、分子生成（GenMol）、配體对接（DiffDock）、序列設計（ProteinMPNN）、多序列比对（MSA Search）與基因組學（Evo 2、Parabricks）等生物分子 AI 模型，包裝成文件化、可呼叫的微服務。BioNeMo Skills 描述每個模型的用途、必要輸入、選擇性參數、預期產出（CIF、SDF、FASTA、A3M、SMILES）與失敗模式，使 Agent 能正確選擇工具、準備有效請求並解讀結果。未包裝為 NIM 的開放模型則透過 Model Context Protocol（MCP）伺服器包裝提供相同介面。
- **部署策略與效能基準測試**：NIM 支援託管與本地兩種部署路徑——託管端點適合非生產環境的快速存取與基礎設施密集服務（如 MSA 搜索）；本地部署適合重複調用相同模型、需要低冷啟動延遲、資料在地性與執行階段控制的迭代 Agent 循環。基準測試顯示：使用 BioNeMo Skills 的 Agent 任務完成率從 57.1% 提升至 100%；在 token 效率方面，每 1,000 個 token 產生的通過斷言數（passing assertions）提升 2 倍。
- **四步驟建構 AI 科學家工作流**：（1）規劃科學工作流——從研究目標出發，選擇適合模型；（2）將 Agent 指向 BioNeMo Agent Toolkit 倉庫以探索可用能力；（3）選擇託管或本地部署；（4）透過 Skills 使用模型。Agent 的工作循環為：生成候選→檢查產出→調整參數→重新執行，BioNeMo Skills 加速此循環並減少設定與重試次數。

## 結論
BioNeMo Agent Toolkit 解決了通用程式設計 Agent 無法直接應用於生物學研究的核心問題——生命科學不是軟體工程，沒有測試套件能驗證假說是否正確，Discovery 是迭代、不確定且扎根於物理世界的。透過將 NVIDIA 加速生物分子堆疊轉化為 Agent 可用的工具層，BioNeMo 讓「AI 科學家」能從提示到假說、從假說到模型呼叫、從模型產出到下一個科學決策，形成完整的研究迭代循環，將孤立的模型呼叫轉化為真正的自動化生物科學發現流程。

---
