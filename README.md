# AI Marketing Skills

> **你在一家 AI 公司做市场。**
>
> 你的产品能写文案、能画图、能剪视频、能写代码。但你自己呢？还在手动翻 changelog 找卖点，在飞书文档里复制粘贴活动 SOP，在 Excel 里排发布节奏，在微信群里追嘉宾确认。
>
> 你教全世界用 AI 提效。你自己是全公司最不 AI Native 的人。
>
> **这事儿不对。**

---

## 这不是又一个「营销 AI 工具」

市面上不缺 AI 营销工具。写文案的、做海报的、自动发帖的，一搜一大把。

但它们解决的是**执行层**的问题——帮你写一篇文章、生成一张图。

**AI Native Marketing 要解决的是思维层的问题：AI 公司的市场团队，到底该怎么工作？**

传统市场经验告诉你：先做调研，再定策略，再出内容，再投放，再复盘。一个 campaign 周期 2-4 周。内容要精雕细琢、层层审批。每个渠道配专人运营。

**这套打法在 AI 行业会死。**

AI 行业的节奏是：竞品周二发了个新模型，你周三必须有响应；开源社区今天在讨论一个新范式，你今天就得参与；一个用户在 Twitter 上用你的 API 做了个很酷的东西，你必须在它火之前就转发和放大。

**AI Native Marketing 的核心不是「用 AI 做营销」，而是「像 AI 一样做营销」：**

- **快速迭代 > 完美执行**。先发出去，再优化。一条推文 5 分钟，不是 5 天
- **信号驱动 > 计划驱动**。别做月度排期表了。盯信号，抓机会，快响应
- **全员皆兵 > 市场部独扛**。工程师写的技术博客比市场写的推广文效果好 10 倍
- **社区共创 > 单向传播**。最好的内容不是你写的，是用户创造的
- **自动化 > 人肉**。能用 Agent 跑的流程，别用人

## 这套 Skills 干什么

5 个模块化 Skill，装进你的 AI Agent（Claude Code / Cursor / Windsurf），让它理解 AI 公司市场部的工作语境，直接上手干活。

```
┌─────────────────────────────┐
│   ai-marketing-context      │
│   （所有 skill 先读这个）      │
└──────────────┬──────────────┘
               │
    ┌──────────┼──────────┬──────────────┐
    ▼          ▼          ▼              ▼
┌────────┐ ┌────────┐ ┌────────┐  ┌──────────┐
│内容抓取 │ │传播策略 │ │活动 SOP│  │赛事筹备   │
│capture │→│distri- │ │event   │  │hackathon │
│        │ │bution  │ │        │  │          │
└────────┘ └────────┘ └───┬────┘  └─────┬────┘
                          │             │
                          └──────┬──────┘
                                 ▼
                      活动产出 → 传播分发
```

| Skill | 不只是什么 | 更是什么 |
|-------|----------|---------|
| [ai-marketing-context](skills/ai-marketing-context) | 产品信息登记表 | 让 Agent 真正理解你的产品，像你的同事而非外包 |
| [ai-content-capture](skills/ai-content-capture) | changelog 整理工具 | 从任何信号源（竞品、用户、数据）中嗅出营销机会 |
| [ai-content-distribution](skills/ai-content-distribution) | 渠道排期表 | 一套信号驱动的传播打法 |
| [ai-event-sop](skills/ai-event-sop) | 活动 checklist | 从「办活动」到「用活动做增长」的完整方法论 |
| [ai-hackathon](skills/ai-hackathon) | 比赛筹备文档 | 把 Hackathon 变成产品增长引擎的操盘手册 |

## 安装

需要先安装 [Claude Code](https://claude.ai/claude-code)。如果你的团队用飞书协作，装上 [飞书 CLI](https://github.com/larksuite/cli) 效果更好——skill 里的很多流程可以直接打通飞书的任务、文档、消息和日程。

```bash
# 安装全部 skill
npx skills add xxhhyyyz/ai-marketing-skills

# 或只装你需要的
npx skills add xxhhyyyz/ai-marketing-skills --skill ai-event-sop ai-hackathon
```

## 使用方式

用自然语言描述你的需求：

```
"设置产品营销上下文"           → ai-marketing-context
"帮我从这个 changelog 提炼卖点"  → ai-content-capture
"这个新功能发布怎么传播"         → ai-content-distribution
"我们要办一个 AI 开发者日"       → ai-event-sop
"筹备一个 AI Hackathon"        → ai-hackathon
```

## 谁适合用

- **AI 公司市场部** — 你终于可以像你卖的产品一样工作了
- **DevRel 团队** — 开发者关系的 SOP 化，让新人也能快速上手
- **AI 创业者** — 你就是整个市场部，这些 skill 就是你的团队
- **活动组织者** — 办过一次 Hackathon 就知道 checklist 有多重要

## 设计理念

**不是通用营销，是 AI 行业营销。**

- **技术翻译**：把模型能力、Benchmark 翻译成「所以我能用来干嘛」
- **Demo 即战场**：AI 产品的现场演示是最强传播力，也是最大风险点
- **开发者即渠道**：开发者既是用户也是推广者，这个关系要认真经营
- **速度即壁垒**：AI 行业以周为单位迭代，传播节奏也得跟上
- **全球化叙事**：同一个产品，中文社区和英文社区需要完全不同的故事
- **Agent 即同事**：能让 Agent 跑的流程就别用人。你的时间应该花在判断和创意上

## 贡献

欢迎 PR 和 Issue！特别欢迎你在 AI 公司实战验证过的营销打法。

## License

[MIT](LICENSE)
