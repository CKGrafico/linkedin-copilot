> **Status: ACTIVE** — This file is current and maintained.

# Skill: company-research

## What This Skill Does

Researches a company using LinkedIn signals to produce a compact assessment: size, growth trajectory, hiring activity, leadership stability, cultural signals, and strategic fit as a target employer or contact.

---

## Used By

- [headhunter](../agents/headhunter.md)

---

## When to Apply

When a specific company needs evaluation — either as a job application target, or when understanding the context behind a contact at that company. Applied after initial qualification signals a company worth deeper investigation.

---

## Browser MCP Automation

Requires Browser MCP active. See [browser-navigation](browser-navigation.md) for setup and general patterns.

### 1. Navigate to the company page

```
navigate: https://www.linkedin.com/company/[company-slug]/
wait: 3
snapshot
```

To find the correct company slug, navigate to LinkedIn and search for the company name, then use the URL of the company's LinkedIn page.

### 2. Read the overview snapshot

```
snapshot
```

Extract from the overview tab:
- Company name and industry
- Employee count
- Headquarters location
- Founded year
- Website URL
- Headcount trend (if visible)

### 3. Check company posts

```
click: [Posts tab]
wait: 2
snapshot
```

Read recent posts for activity signals, culture indicators, and growth announcements.

### 4. Check open jobs

```
click: [Jobs tab]
wait: 2
snapshot
```

Read the number of open roles, recency of postings, and which departments are hiring.

### 5. Return

```
go_back
wait: 2
snapshot
```

---

## Instructions (without Browser MCP)

### 1. Find the company's LinkedIn page

Search for the company directly. Verify you have the right entity (some companies have subsidiaries or similarly-named competitors). Note:
- Full legal name and common name
- Industry / sector
- Headquarters location
- Founded year (if listed)

### 2. Read the headcount signals

LinkedIn shows employee count and headcount growth over time (if available):
- **Growing headcount** (10–30%+ over last year): active expansion, positive signal for hiring
- **Flat headcount**: stable, no growth, may still hire for backfills
- **Declining headcount**: potential layoffs, cautious signal — verify before investing time
- **Very small headcount** (under 10 visible employees): company may be newer, niche, or privacy-conscious

### 3. Review recent company posts

Scroll the company's "Posts" tab:
- Has the company posted in the last 30 days? (activity signal)
- Are they announcing new hires, product launches, funding, partnerships? (growth signal)
- What tone and culture does the content project?
- Are posts getting engagement from employees? (culture and morale proxy)

No posts in 3+ months is a yellow flag. No posts ever on the company page is a red flag.

### 4. Check current job postings

On the company's LinkedIn page, check "Jobs":
- How many open roles are listed?
- Are roles recent (posted in last 30 days)?
- Is hiring concentrated in one department (e.g., all sales, all engineering)?
- Does the target role appear? (Direct match is ideal; adjacent roles suggest the team is growing)

Multiple recent postings across departments = sustained growth. One isolated posting = backfill or experiment.

### 5. Review notable employees and leadership

Search for the company's key leaders:
- Is the leadership team stable? (Recent CxO departures can indicate turbulence)
- Are there visible employees in the target department you could connect with?
- Any alumni from companies you respect? (Culture/quality signal)

### 6. Synthesize the assessment

Produce a company snapshot using the output format below. Use this to inform the opportunity qualification decision.

---

## Input Requirements

- Company name
- The context for research: job application target, potential employer, contact at company

---

## Output Format

```
Company: [Name]
Industry: [sector]
Size: [headcount range from LinkedIn] — [growing / flat / declining]
HQ: [location] | Remote posture: [remote-friendly / hybrid / on-site]
Activity: [active / moderate / dormant] — last post: [approximate date]
Hiring signals: [brief summary of current hiring activity]
Culture signals: [brief summary from posts and content]
Red flags: [any concerns]
Strategic fit: [strong / moderate / weak] — [1-sentence rationale]
```

---

## Related Skills

- [browser-navigation](browser-navigation.md) — foundational browser operation patterns
- [opportunity-qualification](opportunity-qualification.md) — uses this assessment as input for the "Research further" path
- [lead-ranking](lead-ranking.md) — company quality contributes to opportunity ranking

---

## References

- [browser-mcp](../references/browser-mcp.md) — available browser tools and LinkedIn URL patterns
- [company-evaluation-criteria](../references/company-evaluation-criteria.md) — detailed criteria for assessing companies
- [recruiter-signals](../references/recruiter-signals.md) — reading hiring activity patterns

---

## Notes and Caveats

- LinkedIn headcount data is based on employee-reported profiles, not official filings. It is directionally useful but not precise.
- A company with poor LinkedIn presence is not necessarily a bad employer — some industries are simply not LinkedIn-native.
- Private companies do not disclose financials. Use LinkedIn signals as proxies, not as certainties.

---

## Maintenance Notes

Review when LinkedIn changes what company data is publicly visible or how headcount trends are displayed.

Last reviewed: 2026-03-27
