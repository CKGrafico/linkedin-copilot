> **Status: ACTIVE** — This file is current and maintained.

# Skill: profile-summary

## What This Skill Does

Extracts the most relevant information from a LinkedIn profile into a compact, structured summary: current role, career trajectory, key signals, fit indicators, and outreach hooks.

---

## Used By

- [sourcer](../agents/sourcer.md)
- [headhunter](../agents/headhunter.md)

---

## When to Apply

When you need to evaluate a person's profile quickly and accurately — whether assessing a sourced candidate, researching a company contact, or preparing to reach out. Apply before making any decision about whether to pursue, contact, or skip someone.

---

## Browser MCP Automation

Requires Browser MCP active. See [browser-navigation](browser-navigation.md) for setup and general patterns.

### 1. Navigate to the profile

```
navigate: https://www.linkedin.com/in/[profile-slug]
wait: 3
snapshot
```

If you only have a name (not a URL), run a people search first using [person-search](person-search.md), then navigate to the profile URL from those results.

### 2. Read the full profile via snapshot

```
snapshot
```

The snapshot returns the page's accessibility tree. Extract from it:
- Headline and current role
- Experience section (all entries)
- Activity feed (recent posts/comments if visible)
- Education section
- Mutual connections count
- Any "Open to work" or "Hiring" signals

If the page is long and the snapshot is truncated, scroll:

```
press_key: End
wait: 2
snapshot
```

### 3. Return to the previous page

After reading:

```
go_back
wait: 2
snapshot
```

---

## Instructions (without Browser MCP)

### 1. Read the headline and current role first

The headline is the person's self-selected professional identity. Read it carefully:
- Does the title match your target type?
- Is there a value proposition or specialization stated? (e.g., "Recruiting for deep tech | Series A–C")
- Does the headline use keywords that signal fit or misfit?

Note the current company and approximate tenure (from the experience section).

### 2. Scan the career trajectory

Review the experience section from most recent to oldest:
- What is the direction of movement? (upward, lateral, pivoting, returning?)
- Are there any recent role changes? (changed jobs in last 6 months is a significant signal)
- Do the companies indicate a domain focus? (e.g., all fintech, all enterprise software)
- Is there a pattern of seniority growth, or has the person plateaued?

Note: career trajectory is more predictive than current title alone.

### 3. Check activity signals

Scroll to see recent activity (posts, comments, shares):
- Has the person posted or commented in the last 30 days? (positive signal for responsiveness)
- What topics do they engage with? (reveals genuine interests and domain focus)
- Do they post original content? (higher engagement persona, likely to respond to thoughtful messages)
- No activity in 6+ months? (account may be dormant — lower response probability)

### 4. Note education and background markers

- Shared alma mater? (warm outreach hook)
- Notable certifications or credentials?
- Any overlap with your own background?

### 5. Check mutual connections

- How many mutual connections do you share?
- Are any of them people you know well enough to request an introduction?
- A warm introduction through a strong mutual is 3–5× more effective than cold outreach.

### 6. Evaluate fit against your criteria

Using the inputs you were given (target criteria), assess:
- **Role fit:** Does their current role match what you are looking for?
- **Domain fit:** Is their industry and company type aligned with your target?
- **Signal fit:** Are the activity and engagement signals positive?
- **Accessibility fit:** 1st/2nd degree? Mutual connections available?

### 7. Compose the summary

Produce a compact, structured summary (see output format below). This summary feeds into [lead-ranking](lead-ranking.md) and, if applicable, [message-personalization](message-personalization.md).

---

## Input Requirements

- The LinkedIn profile to summarize (name, headline, experience, activity)
- Target criteria to assess fit against

---

## Output Format

```
Name: [Full Name]
Current role: [Title] at [Company] (approx. [tenure])
Trajectory: [brief 1-line description: e.g., "5 years in recruiting, last 2 in fintech, recently promoted to Senior TA Manager"]
Activity: [active / moderate / dormant] — last seen: [approximate date or signal]
Degree: [1st / 2nd (mutual: [name]) / 3rd+]
Shared context: [school / former employer / group / none]
Fit: [strong / moderate / weak] — [one sentence rationale]
Hooks: [1–2 personalization hooks for outreach]
Next action: [outreach / research further / skip / monitor]
```

---

## Related Skills

- [browser-navigation](browser-navigation.md) — foundational browser operation patterns
- [lead-ranking](lead-ranking.md) — uses this summary as input for prioritization
- [message-personalization](message-personalization.md) — uses the hooks identified here

---

## References

- [browser-mcp](../references/browser-mcp.md) — available browser tools and LinkedIn URL patterns
- [profile-evaluation-criteria](../references/profile-evaluation-criteria.md) — detailed criteria for assessing profiles
- [sourcing-heuristics](../references/sourcing-heuristics.md) — signals that indicate a high-value contact

---

## Notes and Caveats

- Profiles with little content are not automatically low-value. Some highly effective professionals maintain minimal profiles.
- Do not conflate low activity with low interest. Some people are active off-platform.
- Profile information may be outdated. If the current role's start date is very recent, some details may not yet be reflected.
- Respect privacy. Note only what is publicly displayed. Do not infer sensitive information.

---

## Maintenance Notes

Review when LinkedIn changes its profile layout or what information is publicly visible.

Last reviewed: 2026-03-27
