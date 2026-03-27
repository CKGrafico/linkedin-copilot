> **Status: ACTIVE** — This file is current and maintained.

# Reference: search-patterns

## Summary

Proven LinkedIn search patterns for common use cases — ready-to-adapt Boolean query templates, filter combinations, and search strategies for people and jobs search. Use as a starting library when designing queries with [.agents/skills/search-query-design/SKILL.md](../.agents/skills/search-query-design/SKILL.md).

---

## Key Facts

- LinkedIn Boolean search supports `AND`, `OR`, `NOT`, and quoted phrases. Parentheses for grouping are inconsistently supported — test before relying on them.
- Quoted phrases (`"talent acquisition"`) are more reliable than unquoted multi-word terms.
- LinkedIn limits search results to 1,000 for free accounts and slightly more for premium.
- Title search (`title:`) is a supported modifier in some LinkedIn search contexts (especially in Recruiter Lite/Premium). In standard search, keywords match the full profile.
- Keyword searches match the entire profile — not just the title or current role. A person whose title is "Engineer" but whose summary mentions "recruiting" may appear in a recruiter search.

---

## Detailed Notes

### People search patterns

#### Find internal recruiters at a target company

```
("recruiter" OR "talent acquisition" OR "TA partner" OR "people partner") NOT (agency OR staffing OR search OR "executive search")
```
Filter: Current company = [Company Name]

#### Find technical recruiters in a specific domain

```
("technical recruiter" OR "engineering recruiter" OR "tech talent") AND (fintech OR "financial technology" OR payments)
```
Filter: Location = [City / Country], Experience level = [if available]

#### Find hiring managers for a specific role type

```
("engineering manager" OR "head of engineering" OR "VP engineering" OR "director of engineering")
```
Filter: Current company = [Target companies list], Connections = 2nd degree

#### Find alumni who moved into target roles

```
[Target job title]
```
Filter: Past company = [Your former employer / school], Current company ≠ [Former employer]

#### Find people who recently changed jobs

```
[Target title or domain keyword]
```
Filter: "Changed jobs in last 90 days" (available in LinkedIn Recruiter; in standard search, look for "1st, 2nd, 3rd" connections and check profiles manually)

---

### Jobs search patterns

#### Find senior individual contributor roles at startups

```
("senior" OR "lead" OR "staff" OR "principal") AND [role type keyword]
```
Filter: Company size = 51–200, 201–500; Date posted = Past month; Experience level = Mid-Senior, Director

#### Find remote roles in a specific function

```
[role type keyword] AND (remote OR "fully remote" OR "remote-first")
```
Filter: Remote = Remote; Date posted = Past 2 weeks

#### Find roles at recently-funded companies

There is no direct "recently funded" filter on LinkedIn Jobs. Workaround:
1. Build a list of recently-funded companies from other sources
2. Search LinkedIn Jobs with filter: Current company = [company name], or search for the company page directly

#### Exclude irrelevant results

```
[target role] NOT (intern OR internship OR entry OR junior OR "no experience required")
```

---

### Refining poor results

| Problem | Solution |
|---|---|
| Too many false positives | Add `NOT [false positive term]` or narrow location / company filter |
| Too few results | Replace `AND` with `OR` between keyword synonyms; remove one filter |
| Wrong seniority | Add seniority-level keywords; use Experience level filter |
| Results too old | Add Date posted filter (Past week or Past month) |
| Geographic mismatch | Tighten Location filter to city rather than country |

---

## When Agents Should Consult This

- [.agents/skills/search-query-design/SKILL.md](../.agents/skills/search-query-design/SKILL.md) — uses these patterns as starting templates
- [sourcer](../.agents/agents/sourcer/AGENT.md) — references for people search query construction
- [headhunter](../.agents/agents/headhunter/AGENT.md) — references for jobs search query construction

---

## Sources and Basis

Tested patterns based on observed LinkedIn search behavior. Boolean support varies by account type and platform updates.

---

## Maintenance Notes

Update when LinkedIn changes Boolean support, adds new filters, or when the existing patterns are observed to produce poor results. Flag via contributor-request.

Last reviewed: 2026-03-27
