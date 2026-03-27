# Contribution Guidelines

> **Status: ACTIVE** — Defines how `contributor` processes changes to the repo. Maintained by `contributor`.

---

## Who can change repo files

Only `contributor` may modify, create, rename, or delete files in this repo. User-facing agents produce outputs in session notes, not in repo files. If an agent session reveals something that should change the repo, the user routes a request to `contributor` using [`templates/contributor-request.md`](../templates/contributor-request.md).

---

## How contributor processes a change request

1. Read the contributor request carefully. Identify the type of change: new file, update to existing file, deprecation, rename, or structural change.
2. Before making any change, check for existing content that covers the same ground. Avoid duplication.
3. Identify which files (if any) will need cross-link updates after the change.
4. Make the change using the appropriate template.
5. Update `AGENTS.md` or `SKILLS.md` if the change involves adding or removing an agent or skill.
6. Update `GLOSSARY.md` if new terms are introduced.
7. Update `CHANGELOG.md` with a brief entry.
8. Set the new or updated file's status banner appropriately.

---

## Periodic review checklist

`contributor` should perform a periodic review of the repo. Use this checklist for each file reviewed:

**All files:**
- [ ] Status banner is present and correct
- [ ] "Last reviewed" date in Maintenance Notes is current
- [ ] Cross-links resolve to existing files
- [ ] File name follows [naming conventions](naming-conventions.md)

**Agent files additionally:**
- [ ] Uses the standard agent template structure
- [ ] All skill references are valid and linked
- [ ] All reference citations are valid and linked
- [ ] Guardrails section is complete and consistent with [`references/ethical-boundaries.md`](../references/ethical-boundaries.md)
- [ ] "When Not to Use" section names alternative agents where relevant

**Skill files additionally:**
- [ ] "Used By" section is accurate
- [ ] Related skills are linked (not duplicated)
- [ ] Instructions are procedural, not factual (factual content belongs in references)

**Reference files additionally:**
- [ ] Content is factual, not instructional
- [ ] Key Facts section is at the top
- [ ] Sections are short and skimmable
- [ ] "When Agents Should Consult This" section is accurate

---

## When to create a new file vs. extend an existing file

**Create a new file when:**
- A genuinely new agent, skill, or reference topic is needed
- An existing file would exceed ~300 lines if the content were added
- A section of an existing file is referenced independently by multiple other files
- The user explicitly requests a new file via contributor-request

**Extend an existing file when:**
- The new content is a natural elaboration of the existing topic
- The existing file is under ~300 lines
- The content does not introduce a new, separable concept

---

## Deprecation procedure

1. Change the file's status banner to `DEPRECATED`
2. Add to the deprecation notice: `Replaced by [new-file.md](path). Do not use for new work.`
3. Update all files that linked to the deprecated file to point to the replacement
4. Remove the file from `AGENTS.md` or `SKILLS.md` if applicable
5. Add a deprecation entry to `CHANGELOG.md`
6. After one review cycle with no active references, move to `archive/` subfolder and set status to `ARCHIVED`

---

## File size guideline

See [file-size-guidelines.md](file-size-guidelines.md) for when to split a file.

---

## What contributor must never do

- Edit the content of session notes (those are user-owned)
- Create files that duplicate existing content
- Add code, YAML, JSON, or non-Markdown content to the repo
- Leave a file in `draft` status indefinitely without a plan to complete it
