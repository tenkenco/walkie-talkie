# @tenken/walkie-cli

Your secret weapon for AI session magic.

`walkie` helps you capture, share, replay, and search AI coding sessions — plus discover and deploy AI agents, right from your terminal.

![Release](https://github.com/tenkenco/walkie-talkie/actions/workflows/release.yml/badge.svg)
[![npm](https://img.shields.io/npm/v/%40tenken%2Fwalkie-cli)](https://www.npmjs.com/package/@tenken/walkie-cli)
[![downloads](https://img.shields.io/npm/dm/%40tenken%2Fwalkie-cli)](https://www.npmjs.com/package/@tenken/walkie-cli)
[![docs](https://img.shields.io/badge/docs-tenken.co%2Fdocs-blue)](https://tenken.co/docs)

## Features

- Session superpowers — create, search, enrich, version, download, sync
- Deploy AI agents — build RAG agents with custom context
- Agent Hub — browse, search, and chat with community agents
- Multi-platform — works with Claude, Claude Code, Codex, OpenCode, ChatGPT
- Built-in OAuth — login in seconds
- Script-friendly — great for automation and CI

## Quick start

```bash
npm i -g @tenken/walkie-cli
walkie --version
walkie auth login
walkie --help
```

## Command map

```text
walkie auth       # signup, login, logout, status
walkie agent      # deploy, list, get, status, publish, unpublish, preview, delete
walkie config     # show and update local CLI settings
walkie hub        # browse, search, info, chat, ask, key
walkie sessions   # list, search, get, upload, download, import, sync, delete
walkie billing    # status, upgrade, portal
walkie usage      # billing usage and quota summary
walkie health     # unauthenticated API health probe
```

## Common workflows

```bash
# Sign up and login
walkie auth signup
walkie auth login

# Discover community agents
walkie hub browse
walkie hub search "research"

# Chat with an agent (interactive)
walkie hub chat research-assistant

# Ask an agent a quick question
walkie hub ask research-assistant "What are the latest developments in AI agents?"

# Get an API key for an agent
walkie hub key create research-assistant
```

## Try an Agent

Browse and chat with these public RAG agents:

| Agent                  | Description                      | Try It                                    |
| ---------------------- | -------------------------------- | ----------------------------------------- |
| **Research Assistant** | Web search + synthesis           | `walkie hub ask research-assistant "..."` |
| **Creative Writer**    | Brainstorming, drafting, editing | `walkie hub ask creative-writer "..."`    |
| **Software Developer** | Debug, code review, architecture | `walkie hub ask dev-partner "..."`        |
| **Finance Advisor**    | Research, analysis, planning     | `walkie hub ask finance-advisor "..."`    |
| **Legal Counsel**      | Research, compliance, concepts   | `walkie hub ask legal-counsel "..."`      |

Example:

```bash
walkie hub chat research-assistant
# Then type your questions interactively
```

## Links

- Product site: [tenken.co](https://www.tenken.co/)
- Docs: [tenken.co/docs](https://tenken.co/docs)
- Discord: [Join the community](https://discord.com/invite/GCBjdrus)

Let's go!
