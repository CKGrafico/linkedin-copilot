# Skills

> **Status: ACTIVE** — This index is maintained by `contributor`. Update it whenever a skill is added, deprecated, or archived.

This is the master index of all shared skills in this repo. A skill is a reusable instructional module — a discrete, teachable capability that one or more agents can apply. Skills live here so that improvements benefit every agent that uses them.

---

## Skills Library

| Skill | File | What it does | Used by |
|---|---|---|---|
| `browser-navigation` | [.github/instructions/skills/browser-navigation.instructions.md](.github/instructions/skills/browser-navigation.instructions.md) | Foundational Browser MCP operation patterns: login check, navigate, snapshot, click, paginate | all browser-enabled skills |
| `search-query-design` | [.github/instructions/skills/search-query-design.instructions.md](.github/instructions/skills/search-query-design.instructions.md) | Constructs effective LinkedIn search queries using Boolean operators, filters, and keyword strategies | `sourcer`, `headhunter` |
| `person-search` | [.github/instructions/skills/person-search.instructions.md](.github/instructions/skills/person-search.instructions.md) | Searches for people on LinkedIn via Browser MCP: filter selection, result interpretation, lead identification | `sourcer` |
| `job-search` | [.github/instructions/skills/job-search.instructions.md](.github/instructions/skills/job-search.instructions.md) | Searches for job postings via Browser MCP: parameters, freshness evaluation, noise filtering | `headhunter` |
| `profile-summary` | [.github/instructions/skills/profile-summary.instructions.md](.github/instructions/skills/profile-summary.instructions.md) | Extracts key information from a LinkedIn profile via Browser MCP: role, trajectory, signals, fit indicators | `sourcer`, `headhunter` |
| `opportunity-qualification` | [.github/instructions/skills/opportunity-qualification.instructions.md](.github/instructions/skills/opportunity-qualification.instructions.md) | Evaluates whether a job or opportunity is worth pursuing given stated criteria | `headhunter` |
| `company-research` | [.github/instructions/skills/company-research.instructions.md](.github/instructions/skills/company-research.instructions.md) | Researches a company via Browser MCP: size, growth, hiring patterns, culture | `headhunter` |
| `lead-ranking` | [.github/instructions/skills/lead-ranking.instructions.md](.github/instructions/skills/lead-ranking.instructions.md) | Ranks and prioritizes a list of people or opportunities using weighted signals | `sourcer`, `headhunter` |
| `outreach-drafting` | [.github/instructions/skills/outreach-drafting.instructions.md](.github/instructions/skills/outreach-drafting.instructions.md) | Drafts effective LinkedIn outreach messages: structure, length, tone, call to action | *(outreach-writer, sourcer)* |
| `message-personalization` | [.github/instructions/skills/message-personalization.instructions.md](.github/instructions/skills/message-personalization.instructions.md) | Personalizes messages using profile data: hooks, shared context, authentic connection points | *(outreach-writer)* |
| `note-taking` | [.github/instructions/skills/note-taking.instructions.md](.github/instructions/skills/note-taking.instructions.md) | Records structured session outputs for reuse in future sessions | all agents |
| `follow-up-planning` | [.github/instructions/skills/follow-up-planning.instructions.md](.github/instructions/skills/follow-up-planning.instructions.md) | Plans next steps and follow-up actions after a search or outreach session | `sourcer`, `headhunter` |

---

## How to add a new skill

1. Copy [`templates/skill-template.md`](templates/skill-template.md) to `skills/your-skill-name.md`.
2. Fill in all sections. Be precise about inputs, outputs, and which agents use it.
3. Set status to `draft`.
4. Submit a [`contributor-request`](templates/contributor-request.md) to have `contributor` review, update this index, and set status to `active`.

---

## Key rules

- Skills are shared. If an instruction appears in more than one agent doc, it must become a skill.
- Skills are instructional. Factual knowledge belongs in `references/`, not `skills/`.
- Skills may reference each other directionally. No circular references.
- Only `contributor` may add or remove entries from this index.

See [governance/naming-conventions.md](governance/naming-conventions.md) for naming rules.
