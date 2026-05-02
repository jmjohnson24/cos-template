# Chief of Staff OS — Template

A Claude Code–powered operating system for engineering directors. Helps you run a tighter daily rhythm — morning briefs, meeting prep, EOD capture, and exec communication — without the admin overhead.

Built and used by [Justin Johnson](https://github.com/jmjohnson24) at Thryv. Shared as a template for others to adapt.

---

## What it does

- **`gm`** — Morning brief: calendar gaps, Jira P1/P2 signals, Slack flags, inbox scan, tasks due today
- **`prep [meeting]`** — Meeting prep from calendar, Jira, Slack, and your relationships file
- **`draft [audience] [topic]`** — Exec-quality Slack/email drafts with built-in critique step
- **`eod`** — End-of-day capture: decisions, open items, goals check, tasks update
- **`triage`** — Classify all unread signals as DECIDE NOW / RESPOND TODAY / DELEGATE / READ LATER / IGNORE
- **`enrich`** — Update your relationships file from recent 1:1s and Slack/email
- **`check`** — Friday goals drift check
- **`week`** — Weekly initiative status for Friday updates
- **`sprint [team]`** — Pull and analyze sprint data from Jira
- **`/schedule`** — Set up remote routines that run automatically on a schedule and DM you the output via Slack. Claude will also suggest routines when it notices you running the same command at the same time repeatedly.

---

## How it works

Your repo has a few key files Claude reads at the start of every session:

| File | Purpose |
|---|---|
| `goals.yaml` | Your annual goals with weights — the north star for every `check` and `eod` |
| `tasks.md` | Discrete action items: things with a clear owner, deadline, and done state |
| `initiatives/` | One file per active multi-week effort — evolving status, risks, blockers, decisions |
| `relationships.md` | How the people around you operate — updated by `enrich` from 1:1s and Slack |
| `decisions-log.md` | Append-only log of decisions made — written by `eod` each day |

**Tasks vs. initiatives:** A task is a checkbox — send an email, approve a ticket, follow up with someone. An initiative is a narrative — something with moving parts, dependencies, and a status that changes week to week. If you'd want to give someone a two-sentence briefing on it, it belongs in `initiatives/`. If it's a single action, it belongs in `tasks.md`.

---

## Getting started

### 1. Use this template

Click **"Use this template"** at the top of this page (not "Clone"). Give your repo a name (e.g. `my-cos`) and set it to **Private**.

### 2. Install Claude Code

```bash
npm install -g @anthropic/claude-code
```

### 3. Open the repo in Claude Code

```bash
cd my-cos
claude
```

### 4. Run setup

```
setup
```

Claude will walk you through configuring the repo for your org — your name, reporting chain, direct reports, goals, key relationships, and Jira/Slack settings. Takes about 10 minutes.

### 5. Try your first morning brief

```
gm
```

---

## Requirements

- Claude Code CLI (or Claude.ai with MCP connectors)
- Atlassian MCP connector (Jira + Confluence access)
- Microsoft 365 MCP connector (email + calendar)
- Slack MCP connector

All connectors are available via Claude.ai's integration settings.

---

## Privacy

This repo is yours. Keep it private. It will contain your goals, decisions, relationships, and org context — none of that should be public.
