---
title: DeepSeek
type: entity
entity_type: product
created: 2026-04-12
updated: 2026-04-12
tags:
  - ai
  - llm
  - open-source
  - reasoning
related:
  - "[[entities/products/deepseek]]"
  - "[[sources/articles/blogjava-2025-02-08-DEEPSEEK背后的数学深入研究群体相对策略优化GRPO]]"
---

# DeepSeek

## 定义

DeepSeek 是一系列开源的大型语言模型（LLM），由中国公司 DeepSeek AI 开发。以 DeepSeek-R1 为代表，该模型在推理能力方面表现出色，可与 OpenAI 的 o1 模型相媲美。

## 核心技术

### 1. DeepSeek-R1
- **推理模型**：专注于复杂推理任务
- **架构**：基于 Transformer 的 MoE（混合专家）架构
- **参数规模**：671B 总参数，37B 激活参数

### 2. GRPO (Group Relative Policy Optimization)
- 群体相对策略优化算法
- **无需 Critic 模型**：通过组内比较优化策略
- **相对评估**：使用组内响应的相对表现作为奖励信号
- **优势**：
  - 降低计算开销
  - 提高训练稳定性
  - 适用于复杂推理任务

### 3. 训练阶段
1. **预训练**：大规模语料训练
2. **监督微调 (SFT)**：高质量指令数据
3. **RLHF/GRPO**：强化学习人类反馈优化

## 性能表现

- **AIME 2024**：71.0% Pass@1（多数投票下 86.7%）
- **数学推理**：与 OpenAI o1 相当
- **代码生成**：在 HumanEval 上表现优异

## 相关资源

- [[sources/articles/blogjava-2025-02-02-DEEPSEEK资源]]
- [[sources/articles/blogjava-2025-02-08-DEEPSEEK背后的数学深入研究群体相对策略优化GRPO]]
- [[sources/articles/blogjava-2025-02-15-满血版DEEPSEEK-R1全网资源]]
