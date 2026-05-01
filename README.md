# Chief of Staff OS — Template

A Claude Code–powered operating system for engineering directors. Helps you run a tighter daily rhythm — morning briefs, meeting prep, EOD capture, and exec communication — without the admin overhead.

Built and used by [Justin Johnson](https://github.com/jmjohnson24) at Thryv. Shared as a template for other directors to adapt.

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
