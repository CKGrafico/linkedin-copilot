> **Status: ACTIVE** — This file is current and maintained.

# Skill: person-search

## What This Skill Does

Guides execution of an effective LinkedIn people search: selecting the right filters, interpreting result quality, identifying promising leads, and knowing when to refine vs. move on.

---

## Used By

- [sourcer](../agents/sourcer.md)

---

## When to Apply

After queries have been designed using [search-query-design](search-query-design.md) and the user is ready to execute the actual search. This skill governs what to do once results appear.

---

## Instructions

### 1. Set up the search correctly

Navigate to LinkedIn People search (not the main search bar, which mixes result types). Apply your Boolean query in the search bar, then layer in filters. Recommended filter order:
1. Geography (location filter)
2. Connection degree (1st, 2nd, 3rd+)
3. Current company or industry
4. Any recency signal if available (recently active, recently changed jobs)

### 2. Assess result quality on the first page

Before diving into individual profiles, scan the first page (10 results):
- Do the headlines match your target type?
- Is the seniority approximately right?
- Are you seeing obvious false positives?

If more than 30% of results are clearly wrong, refine the query before proceeding. Use [search-query-design](search-query-design.md).

### 3. Prioritize by connection degree

Within the same relevance level, prefer results in this order:
1. **2nd-degree connections** — shared connections create credibility for outreach
2. **1st-degree connections** — already connected, but may require a different approach
3. **3rd-degree or open profiles** — cold, lower response rate, but viable with strong personalization

### 4. Review each candidate profile

For each promising result, apply [profile-summary](profile-summary.md) to extract:
- Current role and company
- Career trajectory signals
- Activity signals (recent posts, comments, engagement)
- Connection degree and path
- Any shared context (school, former employer, group membership)

### 5. Apply sourcing heuristics

Consult [references/sourcing-heuristics.md](../references/sourcing-heuristics.md) to identify which profiles are worth prioritizing. Key signals include:
- Recent activity (posted or commented in last 30 days)
- Role type match (internal vs. agency recruiter, for example)
- Company growth signal
- Mutual connections

### 6. Build the candidate list

Record each viable candidate with:
- Name
- Current title and company
- Connection degree + path (if 2nd, who is the mutual?)
- Key signals (why this person is interesting)
- Recommended next action

Pass the list through [lead-ranking](lead-ranking.md) to prioritize.

### 7. Know when to stop

Stop when you have:
- 5–10 well-qualified candidates, OR
- Reviewed 50+ results with diminishing quality, OR
- Exhausted meaningful results in the current query

If the list is too thin, return to [search-query-design](search-query-design.md) and broaden the query.

---

## Input Requirements

- A ready-to-use Boolean query (from [search-query-design](search-query-design.md))
- Targeting criteria (type, seniority, geography, company)
- Any exclusion criteria

---

## Output Format

A candidate list with per-entry structure:
- **Name:** full name
- **Role:** current title at current company
- **Degree:** 1st / 2nd (mutual: [name]) / 3rd+
- **Key signals:** 1–3 bullet points on why this person is interesting
- **Next action:** outreach / research further / skip / monitor

---

## Related Skills

- [search-query-design](search-query-design.md) — prerequisite; designs the queries this skill executes
- [profile-summary](profile-summary.md) — used during candidate review
- [lead-ranking](lead-ranking.md) — used to prioritize the candidate list

---

## References

- [sourcing-heuristics](../references/sourcing-heuristics.md) — which signals indicate a valuable contact
- [search-patterns](../references/search-patterns.md) — reliable search patterns by use case
- [linkedin-usage-patterns](../references/linkedin-usage-patterns.md) — how search results are ranked and displayed
- [ethical-boundaries](../references/ethical-boundaries.md) — volume and behavior limits

---

## Notes and Caveats

- LinkedIn shows different results to different users. Your results depend on your network, premium status, and account history.
- Profiles with incomplete information may still be worth pursuing — do not automatically skip sparse profiles.
- Do not review more than ~100 profiles in a single session without a break. Quality of attention degrades.

---

## Maintenance Notes

Review when LinkedIn changes the People search interface, filters, or connection degree visibility.

Last reviewed: 2026-03-27
