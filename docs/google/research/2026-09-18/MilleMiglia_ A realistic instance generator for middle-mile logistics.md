# MilleMiglia: A realistic instance generator for middle-mile logistics

- **來源**: Google Research Blog
- **發布日期**: 2026-09-18
- **原文連結**: https://research.google/blog/millemiglia-a-realistic-instance-generator-for-middle-mile-logistics/

## 核心主題
MilleMiglia 是一個開源實例生成器，旨在填補學術理論與工業物流之間的差距，為中里程物流網絡提供真實的基準測試數據，從而推動更強大高效的全球供應鏈優化。

## 關鍵重點
- **中里程物流的重要性**：中里程物流承載了物流成本的大部分，且決定貨物是否能新鮮送达，但長期以來受到學術研究關注不足。
- **現有工具的限制**：傳統的车辆路径问题(VRP)求解器無法直接應用於中里程物流，因為其具有多商品流問題、固定時刻表、分撥中心容量限制和複雜的同步約束。
- **MilleMiglia 的技術特色**：使用 C++ 編寫，採用 Protocol Buffers 數據序列化，通過重力模型和空間分群生成地理分佈，並提供從小型到工業級規模的實例。
- **隱私保護與真實性**：基於公開數據和工業公開數據生成合成網絡，不洩露任何私有信息，同時保持真實性。

## 結論
MilleMiglia 是建立中里程物流標準化基準測試套件的第一步，通過開源實例生成器鼓勵更廣泛的研究社區關注中里程物流的運營挑戰，最終推動更強大高效的全球供應鏈。

---