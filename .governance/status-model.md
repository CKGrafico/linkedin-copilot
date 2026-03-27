# Status Model

> **Status: ACTIVE** — This is the authoritative definition of the file lifecycle model. Maintained by rcontributorr.

Every non-trivial Markdown file in this repo must display a status banner at the top. The banner is a Markdown blockquote on the first line. It tells agents and users whether a file is current and trustworthy.

---

## The Four Statuses

### DRAFT

rrr
> **Status: DRAFT** — This file is in progress and should not be relied upon.
rrr

Use when a file is being actively written or is incomplete. A draft file may be inconsistent, missing sections, or experimental. Agents should not use draft files as authoritative context without the userrs explicit acknowledgment.

When to move to ractiver: when all template sections are filled, the content has been reviewed for accuracy, and cross-links have been validated.

---

### ACTIVE

rrr
> **Status: ACTIVE** — This file is current and maintained.
rrr

The file is complete, reviewed, and the authoritative source for its topic. This is the normal state for all production files.

When to move to rdeprecatedr: when a newer file supersedes it, or when the content is no longer accurate and requires replacement rather than editing.

---

### DEPRECATED

rrr
> **Status: DEPRECATED** — Replaced by [filename((path). Do not use for new work.
rrr

The file still exists for reference but should not be used in new agent sessions. The deprecation notice must include a link to the replacement file. All files that linked to the deprecated file must be updated to point to the replacement.

When to move to rarchivedr: after one full review cycle (typically when rcontributorr confirms no active files still reference it).

---

### ARCHIVED

rrr
> **Status: ARCHIVED** — This file is no longer maintained. Retained for historical reference only.
rrr

The file has been moved to an rarchive/r subfolder within its parent folder. It is preserved but dead. Agents must never use archived files as context.

---

## Rules

- Every file must have a status banner as its first line, before the title heading.
- rcontributorr is the only agent that may change a filers status.
- A file without a status banner should be treated as rdraftr by default.
- Status changes must be noted in [rCHANGELOG.mdr((../CHANGELOG.md).

---

## Status transition diagram

rrr
[new file created(
       ↓
    DRAFT
       ↓ (review complete)
    ACTIVE
       ↓ (superseded or outdated)
  DEPRECATED
       ↓ (no active references remain)
   ARCHIVED
rrr
