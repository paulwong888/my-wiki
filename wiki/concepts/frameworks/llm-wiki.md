---
title: LLM Wiki
type: concept
category: framework
created: 2026-04-12
updated: 2026-04-12
sources:
  - graphify-karpathy-llm-wiki
tags:
  - knowledge-management
  - llm
  - methodology
  - personal-wiki
related:
  - "[[concepts/theories/knowledge-graph]]"
  - "[[entities/products/graphify]]"
  - "[[entities/people/karpathy]]"
---

# LLM Wiki

## 定义

LLM Wiki 是由 Andrej Karpathy 在 2026 年 4 月提出的**知识管理方法论**，核心理念是「用 LLM 编译个人知识库」——让 LLM 成为知识库的图书管理员，而非每次从原始文档检索。

## 核心理念

> "The wiki is a persistent, compounding artifact."
> 
> 维基是一个持久的、复利式的产物。

### 关键洞察

1. **增量构建**: 不是每次都从原始文档检索，而是逐步构建和维护结构化维基
2. **交叉引用**: 链接已经存在，无需每次重新发现
3. **矛盾标记**: 矛盾已经被标记，无需重新检测
4. **复利效应**: 每增加一个来源、每提出一个问题，维基都变得更丰富

## 三层架构

```
wiki-project/
├── raw/              # Layer 1: 源文档（不可变）
├── wiki/             # Layer 2: LLM 维护的知识库
│   ├── entities/     # 实体页面（人物、组织、产品）
│   ├── concepts/     # 概念页面（思想、理论、方法）
│   ├── sources/      # 来源摘要
│   └── comparisons/  # 对比分析
├── log.md            # 活动日志
└── WIKI.md           # Layer 3: 模式配置
```

## 核心操作

### 1. 摄入（Ingest）
添加新来源时：
- 创建/更新来源摘要
- 提取实体和概念页面
- 添加交叉引用（`[[page-name]]` 语法）
- 更新索引

### 2. 查询（Query）
提出问题时：
- 定位相关页面
- 综合答案并引用来源
- 将好的分析保存回维基

### 3. 检查（Lint）
定期健康检查：
- 检测页面间的矛盾
- 发现孤立页面
- 识别缺失引用

## 与传统 RAG 的区别

| 维度 | 传统 RAG | LLM Wiki |
|------|----------|----------|
| 存储 | 原始文档 | 结构化维基 |
| 查询 | 每次检索原始文档 | 读取已编译的知识 |
| 积累 | 无积累 | 复利式增长 |
| 交叉引用 | 动态计算 | 预先建立 |
| 矛盾检测 | 每次重新检测 | 已标记 |

## 工程化实现

### Graphify
[[entities/products/graphify]] 是第一个将 LLM Wiki 理念工程化的开源项目，主要创新：
- 从 Wiki 到 Graph（NetworkX 知识图谱）
- 双轨提取引擎（AST + LLM）
- 信任审计链（三级置信度标签）
- 71.5× Token 压缩

### llm-wiki Skill
当前使用的技能，基于 Karpathy 原始理念实现：
- 纯 Markdown 维基
- 三层架构（raw/wiki/config）
- 交互式和批处理模式
- 与 Obsidian 集成

## 最佳实践

1. **一次一个来源**（重要内容，交互模式）
2. **批量相似来源**（效率，新闻更新、常规报告）
3. **写回好查询** — 不要让洞察消失
4. **每周检查** — 在问题累积前捕获
5. **一致使用标签** — 启用 Dataview 查询
6. **保持 raw/ 不可变** — 维基是可变层
7. **每次摄入后 Git 提交** — 版本历史是免费的

## 相关概念

- [[concepts/theories/knowledge-graph]] - 知识图谱
- [[concepts/frameworks/ai-agent]] - AI Agent 智能体

## 来源

- [[sources/articles/graphify-karpathy-llm-wiki]]
- Karpathy 原始 Gist: gist.github.com/karpathy/442a6bf
