# Wiki Activity Log

This log records all wiki operations (ingests, queries, lint checks).

Format: `## [YYYY-MM-DD HH:MM] operation | Title`

---

## [2026-04-12 17:47] init | Wiki Created
- Project initialized with standard structure
- Directories created: raw/, wiki/
- Initial files created: index.md, overview.md, WIKI.md

## [2026-04-12 17:56] ingest | Graphify：把 Karpathy 的 LLM Wiki 从理念变成了产品
- Source: https://mp.weixin.qq.com/s/gkz3l8QiVmL3CsRUvtSygQ (微信公众号)
- Method: wechat-article-spider + llm-wiki skill
- Created source: [[sources/articles/graphify-karpathy-llm-wiki]]
- Created entities: [[entities/products/graphify]], [[entities/people/karpathy]]
- Created concepts: [[concepts/frameworks/llm-wiki]], [[concepts/theories/knowledge-graph]]
- Cross-references: 10+ added
- Images: 6 downloaded to raw/articles/images/

## [2026-04-12 20:00] ingest | BlogJava (paulwong) 博客文章批量摄入
- Source: http://www.blogjava.net/paulwong (2024年6月至今)
- Method: playwright-cli + Python 脚本
- Articles downloaded: 51 篇
- Articles ingested: 51 篇
- Created entities:
  - [[entities/technologies/stable-diffusion]] - AI图像生成
  - [[entities/products/deepseek]] - 开源推理模型
  - [[entities/products/claude-code]] - AI编程助手
- Created concepts:
  - [[concepts/frameworks/ai-agent]] - AI智能体
  - [[concepts/technologies/docker]] - 容器化技术
- Topics covered: Stable Diffusion, DeepSeek, Claude Code, Docker, Linux, LLM微调, RAG, MCP

## [2026-04-12 20:38] ingest | BlogJava (paulwong) 博客文章补充摄入
- Source: http://www.blogjava.net/paulwong (补充抓取)
- Method: playwright-cli + Python 脚本
- Articles downloaded: +53 篇 (总计 104 篇)
- Articles ingested: +49 篇 (总计 100 篇)
- New topics covered:
  - Agent案例 (研发团队、制作PPT、规格驱动开发、开发流程)
  - Claude Code Skill (50个常用skill、planning-with-files)
  - OpenClaw资源
  - AI炒股资源
  - vLLM部署

