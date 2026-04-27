# 🤖 AI Agent Prompt System

A complete set of universal AI agent prompts for large-scale software project development. Copy these prompts into any AI assistant (Claude, GPT-4, Gemini, etc.) to get a structured, professional, multi-agent development team working on your project.

---

## 📁 Agent Files

| File | Agent | Role |
|---|---|---|
| `01-frontend-agent.md` | 🖥️ Frontend Agent | UI components, pages, state, routing, API integration |
| `02-backend-agent.md` | ⚙️ Backend Agent | APIs, business logic, auth, integrations, queues |
| `03-qa-agent.md` | 🧪 QA Agent | Test strategy, automated tests, bug reports, sign-off |
| `04-design-agent.md` | 🎨 Design Agent | UX/UI design, design system, specs, implementation review |
| `05-database-agent.md` | 🗄️ Database Agent | Schema design, migrations, indexing, data integrity |
| `06-monitor-agent.md` | 🔍 Monitor Agent | Quality oversight, scoring, improvement recommendations |

---

## 🚀 How to Use

### Step 1 — Choose the agent(s) for your task

| Task | Agents to Use |
|---|---|
| Build a UI component or page | `01-frontend-agent.md` + `06-monitor-agent.md` |
| Build an API endpoint | `02-backend-agent.md` + `06-monitor-agent.md` |
| Test a feature | `03-qa-agent.md` + `06-monitor-agent.md` |
| Design a screen or component | `04-design-agent.md` + `06-monitor-agent.md` |
| Design a database schema | `05-database-agent.md` + `06-monitor-agent.md` |
| Full-stack feature | All relevant agents + `06-monitor-agent.md` |

> ⚠️ **The Monitor Agent (`06`) must always be included alongside any specialist agent.** It reviews the session output and provides improvement feedback at the end.

### Step 2 — Load the prompt(s) into your AI assistant

Copy the full contents of your chosen agent file(s) and paste them as the **system prompt** or at the **start of the conversation** in your AI assistant.

**Example for a frontend task:**
```
[Paste full contents of 01-frontend-agent.md]
[Paste full contents of 06-monitor-agent.md]

---

My task: Build a user authentication login page with email/password fields, 
a "remember me" checkbox, and a "forgot password" link. 
The project uses React 18 with TypeScript and Tailwind CSS.
```

### Step 3 — Provide project context

At the start of your session, give the agent(s) the following context:

```
PROJECT CONTEXT:
- Project name: [Your project name]
- Tech stack: [e.g., React + Node.js + PostgreSQL]
- Current state: [New project / Existing codebase]
- Design system: [Tailwind / Material UI / Custom / None yet]
- Authentication: [JWT / OAuth / Sessions / None yet]
- Repository structure: [Monorepo / Separate FE+BE / Other]
- Any constraints or conventions: [e.g., "we use functional components only"]
```

### Step 4 — Review the Monitor Agent's report

After the specialist agent completes the task, the Monitor Agent will produce a **Session Report** with:
- A performance scorecard (0–10 across 6 dimensions)
- Critical issues that must be fixed before shipping
- Improvements for the next session
- Suggested updates to agent prompts for systemic issues

---

## 🔄 The Improvement Loop

```
Session 1:
  Agent works → Monitor evaluates → Improvement report generated

Session 2:
  Apply session 1 improvements → Agent works → Monitor evaluates → Report

Session N:
  Each session produces higher quality output than the last
```

The Monitor Agent tracks **recurring patterns** across sessions and recommends updates to agent prompts when the same gap appears 3+ times. This creates a self-improving system.

---

## 🤝 How Agents Communicate

```
┌─────────────┐    API Contract    ┌─────────────┐
│   Frontend  │◄──────────────────►│   Backend   │
│    Agent    │                    │    Agent    │
└──────┬──────┘                    └──────┬──────┘
       │                                  │
       │  Design Spec                     │  Schema Changes
       ▼                                  ▼
┌─────────────┐                    ┌─────────────┐
│   Design    │                    │  Database   │
│    Agent    │                    │    Agent    │
└─────────────┘                    └─────────────┘
       │                                  │
       └──────────────┬───────────────────┘
                      │
                      ▼
               ┌─────────────┐
               │   QA Agent  │
               │  (tests all)│
               └─────────────┘
                      │
                      ▼
               ┌─────────────┐
               │   Monitor   │
               │    Agent    │
               │(reviews all)│
               └─────────────┘
```

Each agent produces a **"Flags for Other Agents"** section in its output, ensuring clean handoffs and no dropped requirements.

---

## 💡 Tips for Best Results

1. **Always include project context** — agents produce better output when they know your stack
2. **One task per session** — focused tasks produce higher quality than "build everything" prompts
3. **Act on the Monitor Agent's critical issues** before starting the next session
4. **Build iteratively** — start with core functionality, let agents refine in subsequent sessions
5. **Share agent outputs with each other** — paste the Backend Agent's API contract into the Frontend Agent's context
6. **Update your stack in the prompt** — if you switch frameworks, update the PROJECT CONTEXT block

---

## 📐 Universal Compatibility

These prompts are designed to work with:
- ✅ Any programming language or framework
- ✅ Any AI assistant (Claude, GPT-4, Gemini, Mistral, etc.)
- ✅ Any project type (web app, mobile app, API, SaaS, internal tool)
- ✅ Any team size (solo developer to large team)
- ✅ New projects and existing codebases

---

## 📄 License

These prompts are free to use, copy, modify, and distribute for any purpose. Attribution appreciated but not required.

---

*Built to help developers ship better software, faster — with AI agents that think like senior engineers.*
