# Agents

> **Status: ACTIVE** — This index is maintained by `contributor`. Update it whenever an agent is added, deprecated, or archived.

This is the master index of all agents in this repo. Each agent is a focused role with a defined mission, clear boundaries, and a complete operating manual in its file.

---

## Core Agents

| Agent | File | Purpose |
|---|---|---|
| `contributor` | [agents/contributor.md](agents/contributor.md) | Repo steward. The only agent authorized to modify, restructure, and maintain repo files. |
| `sourcer` | [agents/sourcer.md](agents/sourcer.md) | Finds relevant people on LinkedIn: recruiters, hiring managers, connectors, subject-matter experts. |
| `headhunter` | [agents/headhunter.md](agents/headhunter.md) | Finds jobs and opportunities aligned with your profile, goals, and preferences. |

---

## Planned Future Agents

These agents are not yet implemented. They are listed here to reserve their names and clarify intent.

| Agent | Planned purpose |
|---|---|
| `networker` | Builds intentional connection strategy. Identifies high-value targets for outreach. |
| `outreach-writer` | Drafts and refines personalized LinkedIn messages and connection requests. |
| `researcher` | Deep-dives on a specific person or company to prepare for a conversation or meeting. |
| `profile-reviewer` | Analyzes your own LinkedIn profile and produces improvement recommendations. |
| `company-scout` | Builds and maintains a target company list. Tracks hiring signals and company momentum. |

---

## How to add a new agent

1. Copy [`templates/agent-template.md`](templates/agent-template.md) to `agents/your-agent-name.md`.
2. Fill in all sections of the template.
3. Set status to `draft`.
4. Submit a [`contributor-request`](templates/contributor-request.md) to have `contributor` review, update this index, and set status to `active`.

---

## Notes

- Agent file names match the agent name exactly: `sourcer.md`, not `sourcing-agent.md`.
- Only `contributor` may add or remove entries from this index.
- See [governance/naming-conventions.md](governance/naming-conventions.md) for naming rules.
