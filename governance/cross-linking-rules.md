# Cross-Linking Rules

> **Status: ACTIVE** — Defines how files in this repo should reference each other. Maintained by `contributor`.

---

## Purpose

Cross-links make the repo navigable and allow agents to load only the files they need. Bad cross-links break agent sessions and waste time. These rules ensure links are consistent, correct, and maintainable.

---

## Link format

All links use **relative paths** from the current file's location.

```markdown
[skill-name](../skills/skill-name.md)
[reference-name](../references/reference-name.md)
[agent-name](../agents/agent-name.md)
```

From a root file (e.g., `README.md`), links are relative to the root:

```markdown
[sourcer](.github/instructions/agents/sourcer.instructions.md)
[person-search](.github/instructions/skills/person-search.instructions.md)
```

**Never use absolute paths.** Absolute paths break when the repo is moved or cloned.

---

## Link anchor text

Use the **file's canonical name** (without the `.md` extension) as anchor text when the name is self-explanatory:

```markdown
See [person-search](../.github/instructions/skills/person-search.instructions.md) for query construction.
```

When the file name alone is ambiguous, use a short descriptive phrase:

```markdown
See the [recruiter signals reference](../references/recruiter-signals.md) for activity pattern definitions.
```

**Never use raw paths as anchor text:**
- ❌ `[../references/recruiter-signals.md](../references/recruiter-signals.md)`
- ✅ `[recruiter-signals](../references/recruiter-signals.md)`

---

## Where links belong

### In agent files
- **Skills Used** section: link to every skill the agent uses
- **References Consulted** section: link to every reference the agent consults
- **Handoff Rules** section: link to the agents or templates involved in handoffs
- **Guardrails** section: link to `references/ethical-boundaries.md` where relevant

### In skill files
- **Used By** section: link to every agent that uses the skill
- **Related Skills** section: link to skills that complement or depend on this one
- **References** section: link to any reference files the skill consults

### In workflow files
- **Participants** section: link to every agent involved
- **Skills Invoked** section: link to every skill used
- **Steps**: inline link to the skill used at each step

### In reference files
- **When Agents Should Consult This** section: link to agents and skills that use it

---

## Directionality rule

Skill cross-references are **directional**: a more-specific skill may reference a more-general skill, but not the other way around.

- ✅ `outreach-drafting` → references `message-personalization`
- ❌ `message-personalization` → references `outreach-drafting` (creates a cycle)

Circular references are forbidden. `contributor` is responsible for detecting and breaking them.

---

## Link validation

When `contributor` renames or moves a file, it must:
1. Search all files for links pointing to the old path
2. Update every link to the new path
3. Verify no broken links remain
4. Note the rename in `CHANGELOG.md`

A broken link is treated as a high-priority maintenance issue.

---

## What not to link

- Do not link to external URLs in agent, skill, or workflow files. This repo is self-contained. External references may appear in `references/` files only, sparingly, and in a clearly labeled section.
- Do not link to session notes (those are user-owned, outside the repo).
- Do not link to archived files in active content.
