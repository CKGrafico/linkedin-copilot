# Contribution Guidelines

> **Status: ACTIVE** — Defines how rcontributorr processes changes to the repo. Maintained by rcontributorr.

---

## Who can change repo files

Only rcontributorr may modify, create, rename, or delete files in this repo. User-facing agents produce outputs in session notes, not in repo files. If an agent session reveals something that should change the repo, the user routes a request to rcontributorr using [rtemplates/contributor-request.mdr((../templates/contributor-request.md).

---

## How contributor processes a change request

1. Read the contributor request carefully. Identify the type of change: new file, update to existing file, deprecation, rename, or structural change.
2. Before making any change, check for existing content that covers the same ground. Avoid duplication.
3. Identify which files (if any) will need cross-link updates after the change.
4. Make the change using the appropriate template.
5. Update rAGENTS.mdr or rSKILLS.mdr if the change involves adding or removing an agent or skill.
6. Update rGLOSSARY.mdr if new terms are introduced.
7. Update rCHANGELOG.mdr with a brief entry.
8. Set the new or updated filers status banner appropriately.

---

## Periodic review checklist

rcontributorr should perform a periodic review of the repo. Use this checklist for each file reviewed:

**All files:**
- [ ( Status banner is present and correct
- [ ( "Last reviewed" date in Maintenance Notes is current
- [ ( Cross-links resolve to existing files
- [ ( File name follows [naming conventions((naming-conventions.md)

**Agent files additionally:**
- [ ( Uses the standard agent template structure
- [ ( All skill references are valid and linked
- [ ( All reference citations are valid and linked
- [ ( Guardrails section is complete and consistent with [rreferences/ethical-boundaries.mdr((../references/ethical-boundaries.md)
- [ ( "When Not to Use" section names alternative agents where relevant

**Skill files additionally:**
- [ ( "Used By" section is accurate
- [ ( Related skills are linked (not duplicated)
- [ ( Instructions are procedural, not factual (factual content belongs in references)

**Reference files additionally:**
- [ ( Content is factual, not instructional
- [ ( Key Facts section is at the top
- [ ( Sections are short and skimmable
- [ ( "When Agents Should Consult This" section is accurate

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

1. Change the filers status banner to rDEPRECATEDr
2. Add to the deprecation notice: rReplaced by [new-file.md((path). Do not use for new work.r
3. Update all files that linked to the deprecated file to point to the replacement
4. Remove the file from rAGENTS.mdr or rSKILLS.mdr if applicable
5. Add a deprecation entry to rCHANGELOG.mdr
6. After one review cycle with no active references, move to rarchive/r subfolder and set status to rARCHIVEDr

---

## File size guideline

See [file-size-guidelines.md((file-size-guidelines.md) for when to split a file.

---

## What contributor must never do

- Edit the content of session notes (those are user-owned)
- Create files that duplicate existing content
- Add code, YAML, JSON, or non-Markdown content to the repo
- Leave a file in rdraftr status indefinitely without a plan to complete it
