# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

A personal AI agent management dashboard for the OpenClaw agent framework. It's a single static HTML file (`index.html`) — no build system, no package manager, no dependencies.

## Development

Open `index.html` directly in a browser. No server or build step required.

## Architecture

**Single file:** `index.html` contains all HTML, CSS, and JavaScript inline.

**Tab-based UI** with four sections:
- **Memory** — Lists and displays markdown files from the parent workspace (`../MEMORY.md`, `../memory/*.md`)
- **Projects** — Textarea editor for project notes; tied to `PROJECTS.yaml` in the parent workspace
- **Uploads** — Form to upload files to Google Drive folder `10D4Dj4vkHlimS4te2TPDzZBd1t5IC-Y2` (OpenClaw/Uploads)
- **Agents** — Status display for spawned sub-agents (@Teacher-Claw, @CEO-Claw)

**Key JS functions** (all stubs — most logic not yet implemented):
- `showTab(tab)` — toggles active section/button
- `viewFile(path)` — intended to load and render a workspace markdown file
- `saveProjects()` — intended to persist projects textarea
- `refreshAgents()` — intended to fetch live agent status

## Workspace Context

This dashboard sits inside a larger OpenClaw workspace:

```
~/.openclaw/workspace/
├── dashboard/index.html   ← this repo
├── memory/                ← daily session logs (2026-03-XX.md)
├── MEMORY.md              ← curated long-term memory index
├── AGENTS.md              ← agent operational rules
├── SOUL.md                ← agent personality charter
├── USER.md                ← owner profile (Robert Baker)
├── PROJECTS.yaml          ← project status tracker
└── HEARTBEAT.md           ← periodic task checklist
```

The OpenClaw Python runtime (in `~/.openclaw/`) runs the actual agent logic; this dashboard is the human-facing UI layer.

## Current State

The dashboard is v1.3 and largely a UI prototype — `viewFile()`, `saveProjects()`, and Drive upload logic are not yet implemented. The agents tab is hardcoded static HTML.
