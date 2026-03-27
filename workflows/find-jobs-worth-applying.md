> **Status: ACTIVE** — This file is current and maintained.

# Workflow: Find Jobs Worth Applying To

## Purpose

An end-to-end guide for discovering, qualifying, and prioritizing job opportunities on LinkedIn. This workflow exists as a standalone document because it involves multiple skills in sequence and produces a reusable output (the ranked opportunity list) that is the foundation for subsequent application or outreach sessions.

---

## Trigger

- **User request:** "Find me jobs that match my profile and preferences"
- **User request:** "I want to start a job search — where do I begin?"
- **Condition:** Beginning a new active job search campaign

---

## Participants

- **Agent:** [headhunter](../.github/instructions/agents/headhunter.instructions.md)

---

## Skills Invoked

- [search-query-design](../.github/instructions/skills/search-query-design.instructions.md) — Step 2
- [job-search](../.github/instructions/skills/job-search.instructions.md) — Step 3
- [opportunity-qualification](../.github/instructions/skills/opportunity-qualification.instructions.md) — Step 4
- [company-research](../.github/instructions/skills/company-research.instructions.md) — Step 5
- [lead-ranking](../.github/instructions/skills/lead-ranking.instructions.md) — Step 6
- [note-taking](../.github/instructions/skills/note-taking.instructions.md) — Step 8
- [follow-up-planning](../.github/instructions/skills/follow-up-planning.instructions.md) — Step 9

---

## Steps

### Step 1: Clarify criteria

**Agent:** headhunter
**Action:** Confirm the user's search parameters before designing queries:
- Target role titles (be inclusive — ask about lateral roles they might not have considered)
- Target industries or domains
- Location / remote preference
- Seniority level
- Company size / stage preference
- Hard non-negotiables (compensation floor if known, relocation constraints, etc.)
- Nice-to-haves
**Output:** Confirmed targeting criteria.

### Step 2: Design job search queries

**Agent:** headhunter
**Skill used:** [search-query-design](../.github/instructions/skills/search-query-design.instructions.md)
**Action:** Build Boolean queries for LinkedIn Jobs combining role title variants, domain keywords, and seniority signals. Identify the filter set to apply (recency, experience level, remote, company size).
**Output:** 1–3 ready-to-use Boolean queries + filter list.

### Step 3: Execute job search

**Agent:** headhunter
**Skill used:** [job-search](../.github/instructions/skills/job-search.instructions.md)
**Action:** Run queries in LinkedIn Jobs. Apply filters. Assess result quality on the first page. Build a raw opportunity list of results that pass the initial scan.
**Output:** Raw opportunity list (10–25 postings).

### Step 4: Qualify each opportunity

**Agent:** headhunter
**Skill used:** [opportunity-qualification](../.github/instructions/skills/opportunity-qualification.instructions.md)
**Action:** Apply hard filters to eliminate clear mismatches (role, location, non-negotiables, legitimacy, freshness). Score remaining opportunities on description quality, company signals, fit, and accessibility. Assign a decision: Apply now / Apply soon / Monitor / Research further / Skip.
**Output:** Qualified opportunity list with decisions.

### Step 5: Research companies behind strong leads

**Agent:** headhunter
**Skill used:** [company-research](../.github/instructions/skills/company-research.instructions.md)
**Action:** For each "Apply now" and "Research further" opportunity, produce a company snapshot: headcount signals, job posting activity, company page content, leadership stability, strategic fit.
**Output:** Company snapshots attached to relevant opportunity entries.

### Step 6: Rank qualified opportunities

**Agent:** headhunter
**Skill used:** [lead-ranking](../.github/instructions/skills/lead-ranking.instructions.md)
**Action:** Rank the qualified opportunity list across Role fit, Company fit, Opportunity quality, Accessibility, and Timing. Assign Priority 1 (apply now), Priority 2 (apply soon), or Monitor.
**Output:** Ranked opportunity list.

### Step 7: Assign next actions

**Agent:** headhunter
**Action:** For each Priority 1 and Priority 2 opportunity:
- Identify whether an internal connection exists (if yes: warm application path)
- Note the application method (Easy Apply vs. company website vs. direct contact)
- Flag any opportunities where identifying a hiring manager via [`sourcer`](../.github/instructions/agents/sourcer.instructions.md) would improve the approach
**Output:** Opportunity list with next actions per entry.

### Step 8: Record session notes

**Agent:** headhunter
**Skill used:** [note-taking](../.github/instructions/skills/note-taking.instructions.md)
**Action:** Record the full session: queries, filters, opportunity list with qualifications and decisions, open questions, company snapshots.
**Output:** Structured session note (user-owned).

### Step 9: Plan follow-up

**Agent:** headhunter
**Skill used:** [follow-up-planning](../.github/instructions/skills/follow-up-planning.instructions.md)
**Action:** Convert Priority 1 and Priority 2 opportunities into time-bound commitments: apply by [date], follow up after [date] if no ATS confirmation, check-in on "Monitor" items in [N] days.
**Output:** Follow-up plan embedded in the session note.

---

## Expected Output

A structured session note containing:
- The Boolean queries used
- A ranked opportunity list (5–10 Priority 1 + Priority 2 opportunities)
- Company snapshots for strong leads
- Per-opportunity qualification decisions with rationale
- A follow-up plan with specific dates

---

## Handoff

- Opportunities requiring a warm contact: pass session note entry to [`sourcer`](../.github/instructions/agents/sourcer.instructions.md) to find a hiring manager or internal connection
- Opportunities requiring deeper company research: pass to `company-scout` (future) or `researcher` (future)
- Multiple opportunities needing comparison: run [workflows/compare-opportunities.md](compare-opportunities.md)
- New job posting patterns discovered: flag via [templates/contributor-request.md](../templates/contributor-request.md) for [`contributor`](../.github/instructions/agents/contributor.instructions.md)

---

## Failure Modes

- **Too few results:** Broaden queries. Expand role title list. Expand geography. Lower seniority ceiling or floor.
- **All results are old postings:** Tighten the Date posted filter. Consider that the market may be slower right now for this role type.
- **High ghost posting rate:** This happens. Focus on freshness signals and company activity as filters. Prioritize companies with multiple recent postings.

---

## Maintenance Notes

Review when LinkedIn Jobs interface or filter options change significantly.

Last reviewed: 2026-03-27
