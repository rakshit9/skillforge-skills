# SkillForge Skills

A curated library of **agent "skills"** — self-contained Markdown prompt modules that give an AI assistant a specific persona, mental model, or workflow. Each skill has YAML frontmatter (`name`, `description`, activation triggers) followed by the behavioral playbook the model adopts when the skill is invoked.

This repo is the content library that powers [**SkillForge**](https://github.com/rakshit9/SkillForge). Skills are portable plain Markdown — drop them into any agent runtime that supports loadable skills/system prompts.

## Skill format

```markdown
---
name: senior-engineer
description: |
  Senior engineer code reviewer. Catches bugs, design flaws,
  security issues, and performance problems before they hit production.
  Use when: "review this code", "is this production ready"...
---

# Senior Engineer · Code Review Skill
...behavioral playbook, activation triggers, frameworks...
```

## Skill catalog

### Thinkers & mental models
| Skill | What it does |
|-------|--------------|
| `charlie-munger` | Latticework of mental models, inversion, incentive analysis |
| `naval-ravikant` | Leverage, specific knowledge, wealth-creation philosophy |
| `paul-graham` | Essayist's clarity; startup and founder reasoning |
| `steve-jobs` | Product taste, focus, "say no to 1,000 things" |
| `elon-musk` | First-principles engineering, aggressive simplification |
| `richard-feynman` | Explain by understanding from the ground up |
| `first-principles` | Decompose a problem to fundamentals and rebuild |

### Engineering
| Skill | What it does |
|-------|--------------|
| `senior-engineer` | Production-grade code review (correctness → design → security → perf) |
| `git-workflow` | Disciplined branching, commits, and PR hygiene |
| `clarity-editor` | Tighten writing without losing meaning |

### Explaining
| Skill | What it does |
|-------|--------------|
| `eli5` | Explain like I'm 5 — simple, accurate, not dumbed down |
| `explain-deep` | Layered explanations from intuition to depth |

### Product & strategy
| Skill | What it does |
|-------|--------------|
| `product-strategist` | Frame product bets, tradeoffs, and prioritization |
| `startup-roast` | Brutally honest critique of a startup idea |

## Usage

Pick a skill file and load its contents as a system prompt / skill in your agent runtime (Claude Code, custom agents, etc.). The frontmatter `description` tells the host when to activate it; the body defines how the model behaves.

## Related

- [SkillForge](https://github.com/rakshit9/SkillForge) — the app that creates, manages, and serves these skills.
