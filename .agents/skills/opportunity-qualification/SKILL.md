> **Status: ACTIVE** — This file is current and maintained.

# Skill: opportunity-qualification

## What This Skill Does

Evaluates whether a job posting or professional opportunity is worth pursuing given the user's stated criteria, applying a structured rubric to separate real opportunities from noise.

---

## Used By

- [headhunter](../../agents/headhunter/AGENT.md)

---

## When to Apply

After initial job search results have been gathered using [job-search](./`job-search.instructions.md), before ranking. This skill takes raw results and determines which ones deserve further investment of time.

---

## Instructions

### 1. Apply the hard filters first

These are binary pass/fail checks. If a posting fails any hard filter, mark it **Skip** and move on.

- [ ] **Role match:** Does the job title and description match the user's target role type at the stated seniority level?
- [ ] **Location match:** Is the location (or remote status) within the user's stated constraints?
- [ ] **Non-negotiables:** Does the posting satisfy all hard filters the user specified (e.g., minimum compensation if stated, no relocation required)?
- [ ] **Company legitimacy:** Is the company real, verifiable, and actively operating? (Check LinkedIn company page — does it exist? Does it have employees?)
- [ ] **Posting freshness:** Was it posted within the user's acceptable window? (Default: reject anything older than 45 days without other strong signals.)

### 2. Score the opportunity on soft signals

For postings that pass hard filters, evaluate these quality signals. This is not a numeric score — use judgment to produce a **Strong / Moderate / Weak** overall rating.

**Description quality**
- Does the description clearly explain what the person will actually do day-to-day? (Specific > vague)
- Is the team, reporting structure, or manager mentioned?
- Are compensation or salary ranges listed? (Positive signal for transparency)
- Does it sound like it was written for this specific role, or is it a recycled template?

**Company signals**
- Is the company growing? (LinkedIn headcount trend, recent hires visible)
- Is the company actively hiring across multiple roles? (Suggests real growth, not a single ghost post)
- Does the company page have recent posts and employee engagement?
- Are there any negative signals? (Mass layoffs, no recent activity, suspiciously high job posting volume)

**Fit signals**
- Does your background map well to the requirements?
- Are the required skills a strong match, partial match, or stretch?
- Is the role a logical next step in your career trajectory?

**Accessibility signals**
- Do you have any connections at this company? (Warm application is 3–5× more effective)
- Is there a recruiter or hiring manager visible on LinkedIn?
- Is the company responsive to outreach (based on past signals if available)?

### 3. Assign a qualification decision

Based on hard filters and soft signal rating:

- **Apply now:** Strong fit, fresh posting, real company, accessible.
- **Apply soon:** Good fit, minor concerns (slightly old, no internal contact), worth acting on this week.
- **Monitor:** Interesting but something is unclear or a concern exists. Re-evaluate in 7 days.
- **Research further:** Looks promising but needs more information before deciding (use [company-research](./`company-research.instructions.md)).
- **Skip:** Failed hard filter, or soft signals are predominantly negative.

### 4. Document the qualification

Record each decision in session notes using [note-taking](./`note-taking.instructions.md):
- Opportunity name and company
- Qualification decision and 1-sentence rationale
- Any flags or open questions

---

## Input Requirements

- The job posting content: title, company, description, requirements, date posted, applicant count (if visible)
- The user's stated criteria: target roles, non-negotiables, nice-to-haves, location constraints

---

## Output Format

For each opportunity:
```
Title: [Job Title] at [Company]
Decision: Apply now / Apply soon / Monitor / Research further / Skip
Rationale: [1–2 sentences]
Flags: [any concerns or open questions]
```

---

## Related Skills

- [job-search](./`job-search.instructions.md) — produces the raw results this skill qualifies
- [company-research](./`company-research.instructions.md) — used when "Research further" decision is made
- [lead-ranking](./`lead-ranking.instructions.md) — used after qualification to prioritize the "apply" list

---

## References

- [job-search-heuristics](../../../references/job-search-heuristics.md) — detailed signals for posting quality
- [company-evaluation-criteria](../../../references/company-evaluation-criteria.md) — how to assess a company

---

## Notes and Caveats

- Hard filters are non-negotiable. Do not rationalize applying to a posting that fails a hard filter.
- A "Monitor" decision is not indefinite. Set a specific date to revisit, and skip if nothing has changed.
- The "Apply now" decision is a recommendation, not a commitment. The user decides whether to act.
- Ghost postings are a real and common problem. When in doubt, treat a 45+ day old posting as suspect.

---

## Maintenance Notes

Review when job market dynamics shift significantly (e.g., a recession causing more ghost postings, or new LinkedIn features that indicate active review).

Last reviewed: 2026-03-27
