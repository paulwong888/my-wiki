---
title: AI Agent
type: concept
category: framework
created: 2026-04-12
updated: 2026-04-12
tags:
  - ai
  - agent
  - automation
  - llm
related:
  - "[[concepts/frameworks/llm-wiki]]"
  - "[[entities/products/claude-code]]"
  - "[[sources/articles/blogjava-2026-02-04-OPEN-CLAW资源]]"
---

# AI Agent (智能体)

## 定义

AI Agent（人工智能智能体）是一种能够**自主感知环境、做出决策并执行行动**的 AI 系统。与传统的单轮对话模型不同，Agent 可以持续与环境交互，完成复杂任务。

## 核心组件

### 1. 感知 (Perception)
- 接收环境输入
- 理解用户意图
- 收集外部信息

### 2. 推理 (Reasoning)
- 分析问题
- 制定计划
- 选择工具

### 3. 行动 (Action)
- 执行工具调用
- 修改环境状态
- 返回结果

### 4. 记忆 (Memory)
- 短期记忆：当前对话上下文
- 长期记忆：历史交互和知识

## Agent 类型

| 类型 | 描述 | 示例 |
|------|------|------|
| **任务型** | 专注于特定任务 | 代码助手、数据分析 |
| **通用型** | 处理多种任务 | AutoGPT、Claude Code |
| **协作型** | 多 Agent 协作 | Multi-Agent 系统 |
| **自主型** | 高度自主决策 | 研究 Agent |

## 相关技术

- **ReAct**：推理+行动框架
- **CoT (Chain-of-Thought)**：思维链推理
- **Tool Use**：工具使用能力
- **RAG**：检索增强生成

## 相关资源

- [[sources/articles/blogjava-2026-01-06-AI应用资源]]
- [[sources/articles/blogjava-2026-01-27-AGENT-SKILL]]
- [[sources/articles/blogjava-2026-02-06-Agent案例-开发流程]]
