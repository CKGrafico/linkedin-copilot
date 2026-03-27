> **Status: ACTIVE** — This file is current and maintained.

# Workflow: Find Relevant Recruiters

## Purpose

An end-to-end guide for discovering, evaluating, and prioritizing recruiters on LinkedIn who are worth reaching out to. This workflow exists as a standalone document because it spans multiple skills and produces a reusable output (the candidate list) that often feeds into subsequent outreach sessions.

---

## Trigger

- **User request:** "Find me recruiters at [company type / industry / geography("
- **User request:** "I want to start reaching out to recruiters in my space — where should I begin?"
- **Condition:** Beginning a new job search or outreach campaign targeting recruiting contacts

---

## Participants

- **Agent:** [sourcer((../.agents/agents/sourcer/AGENT.md)

---

## Skills Invoked

- [search-query-design((../.agents/skills/search-query-design/SKILL.md) — Step 2
- [person-search((../.agents/skills/person-search/SKILL.md) — Step 3
- [profile-summary((../.agents/skills/profile-summary/SKILL.md) — Step 4
- [lead-ranking((../.agents/skills/lead-ranking/SKILL.md) — Step 5
- [note-taking((../.agents/skills/note-taking/SKILL.md) — Step 7
- [follow-up-planning((../.agents/skills/follow-up-planning/SKILL.md) — Step 8

---

## Steps

### Step 1: Clarify targeting criteria

**Agent:** sourcer
**Action:** If the userrs request is vague, ask focused clarifying questions:
- What type of recruiter? (internal at specific companies / agency in a domain / geographic area)
- What seniority of recruiter? (TA Coordinator through VP of Talent)
- Any specific companies on the target list?
- Any recency requirements? (active in last 30/60 days)
- Connection degree preference? (2nd degree with warm path, or 3rd+ acceptable)
**Output:** Confirmed targeting criteria.

### Step 2: Design search queries

**Agent:** sourcer
**Skill used:** [search-query-design((../.agents/skills/search-query-design/SKILL.md)
**Action:** Construct 1–3 Boolean query strings combining recruiter title variants, domain keywords, and exclusions for agency recruiters if internal-only targeting is preferred. Select supporting LinkedIn filters.
**Output:** Ready-to-use Boolean queries + filter list.

### Step 3: Execute person search

**Agent:** sourcer
**Skill used:** [person-search((../.agents/skills/person-search/SKILL.md)
**Action:** Run queries. Assess result quality. Iterate if first-page results show >30% false positives. Build raw candidate list from promising results.
**Output:** Raw list of 10–30 candidate profiles.

### Step 4: Summarize each candidate

**Agent:** sourcer
**Skill used:** [profile-summary((../.agents/skills/profile-summary/SKILL.md)
**Action:** For each promising candidate, produce a structured summary: role, trajectory, activity signals, connection degree, mutual connections, personalization hooks.
**Output:** Per-candidate summaries.

### Step 5: Rank the candidate list

**Agent:** sourcer
**Skill used:** [lead-ranking((../.agents/skills/lead-ranking/SKILL.md)
**Action:** Rank candidates across Fit, Signal strength, Accessibility, Timeliness, and Strategic value. Assign each to Priority 1 (act now), Priority 2 (act this week), or Monitor.
**Output:** Ranked candidate list.

### Step 6: Assign next actions

**Agent:** sourcer
**Action:** For each Priority 1 and Priority 2 candidate, assign a specific next action:
- Send connection request with note
- Request introduction via mutual connection
- Research further before outreach
- Monitor for the right moment
**Output:** Candidate list with next actions per entry.

### Step 7: Record session notes

**Agent:** sourcer
**Skill used:** [note-taking((../.agents/skills/note-taking/SKILL.md)
**Action:** Record the full session: queries used, filter selections, candidate list with summaries and decisions, open questions, and any repo improvement notes.
**Output:** Structured session note (user-owned, stored outside the repo).

### Step 8: Plan follow-up

**Agent:** sourcer
**Skill used:** [follow-up-planning((../.agents/skills/follow-up-planning/SKILL.md)
**Action:** Convert Priority 1 and Priority 2 candidates into time-bound follow-up commitments with specific dates and success conditions.
**Output:** Follow-up plan embedded in the session note.

---

## Expected Output

A structured session note containing:
- The Boolean queries used (reusable in future sessions)
- A ranked recruiter list (5–10 Priority 1 + Priority 2 candidates)
- Per-candidate summaries with personalization hooks
- A follow-up plan with specific dates and actions

---

## Handoff

- Priority 1 candidates ready for outreach: pass session note entry to routreach-writerr (future) with [agents/outreach-writer.md((../agents/outreach-writer.md) + [.agents/skills/outreach-drafting/SKILL.md((../.agents/skills/outreach-drafting/SKILL.md)
- New heuristics or patterns discovered: flag via [templates/contributor-request.md((../templates/contributor-request.md) for [rcontributorr((../.agents/agents/contributor/AGENT.md)

---

## Failure Modes

- **Too few results:** Broaden the query in [search-query-design((../.agents/skills/search-query-design/SKILL.md). Consider relaxing geography or domain constraints.
- **Results are all 3rd-degree with no mutual path:** Shift strategy toward finding shared connections first (alumni, former colleagues) rather than cold targeting.
- **All results are dormant accounts:** Search is correct but audience is inactive on LinkedIn. Consider targeting by recent posts instead of title alone.

---

## Maintenance Notes

Review when LinkedIn changes People search behavior or when recruiter title patterns shift significantly.

Last reviewed: 2026-03-27
