# Skills

> **Status: ACTIVE** — This index is maintained by `contributor`. Update it whenever a skill is added, deprecated, or archived.

This is the master index of all shared skills in this repo. A skill is a reusable instructional module — a discrete, teachable capability that one or more agents can apply. Skills live here so that improvements benefit every agent that uses them.

---

## Skills Library

| Skill | File | What it does | Used by |
|---|---|---|---|
| `browser-navigation` | [.agents/skills/browser-navigation/SKILL.md](.agents/skills/browser-navigation/SKILL.md) | Foundational Browser MCP operation patterns: login check, navigate, snapshot, click, paginate | all browser-enabled skills |
| `search-query-design` | [.agents/skills/search-query-design/SKILL.md](.agents/skills/search-query-design/SKILL.md) | Constructs effective LinkedIn search queries using Boolean operators, filters, and keyword strategies | `sourcer`, `headhunter` |
| `person-search` | [.agents/skills/person-search/SKILL.md](.agents/skills/person-search/SKILL.md) | Searches for people on LinkedIn via Browser MCP: filter selection, result interpretation, lead identification | `sourcer` |
| `job-search` | [.agents/skills/job-search/SKILL.md](.agents/skills/job-search/SKILL.md) | Searches for job postings via Browser MCP: parameters, freshness evaluation, noise filtering | `headhunter` |
| `profile-summary` | [.agents/skills/profile-summary/SKILL.md](.agents/skills/profile-summary/SKILL.md) | Extracts key information from a LinkedIn profile via Browser MCP: role, trajectory, signals, fit indicators | `sourcer`, `headhunter` |
| `opportunity-qualification` | [.agents/skills/opportunity-qualification/SKILL.md](.agents/skills/opportunity-qualification/SKILL.md) | Evaluates whether a job or opportunity is worth pursuing given stated criteria | `headhunter` |
| `company-research` | [.agents/skills/company-research/SKILL.md](.agents/skills/company-research/SKILL.md) | Researches a company via Browser MCP: size, growth, hiring patterns, culture | `headhunter` |
| `lead-ranking` | [.agents/skills/lead-ranking/SKILL.md](.agents/skills/lead-ranking/SKILL.md) | Ranks and prioritizes a list of people or opportunities using weighted signals | `sourcer`, `headhunter` |
| `outreach-drafting` | [.agents/skills/outreach-drafting/SKILL.md](.agents/skills/outreach-drafting/SKILL.md) | Drafts effective LinkedIn outreach messages: structure, length, tone, call to action | *(outreach-writer, sourcer)* |
| `message-personalization` | [.agents/skills/message-personalization/SKILL.md](.agents/skills/message-personalization/SKILL.md) | Personalizes messages using profile data: hooks, shared context, authentic connection points | *(outreach-writer)* |
| `note-taking` | [.agents/skills/note-taking/SKILL.md](.agents/skills/note-taking/SKILL.md) | Records structured session outputs for reuse in future sessions | all agents |
| `follow-up-planning` | [.agents/skills/follow-up-planning/SKILL.md](.agents/skills/follow-up-planning/SKILL.md) | Plans next steps and follow-up actions after a search or outreach session | `sourcer`, `headhunter` |

---

## How to add a new skill

1. Copy [`templates/skill-template.md`](.templates/skill-template.md) to `skills/your-skill-name.md`.
2. Fill in all sections. Be precise about inputs, outputs, and which agents use it.
3. Set status to `draft`.
4. Submit a [`contributor-request`](.templates/contributor-request.md) to have `contributor` review, update this index, and set status to `active`.

---

## Key rules

- Skills are shared. If an instruction appears in more than one agent doc, it must become a skill.
- Skills are instructional. Factual knowledge belongs in `references/`, not `skills/`.
- Skills may reference each other directionally. No circular references.
- Only `contributor` may add or remove entries from this index.

See [governance/naming-conventions.md](.governance/naming-conventions.md) for naming rules.
