# File Size Guidelines

> **Status: ACTIVE** — Defines when a file should be split. Maintained by `contributor`.

---

## Why file size matters

Large files are hard to read, hard to navigate, and expensive to inject as AI context. A 600-line agent doc is not a better agent doc — it is a maintenance liability. Small, focused files are easier to update, easier to link, and easier for AI models to use effectively.

---

## Soft limits by file type

These are guidelines, not hard rules. Use judgment. The goal is clarity, not line-count compliance.

| File type | Soft limit | Notes |
|---|---|---|
| Agent files | ~300 lines | If procedural detail is growing, it belongs in a skill |
| Skill files | ~250 lines | If covering multiple distinct capabilities, split them |
| Workflow files | ~200 lines | If a workflow step is very detailed, link to a skill instead |
| Reference files | ~400 lines | Reference files can be denser; use subsections liberally |
| Governance files | ~300 lines | This file is an example of an appropriate length |
| Templates | ~100 lines | Templates should be minimal scaffolds, not filled-in examples |

---

## Signals that a file should be split

Beyond line count, split a file when:

- **The file is doing two things.** If you cannot name it in five words without using "and", it is doing two things.
- **A section is referenced independently by multiple other files.** That section deserves its own file.
- **The table of contents has more than seven top-level sections.** The file is too broad.
- **An agent doc contains step-by-step instructions longer than ~5 lines.** Those instructions are a skill.
- **A skill file covers two unrelated capabilities.** Split into two skill files.

---

## How to split a file

1. Identify the natural split point (usually a major section boundary).
2. Create the new file using the appropriate template.
3. Move the relevant content to the new file.
4. Replace the moved content in the original file with a brief summary and a link to the new file.
5. Update all cross-links in other files that referenced content now in the new file.
6. Update `AGENTS.md` or `SKILLS.md` if the new file is an agent or skill.
7. Add a note to `CHANGELOG.md`.

---

## What not to do

- Do not split a file just because it is approaching the soft limit. Split only when a clear conceptual boundary exists.
- Do not create a file so small it has no standalone value. A two-paragraph skill file should be a section in a related skill instead.
- Do not split a file and leave broken links behind. Validate all cross-links after splitting.
