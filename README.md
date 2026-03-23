# OpenClaw Dashboard

A lightweight personal dashboard for managing the OpenClaw AI agent workspace — memory files, projects, file uploads, and sub-agent status.

## What It Is

A single-page HTML dashboard (`dashboard/index.html`) with no build system or dependencies. Open it directly in a browser.

## Features

- **Memory** — Browse and view workspace markdown memory files
- **Projects** — Edit and track active projects
- **Uploads** — Upload files to Google Drive (OpenClaw/Uploads folder)
- **Agents** — Monitor status of spawned sub-agents

## Structure

```
workspace/
├── dashboard/index.html   # The dashboard UI
├── memory/                # Daily session logs
├── MEMORY.md              # Long-term memory index
├── AGENTS.md              # Agent operational rules
├── SOUL.md                # Agent personality charter
├── USER.md                # Owner profile
└── PROJECTS.yaml          # Project tracker
```

## Stack

Vanilla HTML, CSS, and JavaScript. No frameworks, no build step.
