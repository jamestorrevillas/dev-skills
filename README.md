# dev-skills

A modular AI skill library for software engineers. 37 structured `SKILL.md` files covering technical development, AI agents, soft skills, and career growth — built for **GitHub Copilot Agents**, **Claude**, and **Claude Code**.

Drop it into any project and your AI assistant instantly becomes a better, more context-aware engineering partner.

---

## What's Inside

```
.github/
├── copilot-instructions.md     ← Always-on root instructions (plan mode, verification, self-improvement)
├── skills/                     ← 37 modular skill files
│   ├── ai-agent-design/
│   ├── git-workflow/
│   ├── testing/
│   └── ... (34 more)
└── tasks/
    ├── lessons.md              ← Persistent agent memory (commit this, never delete)
    ├── todo.md                 ← Per-session task tracker template
    └── session.md              ← Per-session work log template
```

---

## Skills

### Technical
| Skill | What It Covers |
|---|---|
| `ai-agent-design` | LLM integration, RAG, multi-agent orchestration, MCP, LangGraph, CrewAI, self-healing agents |
| `api-design` | REST, GraphQL, tRPC, gRPC patterns, versioning, pagination, security |
| `backend-dev` | Server logic, auth patterns, middleware, queues, error handling |
| `database-design` | Schema design, indexing, query optimization, vector DBs, Redis patterns |
| `debugging-mindset` | Scientific debugging method, divide & conquer, rubber duck, root cause |
| `devops-cicd` | CI/CD pipelines, Docker, Kubernetes, Terraform, monitoring, DevSecOps |
| `frontend-design` | Component architecture, Tailwind, accessibility, performance, Next.js App Router |
| `git-workflow` | Conventional commits, PR templates, branching strategies, code review etiquette |
| `incident-response` | Production incidents, postmortems, runbooks, blameless culture |
| `system-design` | Scalability, caching, load balancing, CAP theorem, back-of-envelope estimation |
| `testing` | Unit, integration, E2E (Playwright), mocking, coverage guidelines |
| `threat-modeling` | STRIDE, OWASP Top 10, attack surface analysis, security design principles |
| `code-review` | Quality checklists, security review, architecture review, feedback categories |

### AI & Prompting
| Skill | What It Covers |
|---|---|
| `prompt-engineering` | CoT, few-shot, ReAct, plan-before-execute, verification patterns, self-improvement loops |
| `ai-prompting-patterns` | Intent clarification, plan mode, task tracking, confirmation protocols, error communication |
| `ai-assisted-learning` | Socratic method, codebase navigation, skill gap analysis, avoiding over-reliance |
| `self-healing-mindset` | Resilience design, circuit breakers, retry logic, chaos engineering, developer self-improvement |
| `mcp-builder` | MCP server implementation in Python (FastMCP) and TypeScript |

### Documentation & Communication
| Skill | What It Covers |
|---|---|
| `doc-creation` | READMEs, architecture docs, runbooks, ADRs, AI-optimized documentation |
| `internal-comms` | DSU/standup format, sprint updates, leadership comms, Slack best practices |
| `technical-communication` | Explaining tech to non-technical audiences, BLUF format, decision communication |
| `code-explanation` | Inline comments, docstrings, PR descriptions, Architecture Decision Records |
| `cross-functional-collab` | Working with PMs and designers, translating tech decisions to business language |
| `client-communication` | Project scoping, scope creep, delivering bad news, handling feedback |

### Career & Growth
| Skill | What It Covers |
|---|---|
| `performance-review` | PA documents, self-assessments, peer feedback, honest accomplishment writing |
| `career-growth` | Developer growth model, 90-day plans, visibility without bragging |
| `interview-prep` | DSA patterns, system design framework, STAR behavioral method |
| `resume-portfolio` | Accomplishment writing formula, quantifying impact, portfolio writeups |
| `technical-mentoring` | Socratic code review, teaching patterns, feedback ladder |
| `side-project-planning` | Idea validation, MVP scoping, monetization models, build vs buy |

### Thinking & Problem-Solving
| Skill | What It Covers |
|---|---|
| `problem-solving` | First principles thinking, MECE decomposition, trade-off analysis |
| `research-synthesis` | Technology evaluation framework, decision documents, source quality |
| `code-reading` | Codebase onboarding order, code tracing, navigating large repos |
| `focus-productivity` | Deep work protocol, task prioritization, fighting procrastination |
| `tech-research` | Build vs buy framework, comparison templates, staying current |

### Building
| Skill | What It Covers |
|---|---|
| `web-artifacts-builder` | Multi-component React apps, shadcn/ui, Zustand, TanStack Query |
| `sprint-planning` | User stories, INVEST criteria, estimation scale, retrospectives, DSU |

---

## How It Works

### Skill Discovery
All skill names and descriptions are always in the agent's context via `copilot-instructions.md`. When a task matches a skill, the agent loads the full `SKILL.md` — this is called **progressive disclosure**. The agent only loads what's relevant, keeping context lean.

### Task Tracking (`.github/tasks/`)

| File | Purpose | Lifecycle |
|---|---|---|
| `lessons.md` | Persistent memory of past mistakes and rules | Commit it. Never delete. Grows over time. |
| `todo.md` | Plan + step tracker for the current session | Reset at start of each new task |
| `session.md` | Real-time work log and decision record | Reset at start of each new session |

The agent reads `lessons.md` at the start of complex tasks to avoid repeating mistakes from previous sessions.

### Root Instructions (`copilot-instructions.md`)

Inspired by Boris Cherny's CLAUDE.md, the root file enforces:
- **Plan before execute** — spec before code for any non-trivial task
- **Verification before done** — prove it works, don't just assert it
- **Self-improvement loop** — capture lessons from every correction
- **Confirmation before irreversible actions** — always ask before push, delete, deploy

---

## Pushing to GitHub (First Time Setup)

### Step 1 — Extract the zip
Extract `james-skills.zip` anywhere on your machine. You'll get a `james-skills/` folder.

### Step 2 — Initialize the repo
```bash
cd james-skills
git init
git add .
git commit -m "feat: initial commit — 37 dev skills for Copilot Agents and Claude"
```

### Step 3 — Create the repo on GitHub
Go to [github.com/new](https://github.com/new) and fill in:
- **Repository name:** `dev-skills`
- **Description:** `A modular AI skill library for software engineers — 37 SKILL.md files covering technical, soft, and career skills for GitHub Copilot Agents, Claude, and Claude Code.`
- **Visibility:** Public
- **Do NOT** initialize with README, .gitignore, or license (you already have your files)

Click **Create repository**.

### Step 4 — Connect and push
```bash
git remote add origin https://github.com/YOUR_USERNAME/dev-skills.git
git branch -M main
git push -u origin main
```

### Step 5 — Add topics
On your repo page, click the ⚙️ gear icon next to **About** and add these topics:
```
ai-skills  github-copilot  claude  prompt-engineering  skill-library
developer-tools  ai-agent  copilot-instructions  mcp  software-engineering
```

### Step 6 — Add license file
```bash
cat > LICENSE << 'EOF'
MIT License

Copyright (c) 2026 James Torrevillas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
EOF

git add LICENSE
git commit -m "chore: add MIT license"
git push
```

### Step 7 — Add .gitignore (recommended)
```bash
cat > .gitignore << 'EOF'
# OS
.DS_Store
Thumbs.db

# Editor
.vscode/
.idea/
*.swp

# Logs
*.log
EOF

git add .gitignore
git commit -m "chore: add .gitignore"
git push
```

> **Tip:** For future skill updates, use conventional commits:
> ```bash
> git add .github/skills/your-skill/SKILL.md
> git commit -m "feat(skills): add your-skill"
> git push
> ```

---

## Installation

### Option 1: Drop into an existing project
```bash
# Clone or download this repo, then copy .github/ into your project root
cp -r .github/ /path/to/your/project/
```

### Option 2: Clone and use as template
```bash
git clone https://github.com/YOUR_USERNAME/dev-skills.git
cd your-project
cp -r dev-skills/.github .
```

### Option 3: Git submodule
```bash
git submodule add https://github.com/YOUR_USERNAME/dev-skills.git .dev-skills
cp -r .dev-skills/.github .
```

After installing, GitHub Copilot Agents will automatically detect `.github/copilot-instructions.md` and load skills on demand.

---

## Compatibility

| Platform | Support | Notes |
|---|---|---|
| **GitHub Copilot Agents** (VSCode) | ✅ Full | Native support via `.github/skills/` and `copilot-instructions.md` |
| **Claude** (claude.ai) | ✅ Full | Upload `.github/skills/` folder to a Claude Project |
| **Claude Code** | ✅ Full | Place at project root — reads `SKILL.md` automatically |
| **Cursor** | ✅ Partial | Place content as `.cursor/rules/dev-skills.mdc` (`.cursorrules` is deprecated since 2025) |
| **Continue** | ✅ Partial | Reference skill files via prompt file system |

---

## Customizing

### Add your own skill
```
.github/skills/your-skill-name/
└── SKILL.md
```

Minimum `SKILL.md` structure:
```markdown
---
name: your-skill-name
description: Use this skill when [task]. Trigger on keywords: [keyword1], [keyword2].
---

# Your Skill Name

## Core Principle
[One sentence that captures the philosophy]

## [Section]
[Content]
```

Then add it to the skills table in `copilot-instructions.md`.

### Personalize the root instructions
Edit `.github/copilot-instructions.md` to match your team's stack, conventions, and preferred communication style.

### Track lessons across sessions
When your AI makes a mistake, ask it to append to `.github/tasks/lessons.md`. Over time this builds a project-specific memory of what goes wrong and how to prevent it.

---

## Structure Reference

```
.github/
├── copilot-instructions.md
├── skills/
│   ├── ai-agent-design/SKILL.md
│   ├── ai-assisted-learning/SKILL.md
│   ├── ai-prompting-patterns/SKILL.md
│   ├── api-design/SKILL.md
│   ├── backend-dev/SKILL.md
│   ├── career-growth/SKILL.md
│   ├── client-communication/SKILL.md
│   ├── code-explanation/SKILL.md
│   ├── code-reading/SKILL.md
│   ├── code-review/SKILL.md
│   ├── cross-functional-collab/SKILL.md
│   ├── database-design/SKILL.md
│   ├── debugging-mindset/SKILL.md
│   ├── devops-cicd/SKILL.md
│   ├── doc-creation/SKILL.md
│   ├── focus-productivity/SKILL.md
│   ├── frontend-design/SKILL.md
│   ├── git-workflow/SKILL.md
│   ├── incident-response/SKILL.md
│   ├── internal-comms/SKILL.md
│   ├── interview-prep/SKILL.md
│   ├── mcp-builder/SKILL.md
│   ├── performance-review/SKILL.md
│   ├── problem-solving/SKILL.md
│   ├── prompt-engineering/
│   │   ├── SKILL.md
│   │   └── references/prompt-templates.md
│   ├── research-synthesis/SKILL.md
│   ├── resume-portfolio/SKILL.md
│   ├── self-healing-mindset/SKILL.md
│   ├── side-project-planning/SKILL.md
│   ├── sprint-planning/SKILL.md
│   ├── system-design/SKILL.md
│   ├── tech-research/SKILL.md
│   ├── technical-communication/SKILL.md
│   ├── technical-mentoring/SKILL.md
│   ├── testing/SKILL.md
│   ├── threat-modeling/SKILL.md
│   └── web-artifacts-builder/SKILL.md
└── tasks/
    ├── lessons.md
    ├── todo.md
    └── session.md
```

---

## License

MIT — use freely, modify as needed, attribution appreciated but not required.

---

## Acknowledgements

Skill structure inspired by the [Claude Skills spec](https://github.com/travisvn/awesome-claude-skills) and [Boris Cherny's Claude Code workflow](https://www.infoq.com/news/2026/01/claude-code-creator-workflow/) (Boris Cherny is the creator of Claude Code at Anthropic). Research grounded in community data from [GitHub Awesome Copilot](https://github.com/github/awesome-copilot), [State of JS 2025](https://2025.stateofjs.com/en-US/), and Anthropic/OpenAI agentic communication guidelines.
