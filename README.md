# linkedin-copilot

> A Markdown-only, multi-agent knowledge and workflow system for your personal LinkedIn activity.

---

## What this is

rlinkedin-copilotr is a personal operating system for LinkedIn — made entirely of Markdown files. There is no code, no database, no API. The repo is a collection of AI-readable agent instructions, reusable skill modules, workflow guides, and reference documents. You give an AI model the relevant files as context, and those files tell it exactly who it is, what to do, and how to do it.

This is a serious personal knowledge-work system, not a toy.

---

## Who it is for

A single personal user managing their own LinkedIn presence: job searching, sourcing contacts, building a network, writing outreach, and researching people and companies. This is not an enterprise product.

---

## How to use it

1. Choose an agent from [rAGENTS.mdr((AGENTS.md) that matches your goal.
2. Open the agentrs file from ragents/r and read its **When to Use** section to confirm it is the right tool.
3. Give the agent file — and any referenced skill or reference files — to your AI model as context.
4. State your request in natural language.
5. Capture the output using the structured note format from [r.agents/skills/note-taking/SKILL.mdr((.agents/skills/note-taking/SKILL.md).

To request changes to the repo (new agents, updated references, new skills), use the [rtemplates/contributor-request.mdr((templates/contributor-request.md) template and invoke the rcontributorr agent.

---

## Repository structure

rrr
linkedin-copilot/
├── README.md               ← you are here
├── AGENTS.md               ← master index of all agents
├── SKILLS.md               ← master index of all skills
├── GLOSSARY.md             ← shared terminology
├── CHANGELOG.md            ← notable repo changes
│
├── agents/                 ← one file per agent
├── skills/                 ← reusable instruction modules
├── workflows/              ← end-to-end task flows
├── references/             ← factual LinkedIn knowledge base
├── templates/              ← blank scaffolds for new files
└── governance/             ← rules and conventions for contributor
rrr

---

## Agents at a glance

| Agent | What it does |
|---|---|
| [rcontributorr((.agents/agents/contributor/AGENT.md) | Maintains, organizes, and evolves the repo |
| [rsourcerr((.agents/agents/sourcer/AGENT.md) | Finds relevant people on LinkedIn |
| [rheadhunterr((.agents/agents/headhunter/AGENT.md) | Finds jobs and opportunities |

See [rAGENTS.mdr((AGENTS.md) for the full catalog including planned future agents.

---

## Design principles

This repo is built on a few hard rules:

- **Markdown only.** No code, YAML, JSON, or scripts.
- **One file, one purpose.** Each file does exactly one thing.
- **Skills are shared.** Reusable instructions live in rskills/r, not duplicated inside agent docs.
- **Only rcontributorr edits the repo.** User-facing agents consume knowledge; they do not rewrite it.
- **Every file has a status.** rdraftr, ractiver, rdeprecatedr, or rarchivedr — always visible.

See [rgovernance/r((governance/) for the full rulebook.

---

## Maintenance

This repo is maintained by the [rcontributorr((.agents/agents/contributor/AGENT.md) agent. To request a change, use [rtemplates/contributor-request.mdr((templates/contributor-request.md).
