---
title: Knowledge Graph
type: concept
category: theory
created: 2026-04-12
updated: 2026-04-12
sources:
  - graphify-karpathy-llm-wiki
tags:
  - knowledge-representation
  - graph-theory
  - ai
  - data-structure
related:
  - "[[concepts/frameworks/llm-wiki]]"
  - "[[entities/products/graphify]]"
---

# Knowledge Graph（知识图谱）

## 定义

知识图谱是一种用图结构表示知识的方法，由**节点**（实体、概念）和**边**（关系）组成，用于描述现实世界中事物之间的关联。

## 基本结构

```
节点（Node）: 实体或概念
  ├── 人物: Karpathy, Elon Musk
  ├── 组织: OpenAI, Tesla
  ├── 产品: Graphify, GPT-4
  └── 概念: Transformer, 深度学习

边（Edge）: 关系
  ├── 类型: works_at, created, uses, relates_to
  ├── 方向: 有向或无向
  └── 属性: 权重、置信度、时间戳
```

## 与传统数据库的区别

| 特性 | 关系型数据库 | 知识图谱 |
|------|-------------|----------|
| 数据模型 | 表格 | 图（节点+边） |
| 关系表达 | 外键连接 | 直接边连接 |
| 查询方式 | JOIN 操作 | 图遍历 |
| 灵活性 | 固定模式 | 动态模式 |
| 语义表达 | 弱 | 强 |

## Graphify 中的知识图谱

[[entities/products/graphify]] 采用了独特的知识图谱设计：

### 1. 双轨构建
- **代码**: AST 解析 → 确定性图谱边
- **文档**: LLM 提取 → 语义相似性边

### 2. 无向量数据库
Graphify 刻意不使用 embedding 和向量数据库：
- 聚类基于图拓扑（Leiden 算法通过边密度发现社区）
- 图结构本身就是相似性信号

### 3. 信任审计链
每条边都有置信度标签：
- **EXTRACTED**: 直接来源于代码/引用（置信度 1.0）
- **INFERRED**: 合理推论（置信度 0.4-0.9）
- **AMBIGUOUS**: 不确定关系（置信度 0.1-0.3）

### 4. 超边（Hyperedges）
支持 3 个以上节点参与同一概念、流程或模式：
- 所有实现认证流程的函数
- 所有实现同一接口的类

## 应用场景

### 1. 企业知识管理
- 整合分散的文档和数据
- 发现隐性知识关联
- 支持智能问答

### 2. 搜索引擎
- Google Knowledge Graph
- 实体理解和关系推理
- 直接答案（而非链接列表）

### 3. AI 助手增强
- 代码库理解（如 Graphify）
- 上下文感知回答
- 多跳推理

### 4. 推荐系统
- 基于关系的路径推荐
- 发现潜在兴趣
- 解释推荐理由

## 常用技术栈

| 用途 | 工具/库 |
|------|---------|
| 图引擎 | NetworkX, Neo4j, Dgraph |
| 社区检测 | Leiden, Louvain |
| 可视化 | vis.js, D3.js, Gephi |
| 图数据库 | Neo4j, Amazon Neptune, TigerGraph |

## 相关概念

- [[concepts/frameworks/llm-wiki]] - LLM Wiki 方法论
- [[concepts/frameworks/ai-agent]] - AI Agent 智能体

## 相关实体

- [[entities/products/graphify]] - 知识图谱工具
- [[entities/products/deepseek]] - 开源推理模型
- [[entities/products/claude-code]] - AI 编程助手

## 来源

- [[sources/articles/graphify-karpathy-llm-wiki]]
