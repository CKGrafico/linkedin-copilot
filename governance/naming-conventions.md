# Naming Conventions

> **Status: ACTIVE** — Authoritative naming rules for this repo. Maintained by `contributor`. All files must comply.

---

## Guiding principle

Names should be self-explanatory. A person or AI model encountering a file name for the first time should immediately understand what is inside without opening it.

---

## General rules

- All file names: `kebab-case`, lowercase only, `.md` extension
- All folder names: `kebab-case`, lowercase only, no underscores
- No abbreviations unless the abbreviation is universally understood (e.g., `cv` is not acceptable; spell it out)
- No version numbers in file names (use status banners and `CHANGELOG.md` instead)
- No generic names: `utils.md`, `misc.md`, `notes.md`, `temp.md` are never acceptable

---

## By file type

### Agent files (`agents/`)

Named exactly after the agent's role, as a single noun or compound noun.

- ✅ `sourcer.md`
- ✅ `headhunter.md`
- ✅ `outreach-writer.md`
- ❌ `sourcing-agent.md` (redundant suffix)
- ❌ `job-finder.md` (use `headhunter.md` — the canonical name)

### Skill files (`skills/`)

Named as a noun phrase describing the action or capability. Use present-tense gerund form where natural.

- ✅ `person-search.md`
- ✅ `outreach-drafting.md`
- ✅ `lead-ranking.md`
- ❌ `searching-people.md` (gerund phrase, not noun phrase)
- ❌ `how-to-rank-leads.md` (not a noun phrase)

### Workflow files (`workflows/`)

Named as an imperative verb phrase describing the complete task.

- ✅ `find-relevant-recruiters.md`
- ✅ `prepare-outreach.md`
- ✅ `compare-opportunities.md`
- ❌ `recruiter-finding.md` (not imperative)
- ❌ `workflow-1.md` (meaningless)

### Reference files (`references/`)

Named as a noun phrase describing the knowledge domain.

- ✅ `sourcing-heuristics.md`
- ✅ `outreach-best-practices.md`
- ✅ `recruiter-signals.md`
- ❌ `recruiter-info.md` (too vague)

### Template files (`templates/`)

Named as `[type]-template.md`.

- ✅ `agent-template.md`
- ✅ `skill-template.md`
- ❌ `new-agent.md` (not obviously a template)

### Governance files (`governance/`)

Named as a noun phrase describing the policy or convention being documented.

- ✅ `naming-conventions.md`
- ✅ `status-model.md`
- ✅ `handoff-conventions.md`

---

## Reserved names

These root file names are reserved and must not be repurposed:

- `README.md`
- `AGENTS.md`
- `SKILLS.md`
- `GLOSSARY.md`
- `CHANGELOG.md`

---

## Rename policy

When a file is renamed, `contributor` must:
1. Update all cross-links pointing to the old name
2. Check `AGENTS.md` and `SKILLS.md` indexes for the old name
3. Add a note to `CHANGELOG.md`
4. Consider whether a deprecated stub with a forwarding notice is needed
