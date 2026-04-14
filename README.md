# AI Marketing Skills

> **AI 公司的市场团队，可能是全世界最拧巴的一群人。**
>
> 你卖的产品自己就能写文案、做海报、剪视频——但你的营销流程还停留在手动整理 changelog、Excel 排期、飞书文档复制粘贴的时代。你教别人用 AI 提效，自己却在用最传统的方式做市场。
>
> 更难的是：AI 产品的营销和传统 SaaS 完全不同。技术迭代按周计算，竞品发布此起彼伏，开发者社区要运营，Hackathon 要筹备，Demo Day 要执行，每一场活动都是一次技术事故的赌博（API 挂了怎么办？）。
>
> **这套 Skills 就是为了解决这个问题。**
>
> 把 AI 公司市场部最核心的工作流——从内容抓取、传播策略、活动 SOP 到赛事筹备——变成 AI Agent 可以直接执行的标准化技能。不是让 AI 替你思考，而是让 AI 帮你把「知道该怎么做」变成「真的做出来了」。

---

一套面向 AI 公司市场团队的 Agent Skills，让 AI 编码助手理解营销语境，直接上手干活。

适配 Claude Code、Cursor、Windsurf 及所有支持 [Agent Skills 规范](https://agentskills.io) 的 AI Agent。

## 包含什么

5 个模块化 Skill，覆盖 AI 营销全流程：

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

| Skill | 说明 |
|-------|------|
| [ai-marketing-context](skills/ai-marketing-context) | 产品定位、目标用户、品牌调性、竞品格局——所有 skill 的基础上下文 |
| [ai-content-capture](skills/ai-content-capture) | 从 changelog、技术文档、竞品动态、用户反馈、评测数据中提炼营销素材 |
| [ai-content-distribution](skills/ai-content-distribution) | 12 个平台的传播策略矩阵、发布节奏模板、KOL 触达、AI 搜索优化（AEO）、效果复盘 |
| [ai-event-sop](skills/ai-event-sop) | AI 峰会 / 开发者日 / Workshop / Meetup 的全流程 SOP，从 T-30 到 T+3 完整 checklist |
| [ai-hackathon](skills/ai-hackathon) | Hackathon 完整手册：赛题设计、评审标准、技术保障、赞助招商、赛后孵化 |

## 安装

### 方式一：CLI 安装（推荐）

```bash
# 安装全部 skill
npx skills add xxhhyyyz/ai-marketing-skills

# 安装指定 skill
npx skills add xxhhyyyz/ai-marketing-skills --skill ai-event-sop ai-hackathon
```

### 方式二：克隆仓库

```bash
git clone https://github.com/xxhhyyyz/ai-marketing-skills.git
cp -r ai-marketing-skills/skills/* ~/.claude/skills/
```

## 使用方式

安装后，用自然语言描述你的需求即可触发：

```
"设置产品营销上下文"
→ ai-marketing-context

"帮我从这个 changelog 提炼营销素材"
→ ai-content-capture

"这个新功能发布怎么传播"
→ ai-content-distribution

"我们要办一个 AI 开发者日"
→ ai-event-sop

"筹备一个 AI Hackathon"
→ ai-hackathon
```

## 谁适合用

- AI 公司市场部 / 品牌团队
- 开发者关系（DevRel）团队
- AI 创业者——自己就是整个市场部
- AI 活动组织者——筹备 Hackathon、峰会、开发者日

## 设计理念

**不是通用营销，是 AI 行业营销。**

这套 skill 聚焦 AI 产品特有的营销挑战：

- **技术翻译**：把模型能力、Benchmark 数据翻译成用户能感知的价值
- **Demo 即战场**：AI 产品的现场演示是核心传播力，但也是最大风险点
- **开发者即渠道**：开发者既是用户，也是最好的传播者
- **速度即壁垒**：AI 行业以周为单位迭代，传播节奏必须跟上
- **全球化叙事**：同一个产品，中文和英文社区需要完全不同的传播策略

## 贡献

欢迎 PR 和 Issue！如果你有经过实战验证的 AI 产品营销方法论，我们很乐意收录。

## License

[MIT](LICENSE)
