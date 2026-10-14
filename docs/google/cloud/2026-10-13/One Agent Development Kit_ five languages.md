# One Agent Development Kit, five languages

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-10-14
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/one-agent-development-kit-five-languages/

## 核心主題
Google 推出 Agent Development Kit (ADK)，提供 Python、Go、TypeScript、Java 和 Kotlin 五種語言的原生支援，打破單一語言限制，透過開源協議實現跨語言互操作性。

## 關鍵重點
- **五種語言原生支援**：ADK 提供 Python、Go、TypeScript、Java 和 Kotlin 的原生實現，每種語言針對其運行時和類型系統量身打造。
- **統一架構與開源協議**：所有版本共享統一架構，支援 Model Context Protocol (MCP) 和 Agent2Agent (A2A) 協議，實現跨語言互操作性。
- **各語言特色**：
  - **Python**：快速原型開發，最廣的 Google Cloud 整合與模型適配器
  - **Go**：生產後端工程首選，2 MiB 靜態二進制，高併發處理
  - **TypeScript**：與 Zod 搭配，靜態類型推斷，支援瀏覽器運行
  - **Java**：與 Maven/Gradle/Spring Boot 完美整合，RxJava 事件驅動
  - **Kotlin**：構建時安全，KSP 編譯器插件，零運行時反射，支援 Android 設備

## 結論
ADK 讓團隊無需鎖定單一語言，可根據不同組件需求選擇最適合的語言，實現最佳化開發體驗。
---