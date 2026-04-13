---
title: Graphify
type: entity
entity_type: product
created: 2026-04-12
updated: 2026-04-12
sources:
  - graphify-karpathy-llm-wiki
tags:
  - ai-tool
  - knowledge-graph
  - open-source
  - claude-code
related:
  - "[[entities/people/karpathy]]"
  - "[[concepts/frameworks/llm-wiki]]"
  - "[[concepts/theories/knowledge-graph]]"
---

# Graphify

## 基本信息

- **类型**: AI 编程助手技能（Skill）
- **GitHub**: github.com/safishamsi/graphify
- **Stars**: 3.2k+（发布一周）
- **Forks**: 301
- **开发语言**: Python
- **许可证**: MIT
- **创建时间**: 2026 年 4 月

## 一句话定义

一个命令，把任何文件夹变成可查询的知识图谱。

## 核心功能

1. **知识图谱构建**：读取文件夹中的所有内容（代码、文档、论文、截图、白板照片）构建可查询的知识图谱
2. **双轨提取引擎**：
   - 代码文件 → tree-sitter AST 解析（零 Token）
   - 文档/图片 → Claude 语义提取
3. **社区检测**：Leiden 算法基于图拓扑自动发现社区（无需 embedding）
4. **信任审计链**：每条边标记为 EXTRACTED/INFERRED/AMBIGUOUS
5. **Token 压缩**：71.5× 压缩率，后续查询读取 graph.json 而非原始文件

## 使用场景

- 代码库理解：快速理解大型代码库的结构和依赖关系
- 知识管理：构建个人或团队的知识图谱
- 研究辅助：整理论文、笔记、想法之间的关联
- AI 增强：在 Claude Code / Codex 中通过图谱导航而非暴力搜索

## 技术栈

| 组件 | 技术 |
|------|------|
| 图引擎 | NetworkX（纯 Python） |
| 社区检测 | Leiden 算法（graspologic） |
| 代码解析 | tree-sitter（16 种语言） |
| 可视化 | vis.js（交互式 HTML 图谱） |
| LLM 后端 | Claude / GPT-4 |

## 相关实体

- **理念来源**: [[entities/people/karpathy]] - Andrej Karpathy（前 Tesla AI 总监、OpenAI 创始成员）

## 相关概念

- [[concepts/frameworks/llm-wiki]] - LLM 编译知识库理念
- [[concepts/theories/knowledge-graph]] - 知识图谱
- [[concepts/frameworks/ai-agent]] - AI Agent 智能体

## 来源

- [[sources/articles/graphify-karpathy-llm-wiki]]
