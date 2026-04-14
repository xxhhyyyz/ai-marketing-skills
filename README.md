# AI Marketing Skills

AI-native marketing skills for Claude Code and AI agents. Built for AI company marketing teams who want to think and execute marketing the AI-native way.

Works with Claude Code, Cursor, Windsurf, and any agent that supports the [Agent Skills spec](https://agentskills.io).

## What's Inside

5 modular skills covering the full AI marketing workflow:

```
┌─────────────────────────────┐
│   ai-marketing-context      │
│   (all skills read this)    │
└──────────────┬──────────────┘
               │
    ┌──────────┼──────────┬──────────────┐
    ▼          ▼          ▼              ▼
┌────────┐ ┌────────┐ ┌────────┐  ┌──────────┐
│content │ │content │ │event   │  │hackathon │
│capture │→│distri- │ │sop     │  │          │
│        │ │bution  │ │        │  │          │
└────────┘ └────────┘ └───┬────┘  └─────┬────┘
                          │             │
                          └──────┬──────┘
                                 ▼
                    event output → distribution
```

| Skill | Description |
|-------|-------------|
| [ai-marketing-context](skills/ai-marketing-context) | Product positioning, audience, brand voice, competitive landscape — the foundation all other skills read first |
| [ai-content-capture](skills/ai-content-capture) | Extract marketing angles from changelogs, docs, competitor moves, user feedback, and benchmarks |
| [ai-content-distribution](skills/ai-content-distribution) | Platform strategy matrix, launch playbooks, KOL outreach, AEO (AI search optimization), and measurement frameworks |
| [ai-event-sop](skills/ai-event-sop) | End-to-end SOP for AI summits, developer days, workshops, and meetups — from T-30 to T+3 with full checklists |
| [ai-hackathon](skills/ai-hackathon) | Complete hackathon playbook: track design, judging criteria, tech support, sponsor packages, and post-event incubation |

## Installation

### Option 1: CLI Install (Recommended)

```bash
# Install all skills
npx skills add MiniMax-AI/ai-marketing-skills

# Install specific skills
npx skills add MiniMax-AI/ai-marketing-skills --skill ai-event-sop ai-hackathon
```

### Option 2: Clone and Copy

```bash
git clone https://github.com/MiniMax-AI/ai-marketing-skills.git
cp -r ai-marketing-skills/skills/* ~/.claude/skills/
```

## Usage

Once installed, just describe what you need:

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

## Who Is This For

- AI company marketing teams
- Developer relations teams
- AI startup founders doing their own marketing
- Event organizers running AI hackathons and conferences

## Contributing

PRs and issues welcome! If you have battle-tested marketing playbooks for AI products, we'd love to include them.

## License

[MIT](LICENSE)
