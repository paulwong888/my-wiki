---
title: AI应用场景
type: source
category: article
created: 2025-01-17
updated: 2026-04-12
source_url: http://www.blogjava.net/paulwong/archive/2025/01/17/451559.html
author: paulwong
tags: ['ai']
---

# AI应用场景

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/17/451559.html  
**发布时间**: 2025-01-17

## 摘要

# AI应用场景

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/17/451559.html
**发布时间**: 2025-01-17

AI应用场景
@import url(http://www.blogjava.net/CuteSoft_Client/CuteEditor/Load.ashx?type=style&file=SyntaxHighlighter.css);@import url(/css/cuteeditor.css); @import url(http://www.blogjava.net/CuteSoft_Client/CuteEditor/Load.ashx?type=style&file=SyntaxHighlighter.css);@import url(/css/cuteeditor.css);
到底AI是虚的还是假的, 在企业中有没实际落地场景, 以下取实际应用场景:


生物公司
使用qwen2:7b训练细胞制备领域的数据集，目标是
1.预测细胞收获量  
2.算细胞存活状态(存...

## 原文内容

# AI应用场景

**原文链接**: http://www.blogjava.net/paulwong/archive/2025/01/17/451559.html
**发布时间**: 2025-01-17

AI应用场景
@import url(http://www.blogjava.net/CuteSoft_Client/CuteEditor/Load.ashx?type=style&file=SyntaxHighlighter.css);@import url(/css/cuteeditor.css); @import url(http://www.blogjava.net/CuteSoft_Client/CuteEditor/Load.ashx?type=style&file=SyntaxHighlighter.css);@import url(/css/cuteeditor.css);
到底AI是虚的还是假的, 在企业中有没实际落地场景, 以下取实际应用场景:


生物公司
使用qwen2:7b训练细胞制备领域的数据集，目标是
1.预测细胞收获量  
2.算细胞存活状态(存活/死亡)
3.预测工艺是否成功
4.可以提前预测细胞的质量是否达标，以便及时采取措施进行调整
5.细胞培养过程中出现大量细胞死亡的情况，模型可以根据实时数据和历史经验，分析可能是培养箱温度失控、培养基成分错误或受到污染等原因导致的，并提供相应的排查建议」


文体旅游
智能旅游系统:
提供目的地介绍、
旅行路线规划、
酒店预订和景
点推荐等服务。


考试改卷
基于大模型，做一个判试卷的应用，能够判断主观题，比如阅读理解，比如历史，地理，政治问答题。
判卷准确率不能低于人工判卷准确率。
即一次考试，一个班50份试卷，判断结果错误不超过5道题。判断效率高于或等于人工。

取过往同学试卷题目, 作答内容, 得分 作一波ocr出数据, 一个科目, 提取所有试卷内容, 最后就是一个科目一个模型, 提取的内容放在文本, csv, json,
基于“bert-base-chinese”这个模型, 进行微调出专用模型即可,  
让大模型成为专业的判卷老师


考试
用扣子打一个智能体，实现不同学员对掌握的知识进行测试，根据测试结果进行打分和二次出题测试







posted on 2025-01-17 11:23 paulwong 阅读(169) 评论(0)  编辑  收藏 所属分类: AI-LLM

## 摄入记录

- **摄入时间**: 2026-04-12
- **来源**: blogjava.net/paulwong
