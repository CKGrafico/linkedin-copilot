# Skills

> **Status: ACTIVE** — This index is maintained by `contributor`. Update it whenever a skill is added, deprecated, or archived.

This is the master index of all shared skills in this repo. A skill is a reusable instructional module — a discrete, teachable capability that one or more agents can apply. Skills live here so that improvements benefit every agent that uses them.

---

## Skills Library

| Skill | File | What it does | Used by |
|---|---|---|---|
| `search-query-design` | [skills/search-query-design.md](skills/search-query-design.md) | Constructs effective LinkedIn search queries using Boolean operators, filters, and keyword strategies | `sourcer`, `headhunter` |
| `person-search` | [skills/person-search.md](skills/person-search.md) | Searches for people on LinkedIn: filter selection, result interpretation, lead identification | `sourcer` |
| `job-search` | [skills/job-search.md](skills/job-search.md) | Searches for job postings: parameters, freshness evaluation, noise filtering | `headhunter` |
| `profile-summary` | [skills/profile-summary.md](skills/profile-summary.md) | Extracts key information from a LinkedIn profile: role, trajectory, signals, fit indicators | `sourcer`, `headhunter` |
| `opportunity-qualification` | [skills/opportunity-qualification.md](skills/opportunity-qualification.md) | Evaluates whether a job or opportunity is worth pursuing given stated criteria | `headhunter` |
| `company-research` | [skills/company-research.md](skills/company-research.md) | Researches a company using LinkedIn signals: size, growth, hiring patterns, culture | `headhunter` |
| `lead-ranking` | [skills/lead-ranking.md](skills/lead-ranking.md) | Ranks and prioritizes a list of people or opportunities using weighted signals | `sourcer`, `headhunter` |
| `outreach-drafting` | [skills/outreach-drafting.md](skills/outreach-drafting.md) | Drafts effective LinkedIn outreach messages: structure, length, tone, call to action | *(outreach-writer, sourcer)* |
| `message-personalization` | [skills/message-personalization.md](skills/message-personalization.md) | Personalizes messages using profile data: hooks, shared context, authentic connection points | *(outreach-writer)* |
| `note-taking` | [skills/note-taking.md](skills/note-taking.md) | Records structured session outputs for reuse in future sessions | all agents |
| `follow-up-planning` | [skills/follow-up-planning.md](skills/follow-up-planning.md) | Plans next steps and follow-up actions after a search or outreach session | `sourcer`, `headhunter` |

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
