---
title: CLAUDE CODE SKILL - PLANNING-WITH-FILES
type: source
category: article
created: 2026-02-18
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2026/02/18/451744.html
author: paulwong
tags: ['claude']
---

# CLAUDE CODE SKILL - PLANNING-WITH-FILES

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/02/18/451744.html  
**发布时间**: 2026-02-18

## 摘要

# CLAUDE CODE SKILL - PLANNING-WITH-FILES

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/02/18/451744.html
**发布时间**: 2026-02-18

CLAUDE CODE SKILL - PLANNING-WITH-FILES
Planning-with-Files 是一个用于 Claude Code 的 Agent Skill，其核心价值并不是让模型本身变得更聪明，而是通过文件化和结构化的方法，解决 AI 在复杂、长期、多步骤任务中容易出现的上下文遗忘和目标漂移问题。在传统对话式使用 AI 的过程中，随着任务时间拉长，模型往往会偏离最初目标，缺乏清晰的阶段划分和整体进度意识，进而导致反复返工和效率下降。该 Skill 的关键做法，是将任务计划、执行步骤、中间结果以及复盘内容写入本地文件，通常以 Markdown 形式存在。模型在每一次执行前都会读取这些文件，从而重新加载当前任务状态，持续理解整体目标与所处阶段。这种方式本质上是一种工程化的上下文管理手段，把...

## 原文内容

# CLAUDE CODE SKILL - PLANNING-WITH-FILES

**原文链接**: http://www.blogjava.net/paulwong/archive/2026/02/18/451744.html
**发布时间**: 2026-02-18

CLAUDE CODE SKILL - PLANNING-WITH-FILES
Planning-with-Files 是一个用于 Claude Code 的 Agent Skill，其核心价值并不是让模型本身变得更聪明，而是通过文件化和结构化的方法，解决 AI 在复杂、长期、多步骤任务中容易出现的上下文遗忘和目标漂移问题。在传统对话式使用 AI 的过程中，随着任务时间拉长，模型往往会偏离最初目标，缺乏清晰的阶段划分和整体进度意识，进而导致反复返工和效率下降。该 Skill 的关键做法，是将任务计划、执行步骤、中间结果以及复盘内容写入本地文件，通常以 Markdown 形式存在。模型在每一次执行前都会读取这些文件，从而重新加载当前任务状态，持续理解整体目标与所处阶段。这种方式本质上是一种工程化的上下文管理手段，把原本依赖模型短期记忆的内容，转移到可持久保存、可检查、可调整的外部结构中，并提升复杂任务的稳定性和可控性。在多步骤协作场景中尤为明显。适合长期使用。效果稳定。 


安装
/plugin marketplace add OthmanAdi/planning-with-files
/plugin install planning-with-files@planning-with-files



posted on 2026-02-18 18:09 paulwong 阅读(70) 评论(0)  编辑  收藏 所属分类: AI-CLAUDE-CODE

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
