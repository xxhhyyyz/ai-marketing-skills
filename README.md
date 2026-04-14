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

传统市场经验告诉你：
- 先做调研，再定策略，再出内容，再投放，再复盘
- 一个 campaign 周期 2-4 周
- 内容要精雕细琢、层层审批
- 每个渠道配专人运营

**这套打法在 AI 行业会死。**

AI 行业的节奏是：竞品周二发了个新模型，你周三必须有响应；开源社区今天在讨论一个新范式，你今天就得参与；一个用户在 Twitter 上用你的 API 做了个很酷的东西，你必须在它火之前就转发和放大。

**AI Native Marketing 的核心不是「用 AI 做营销」，而是「像 AI 一样做营销」：**

- **快速迭代 > 完美执行**：先发出去，再优化。一条推文 5 分钟，不是 5 天
- **信号驱动 > 计划驱动**：别做月度排期表了。盯信号，抓机会，快响应
- **全员皆兵 > 市场部独扛**：工程师写的技术博客比市场写的推广文效果好 10 倍
- **社区共创 > 单向传播**：最好的内容不是你写的，是用户创造的
- **自动化 > 人肉**：能用 Agent 跑的流程，别用人

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
| [ai-content-distribution](skills/ai-content-distribution) | 渠道排期表 | 一套信号驱动的传播打法，含野路子 |
| [ai-event-sop](skills/ai-event-sop) | 活动 checklist | 从「办活动」到「用活动做增长」的完整方法论 |
| [ai-hackathon](skills/ai-hackathon) | 比赛筹备文档 | 把 Hackathon 变成产品增长引擎的操盘手册 |

## 环境准备

**这套 Skills 推荐搭配 Claude Code + 飞书 CLI 使用，解锁完整能力。**

### 1. Claude Code（必装）

```bash
# 安装 Claude Code
npm install -g @anthropic-ai/claude-code

# 启动
claude
```

这是你的 AI 营销助手运行的底座。所有 skill 通过 Claude Code 加载和触发。

### 2. 飞书 CLI（强烈推荐）

```bash
# 安装
npm install -g @larksuite/cli

# 登录认证
lark-cli auth login --domain im --domain drive --domain calendar --domain task
```

为什么推荐飞书 CLI？因为 AI 公司的市场部日常就在飞书里：

- **活动筹备**的任务分配、日程安排、文档协作 → `lark-cli task` / `lark-cli calendar`
- **内容素材**的文档存储和协作 → `lark-cli docs`
- **团队沟通**和嘉宾对接 → `lark-cli im`
- **数据看板**的多维表格 → `lark-cli base`

搭配飞书 CLI，你的 Agent 不只是帮你想，还能帮你**做**——直接在飞书里创建任务、发消息、写文档、更新表格。

### 3. 安装 Skills

```bash
# 安装全部
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

## 野路子合集

> 传统营销教科书不会教你这些，但在 AI 行业它们真的管用。

**内容抓取的野路子**
- 别等 changelog 出来再提炼——直接盯 GitHub commit log，比 PM 更早知道下个版本有什么
- 去竞品的 Discord/社区里潜水，用户的吐槽就是你的差异化弹药
- 监控 Hacker News 和 Reddit，行业讨论刚起来就参与，别等成了热点再追

**传播的野路子**
- AI Demo 的 GIF/短视频比任何文案都管用。一个 wow moment 顶一千字
- 让工程师自己发推/发朋友圈，比市场部的官方账号有效 10 倍
- 在 GitHub README 里做营销——这是开发者产品最被低估的营销渠道
- 用 Claude Code + 飞书 CLI 实现「一键分发」：写完内容自动同步到飞书文档、发群通知、创建跟进任务

**活动的野路子**
- 别做大会做小局。30 人的闭门 Workshop 转化率吊打 500 人的峰会
- AI 产品的 Demo 环节让观众出题，现场实时跑。观众自己出的 prompt 产出的效果，说服力是你准备好的 demo 的 100 倍
- 活动结束后 30 分钟内出回顾推文（Agent 当场就能写），比第二天出的效果好 5 倍
- 用飞书 CLI 自动创建活动相关的任务清单、日程提醒、群聊——省掉 80% 的行政工作

**Hackathon 的野路子**
- 赛前让参赛者在群里组队，自然社交比你分配的组队有效得多
- 准备一个「速成 Demo 模板」——让完全不会前端的后端工程师也能做出好看的展示
- 获奖作品别只发奖金——帮他们写一篇技术博客，帮他们推上 Product Hunt。这些后续传播的价值比奖金大得多
- 赛后用飞书多维表格追踪所有参赛团队的后续动态，持续运营才是 Hackathon 的真正 ROI

## 谁适合用

- **AI 公司市场部** — 你终于可以像你卖的产品一样工作了
- **DevRel 团队** — 开发者关系的 SOP 化，让新人也能快速上手
- **AI 创业者** — 你就是整个市场部，这些 skill 就是你的团队
- **活动组织者** — 办过一次 Hackathon 就知道 checklist 有多重要

## 设计理念

**不是通用营销，是 AI 行业营销。**

这套 skill 聚焦 AI 产品特有的挑战：

- **技术翻译**：把模型能力、Benchmark 翻译成「所以我能用来干嘛」
- **Demo 即战场**：AI 产品的现场演示是最强传播力，也是最大风险点
- **开发者即渠道**：开发者既是用户也是推广者，这个关系要认真经营
- **速度即壁垒**：AI 行业以周为单位迭代，传播节奏也得跟上
- **全球化叙事**：同一个产品，中文社区和英文社区需要完全不同的故事
- **Agent 即同事**：能让 Agent 跑的流程就别用人。你的时间应该花在判断和创意上

## 贡献

欢迎 PR 和 Issue！

特别欢迎：
- 你在 AI 公司实战验证过的营销打法
- 好用的「野路子」
- 飞书 CLI 的更多集成场景
- 其他语言的本地化

## License

[MIT](LICENSE)
