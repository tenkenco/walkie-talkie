# @tenken/walkie-cli

Optional companion skills and private agent prompts for Walkie's work-history recall.

Walkie's primary product story is creating agents as TOML files, deploying them, and publishing them under a Tenken handle. This repo is for the secondary path: private memory-style recall over prior work, debugging history, handoffs, and next-step briefs.

![Release](https://github.com/tenkenco/walkie-talkie/actions/workflows/release.yml/badge.svg)
[![npm](https://img.shields.io/npm/v/%40tenken%2Fwalkie-cli)](https://www.npmjs.com/package/@tenken/walkie-cli)
[![downloads](https://img.shields.io/npm/dm/%40tenken%2Fwalkie-cli)](https://www.npmjs.com/package/@tenken/walkie-cli)
[![docs](https://img.shields.io/badge/docs-tenken.co%2Fdocs-blue)](https://tenken.co/docs)

## Features

- Work-history companion skills for bug recall, handoff recovery, stale-attempt checks, and next-step briefs
- Private memory-agent TOMLs for session-backed or repo-bootstrapped recall
- Compatible with Claude, Claude Code, Codex, OpenCode, and ChatGPT workflows
- Designed to complement Walkie's public agent storefront, not replace it

## Quick start

```bash
npm i -g @tenken/walkie-cli
walkie --version
walkie auth login
walkie --help
```

## How this fits Walkie

Use the main Walkie flow when you want to ship public agents:

```bash
walkie agent deploy --file agent.toml --repo-path .
walkie agent preview <agent-id> --prompt "what does this agent do?"
walkie agent publish <agent-id>
```

Use this repo when you specifically want private recall over prior work:

```bash
walkie memory daemon
walkie memory status
walkie memory recall "what did we already try here?"
```

## Command map

```text
walkie auth       # signup, login, logout, status, provider, service-account
walkie agent      # deploy, list, get, status, publish, unpublish, reindex, preview, bundle-*, tool-*, secret-*, delete
walkie config     # show, set-tenken-url, set-landing-site-url, set-default-provider
walkie hub        # browse, search, info, chat, ask, key
walkie memory     # optional ambient sync runtime and recall commands
walkie billing    # status, upgrade, portal
walkie usage      # billing usage and quota summary
walkie health     # unauthenticated API health probe
```

## Companion skills

- `skills/walkie-bug-recall`
- `skills/walkie-handoff-recovery`
- `skills/walkie-next-step-brief`
- `skills/walkie-stale-attempt-synthesis`

These are for private prior-work synthesis. They are not the main public onboarding story for Walkie.

## Private agent manifests

- `walkie-memory-agent.toml`
- `walkie-memory-agent-repo.toml`

These are private agents for work-history recall, not public storefront examples.

## Links

- Product site: [tenken.co](https://www.tenken.co/)
- Docs: [tenken.co/docs](https://tenken.co/docs)
- Live deployed agents: [tenken.co/@rryoung98](https://www.tenken.co/@rryoung98)
- Walkie Onboarding Agent: [tenken.co/@rryoung98/walkie-onboarding-agent](https://www.tenken.co/@rryoung98/walkie-onboarding-agent)
- Chicago Dining Concierge: [tenken.co/@rryoung98/chicago-dining-concierge](https://www.tenken.co/@rryoung98/chicago-dining-concierge)
- Japan Dining Concierge: [tenken.co/@rryoung98/japan-dining-concierge](https://www.tenken.co/@rryoung98/japan-dining-concierge)
- Discord: [Join the community](https://discord.com/invite/GCBjdrus)
