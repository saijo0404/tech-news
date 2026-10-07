# Managed Apache Iceberg at scale: How Spanner powers Lakehouse runtime catalog

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-07
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/lakehouse-runtime-catalog-powered-by-spanner/

## 核心主題
這篇文章介紹了 Google Cloud 如何利用 Spanner 構建 Lakehouse runtime catalog，以支持大規模代理（agent）時代的 Apache Iceberg 湖倉架構。

## 關鍵重點
- Lakehouse runtime catalog 是基於 Spanner 的完全無伺服器、高可用性元數據註冊表，原生實現 Apache Iceberg REST Catalog 規範
- 解決了湖倉管理目錄的核心痛點：原子提交與併發控制、高可用性與運維、大規模擴展、表維護協調、治理與安全
- 支持多引擎互操作性，可與 BigQuery、Managed Spark 等引擎協同工作，實現零數據複製
- 提供 AI 驅動的上下文和治理功能，整合 Knowledge Catalog 和 Cloud IAM，支持跨雲目錄聯邦

## 結論
Lakehouse runtime catalog 透過 Spanner 的行星級基礎設施，為代理規模的湖倉工作負載提供高可用性、併發能力和一致性保證，大幅降低運營成本。
---
