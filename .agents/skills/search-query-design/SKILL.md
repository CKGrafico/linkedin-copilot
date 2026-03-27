> **Status: ACTIVE** — This file is current and maintained.

# Skill: search-query-design

## What This Skill Does

Teaches how to construct effective LinkedIn search queries using Boolean logic, keyword strategy, filter selection, and exclusion patterns — applicable to both People search and Jobs search.

---

## Used By

- [sourcer](../../agents/sourcer/AGENT.md)
- [headhunter](../../agents/headhunter/AGENT.md)

---

## When to Apply

Apply this skill at the start of any search session, before executing the actual search. Good query design determines the quality of everything that follows. A poorly designed query returns noise; a well-designed query returns signal.

---

## Instructions

### 1. Define the target clearly

Before writing a single query, answer these questions:
- What is the exact type of person or job I am looking for?
- What are the clearest distinguishing signals of a good result?
- What are the most common false positives I need to exclude?

### 2. Choose your primary keyword anchors

Identify 2–4 core terms that strong results will reliably contain. For people: job titles, domain keywords, seniority terms. For jobs: role titles, required skills, company type signals.

### 3. Build a Boolean query

Combine keywords using Boolean operators:
- `AND` — both terms must be present (narrows results)
- `OR` — either term is acceptable (broadens results, use for synonyms)
- `NOT` — exclude results containing this term

Example for a recruiter search:
```
("technical recruiter" OR "engineering recruiter" OR "talent acquisition") AND (fintech OR "financial technology") NOT agency
```

Example for a job search:
```
("product manager" OR "product lead") AND (B2B OR SaaS) AND (senior OR "lead" OR "principal") NOT "entry level"
```

### 4. Use LinkedIn filters to narrow

Boolean queries work best combined with LinkedIn's built-in filters:
- **People search filters:** connections (1st/2nd/3rd+), location, current company, past company, industry, school
- **Jobs filters:** date posted, experience level, company size, job type (full-time/contract), remote

Use filters to eliminate noise that Boolean alone cannot catch. Apply geography, recency, and seniority filters before reviewing results.

### 5. Test and iterate

Run the query. Review the top 10 results.
- Too many false positives? Tighten with AND or NOT.
- Too few results? Loosen with OR or remove a filter.
- Wrong seniority? Adjust title keywords or use the experience level filter.

Expect to iterate 2–3 times before the query is well-calibrated.

### 6. Document your final query

Record the final working query in your session notes (see [note-taking](./`note-taking.instructions.md)). Good queries are reusable.

---

## Input Requirements

- A clear description of the target (person type or job type)
- Any hard constraints (geography, company type, seniority)
- Any known false positive patterns to exclude

---

## Output Format

- One or more Boolean query strings, ready to paste into LinkedIn search
- A brief explanation of the design choices made
- Recommended LinkedIn filters to apply alongside the queries

---

## Related Skills

- [person-search](./`person-search.instructions.md) — applies these queries in a people search context
- [job-search](./`job-search.instructions.md) — applies these queries in a jobs search context

---

## References

- [search-patterns](../../../references/search-patterns.md) — proven query patterns for common LinkedIn search types
- [linkedin-usage-patterns](../../../references/linkedin-usage-patterns.md) — how LinkedIn's search ranking works

---

## Notes and Caveats

- LinkedIn's Boolean support is inconsistent. Always test queries before trusting them.
- Quoted phrases (`"technical recruiter"`) are more reliable than unquoted multi-word terms.
- LinkedIn caps search results at 1,000 for free accounts. If your query returns more, tighten it.
- Keywords are matched against the full profile or job description, not just the headline. This means results can include people whose title does not match but whose profile mentions the keyword.

---

## Maintenance Notes

Review when LinkedIn changes its search interface or Boolean support. The operator syntax above is based on current LinkedIn behavior.

Last reviewed: 2026-03-27
