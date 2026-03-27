# Handoff Conventions

> **Status: ACTIVE** — Defines how agents pass outputs to each other. Maintained by `contributor`.

Agents in this repo do not call each other programmatically. Handoffs happen through structured session notes and explicit output formats. This document defines how handoffs work so that any agent can pick up where another left off.

---

## Core principle

An agent session produces a **session note** (see [.agents/skills/note-taking/SKILL.md](../.agents/skills/note-taking/SKILL.md)). That note is the unit of handoff. The next agent receives that note as context at the start of its session.

The repo provides the **cognitive scaffold**. The session note provides the **runtime state**. Together, they give the next agent everything it needs.

---

## Standard handoff package

When handing off between agents, the user assembles:

1. The **receiving agent's file** (`agents/receiving-agent.md`)
2. The **session note** from the previous agent session
3. Any **skill files** referenced in the workflow step
4. Any **reference files** relevant to the next step

The user then opens a new AI conversation with these files as context.

---

## Named handoff types

### Sourcer → Outreach-writer

**Trigger:** `sourcer` has identified a specific person worth contacting.

**What to pass:**
- Session note including: person's name, role, company, rationale, and any observed personalization hooks
- `agents/outreach-writer.md`
- `.agents/skills/outreach-drafting/SKILL.md`
- `.agents/skills/message-personalization/SKILL.md`

**Expected input format:** The note entry for the person, formatted per `note-taking` skill.

---

### Headhunter → Researcher (future)

**Trigger:** `headhunter` has identified a company or role worth investigating in depth.

**What to pass:**
- Session note including: company name, role, initial fit assessment, and open questions
- `agents/researcher.md`
- `.agents/skills/company-research/SKILL.md`

---

### Sourcer / Headhunter → Contributor

**Trigger:** An agent session has revealed something that should update the repo (a new heuristic, a changed LinkedIn pattern, a missing skill).

**What to pass:**
- Filled-in `templates/contributor-request.md`
- Description of the issue and the proposed change

This is the only handoff that results in repo edits.

---

## Rules

- Handoffs are always initiated by the **user**, not by agents.
- An agent must never assume it has access to another agent's internal state. Every session starts fresh from files and notes.
- If a handoff requires information that was not captured in the session note, the previous agent's session must be resumed or reconstructed.
- Handoff rules for each agent are also documented in the agent's own **Handoff Rules** section.

---

## What agents must not hand off

- Direct instructions to edit repo files. Route all repo changes through `contributor`.
- Partial or unreviewed session notes. Notes passed as context should be complete and structured.
- Raw, unprocessed lists. Outputs should be ranked and annotated before handoff.
