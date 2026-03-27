> **Status: ACTIVE** — This file is current and maintained.

# Skill: job-search

## What This Skill Does

Guides execution of an effective LinkedIn Jobs search: selecting filters, evaluating posting quality and freshness, filtering out noise, and identifying real opportunities worth pursuing.

---

## Used By

- [headhunter](../agents/headhunter.md)

---

## When to Apply

After job search queries have been designed using [search-query-design](search-query-design.md) and the user is ready to execute the search in LinkedIn Jobs. This skill governs what to do once results appear.

---

## Instructions

### 1. Use LinkedIn Jobs, not the main search bar

Navigate to LinkedIn Jobs directly (`linkedin.com/jobs`). The main search bar returns mixed results and less granular filtering. LinkedIn Jobs provides better recency filters, applicant count signals, and job-specific facets.

### 2. Apply filters immediately

Before reviewing results, apply these filters in order:

1. **Date posted:** Start with "Past week." If results are too thin, expand to "Past month." Do not start with "Any time" — old postings waste time.
2. **Experience level:** Match your target seniority. Do not skip this; titles alone are unreliable.
3. **Job type:** Full-time unless you are explicitly open to contract or part-time.
4. **Remote:** Set to your actual preference (on-site / hybrid / remote). Do not leave this open unless you genuinely are.
5. **Company size:** Apply if you have a preference.

### 3. Scan the first page for signal quality

Review the first 10 results:
- Are the job titles roughly matching your target?
- Are the companies recognizable or at least real-sounding?
- Are posting dates recent (within your filter)?

If quality is low, refine the query. Use [search-query-design](search-query-design.md).

### 4. Evaluate each promising posting

For each result that passes the initial scan, evaluate:

**Posting freshness signals:**
- How long has it been posted? (newer is better; >60 days old is a concern)
- How many applicants? (0–25: early and uncrowded; 26–100: normal; 100+: competitive or old)
- Is it marked "Easy Apply"? (can signal low-effort volume sourcing, but not always)

**Description quality signals:**
- Is the description specific about what the role actually does day-to-day?
- Does it name a real team, manager, or reporting structure?
- Are salary or compensation ranges listed? (positive signal for transparency)
- Does it read like it was written for this specific role, or is it a recycled template?

**Company legitimacy signals:**
- Does the company have an active LinkedIn page with real employees?
- Is the headcount believable for the stated company stage?
- Has the company posted other jobs recently? (confirms active hiring)

### 5. Check for ghost postings

A ghost posting is a job that is no longer active but has not been removed. Signals:
- Posted more than 45 days ago
- Very high applicant count with no "actively reviewing" signal
- No response to applications (if you have tried before)
- Company has no recent activity on LinkedIn

When in doubt, note it as a possible ghost posting in your session notes.

### 6. Build the opportunity list

Record each viable opportunity:
- Job title
- Company
- Location / remote status
- Posting date
- Applicant count (if visible)
- Fit assessment (initial)
- Red flags or questions

Pass the list to [opportunity-qualification](opportunity-qualification.md) for deeper evaluation.

---

## Input Requirements

- Ready-to-use Boolean query (from [search-query-design](search-query-design.md))
- Role targets, seniority, geography, remote preference
- Any company or industry preferences or exclusions

---

## Output Format

A raw opportunity list, to be qualified further:
- **Title:** job title
- **Company:** company name
- **Posted:** date or relative freshness
- **Applicants:** count (if visible)
- **Initial fit:** brief note on why it looks promising or concerning
- **Red flags:** any ghost posting signals or description issues

---

## Related Skills

- [search-query-design](search-query-design.md) — prerequisite; designs the queries this skill executes
- [opportunity-qualification](opportunity-qualification.md) — next step; evaluates each result in depth
- [company-research](company-research.md) — used when a company needs deeper investigation

---

## References

- [job-search-heuristics](../references/job-search-heuristics.md) — what makes a posting worth pursuing
- [recruiter-signals](../references/recruiter-signals.md) — reading company hiring activity patterns
- [search-patterns](../references/search-patterns.md) — reliable search patterns by use case

---

## Notes and Caveats

- LinkedIn Jobs results depend on your profile. A well-optimized profile gets better results.
- "Easy Apply" does not mean low effort on your end — it means low friction to submit. Quality of fit still matters.
- The applicant count shown is a trailing indicator. A post may have many applicants and still be worth applying to if it is a strong fit.

---

## Maintenance Notes

Review when LinkedIn changes the Jobs interface, filter options, or posting quality indicators.

Last reviewed: 2026-03-27
