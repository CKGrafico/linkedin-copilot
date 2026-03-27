> **Status: ACTIVE** — This file is current and maintained.

# Skill: person-search

## What This Skill Does

Executes an effective LinkedIn people search using Browser MCP — navigating to LinkedIn, entering queries, applying filters, reading results, and building a candidate list from what is found.

---

## Used By

- [sourcer](../../agents/sourcer/AGENT.md)

---

## When to Apply

After queries have been designed using [search-query-design](./`search-query-design.instructions.md). Requires Browser MCP to be active and LinkedIn to be open in the browser. See [browser-navigation](./`browser-navigation.instructions.md) for setup.

---

## Instructions

### 1. Open LinkedIn People search

```
navigate: https://www.linkedin.com/search/results/people/
wait: 2
snapshot
```

Confirm the People search page is loaded (you will see a search bar and filter options).

### 2. Enter the search query

```
click: [search bar / keywords input]
type: [Boolean query from search-query-design]
press_key: Enter
wait: 3
snapshot
```

### 3. Apply filters

After the initial results load, apply filters in this order. For each filter:
```
click: [filter button label]
wait: 1
snapshot
[select option]
wait: 2
snapshot
```

Recommended filter order:
1. **Connections** — select 2nd degree first; expand to 3rd+ if results are thin
2. **Locations** — enter the target city or region
3. **Current company** — if targeting specific companies
4. **All filters → Industry** — if domain filtering is needed

### 4. Assess first-page quality

Read the snapshot of the first results page. Scan the 10 visible results:
- Do the headlines match the target type?
- Is seniority approximately right?
- More than 3 obvious false positives? Refine the query and re-run.

### 5. Collect results — iterate through profiles

For each promising result on the page, open the profile and summarize it:

```
click: [person's name link]
wait: 2
snapshot
```

Apply [profile-summary](./`profile-summary.instructions.md) to extract: role, trajectory, activity, connection degree, mutual connections, hooks.

Then return to results:
```
go_back
wait: 2
snapshot
```

Repeat for each promising result. Skip profiles that are clearly mismatched based on the headline alone — do not open every profile.

### 6. Paginate if needed

After reviewing all results on the current page:
```
click: Next
wait: 3
snapshot
```

Continue until you have 5–10 qualified candidates or have reviewed 3 pages with diminishing quality.

### 7. Prioritize by connection degree

Within the same relevance level, prefer:
1. **2nd-degree** with a strong mutual you know well
2. **1st-degree** (already connected)
3. **3rd-degree or open profiles**

### 8. Build the candidate list

Record each viable candidate using the output format below. Pass through [lead-ranking](./`lead-ranking.instructions.md) to prioritize.

### 9. Know when to stop

Stop when you have:
- 5–10 well-qualified candidates, OR
- Reviewed 3+ pages with diminishing quality, OR
- Exhausted results for the current query

If the list is too thin, return to [search-query-design](./`search-query-design.instructions.md) and broaden.

---

## Input Requirements

- A ready-to-use Boolean query (from [search-query-design](./`search-query-design.instructions.md))
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

- [browser-navigation](./`browser-navigation.instructions.md) — foundational browser operation patterns used throughout this skill
- [search-query-design](./`search-query-design.instructions.md) — prerequisite; designs the queries this skill executes
- [profile-summary](./`profile-summary.instructions.md) — used during candidate review
- [lead-ranking](./`lead-ranking.instructions.md) — used to prioritize the candidate list

---

## References

- [browser-mcp](../../../.references/browser-mcp.md) — available browser tools and LinkedIn URL patterns
- [sourcing-heuristics](../../../.references/sourcing-heuristics.md) — which signals indicate a valuable contact
- [search-patterns](../../../.references/search-patterns.md) — reliable search patterns by use case
- [linkedin-usage-patterns](../../../.references/linkedin-usage-patterns.md) — how search results are ranked and displayed
- [ethical-boundaries](../../../.references/ethical-boundaries.md) — volume and behavior limits for automated sessions

---

## Notes and Caveats

- LinkedIn shows different results to different users. Your results depend on your network, premium status, and account history.
- Profiles with incomplete information may still be worth pursuing — do not automatically skip sparse profiles.
- Do not review more than ~100 profiles in a single session without a break. Quality of attention degrades.

---

## Maintenance Notes

Review when LinkedIn changes the People search interface, filters, or connection degree visibility.

Last reviewed: 2026-03-27
