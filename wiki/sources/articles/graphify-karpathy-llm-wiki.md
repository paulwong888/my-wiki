---
title: Graphify：把 Karpathy 的 LLM Wiki 从理念变成了产品
type: source
category: article
created: 2026-04-12
updated: 2026-04-12
source_url: https://mp.weixin.qq.com/s/gkz3l8QiVmL3CsRUvtSygQ
author: AI作弊码
tags: [graphify, llm-wiki, karpathy, knowledge-graph, ai-tool]
---

# Graphify：把 Karpathy 的 LLM Wiki 从理念变成了产品

**原文链接**: https://mp.weixin.qq.com/s/gkz3l8QiVmL3CsRUvtSygQ  
**作者**: AI作弊码  
**抓取时间**: 2026-04-12

## 摘要

Graphify 是 Karpathy 在 2026 年 4 月初提出「用 LLM 编译个人知识库」理念后的**第一个工程化实现**的开源项目，发布一周即获得 3200+ Star。

## 核心定义

Graphify 是一个 **AI 编程助手技能（Skill）**，在 Claude Code、Codex、OpenCode 等工具里输入 `/graphify`，它就会读取文件夹中的所有内容——代码、文档、论文、截图、白板照片——然后构建一张**可查询的知识图谱**。

## 相比 Karpathy 原始理念的三大进化

| 维度 | Karpathy 理念 | Graphify 实现 |
|------|--------------|---------------|
| 存储格式 | Markdown Wiki | NetworkX 图 + JSON |
| 知识发现 | LLM 手动维护反向链接 | Leiden 算法自动社区检测 |
| 代码处理 | 全部走 LLM | 代码走 AST（零 Token），文档走 LLM |
| 可信度 | 无标注 | 三级置信度标签 + 分数 |
| 增量更新 | 概念性描述 | SHA256 缓存 + --update + git hooks |
| 多模态 | 提及图片 | 完整视觉理解（截图/图表/白板） |
| 工具生态 | Obsidian | HTML + Obsidian + Neo4j + MCP + SVG |

## 七级流水线架构

```
检测 → 提取 → 构建 → 聚类 → 分析 → 报告 → 导出
```

提取阶段的双轨并行设计：
- **左轨**：tree-sitter AST 静态解析（代码文件，零 Token，毫秒级）
- **右轨**：Claude 语义提取（文档/图片，并行子代理）

## 关键设计决策

### 1. 无向量数据库
Graphify 刻意不使用 embedding 和向量数据库。聚类完全基于图拓扑结构——Leiden 算法通过边密度发现社区。

### 2. 信任审计链
每条边都附带置信度标签：
- 🟢 **EXTRACTED**（提取）：关系直接来源于代码/引用，置信度 1.0
- 🟡 **INFERRED**（推断）：合理推论，每条边独立评分 0.4-0.9
- 🔴 **AMBIGUOUS**（存疑）：不确定的关系，置信度 0.1-0.3

### 3. 71.5× Token 压缩
- 第一次运行：消耗 Token 进行提取和图谱构建（一次性成本）
- 后续每次查询：读取紧凑的 graph.json 而非原始文件
- SHA256 缓存：重新运行只处理变更的文件，增量更新已有图谱

## 亮眼特性

- **超边（Hyperedges）**：支持 3 个以上节点参与同一个概念、流程或模式
- **全模态支持**：代码、PDF、Markdown、截图、架构图、白板照片
- **Always-On 模式**：每次 Grep/Glob 操作前先读取图谱报告
- **MCP 服务器模式**：把图谱暴露为 MCP stdio 服务器，提供 query_graph、get_neighbors、shortest_path 等工具

## 项目信息

- **GitHub**: github.com/safishamsi/graphify
- **Stars**: 3.2k+
- **Forks**: 301
- **语言**: Python
- **License**: MIT

## 相关阅读

- [[entities/people/karpathy]] - Karpathy 简介
- [[concepts/theories/knowledge-graph]] - 知识图谱概念
- [[concepts/frameworks/llm-wiki]] - LLM Wiki 方法论

## 摄入记录

- **摄入时间**: 2026-04-12
- **摄入方式**: wechat-article-spider 抓取 + llm-wiki 技能处理
