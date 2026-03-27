> **Status: ACTIVE** — This file is current and maintained.

# Skill: lead-ranking

## What This Skill Does

Prioritizes a list of people or opportunities using weighted signals — turning a flat list of candidates or jobs into an ordered list with clear rationale for each position.

---

## Used By

- [sourcer](../agents/sourcer.md)
- [headhunter](../agents/headhunter.md)

---

## When to Apply

After a search or qualification step has produced a list of people or opportunities. Ranking should happen before presenting results to the user. A flat unordered list forces the user to make all prioritization decisions themselves — that is not useful.

---

## Instructions

### Ranking people (candidates, contacts)

Evaluate each person across five dimensions. Use a **High / Medium / Low** rating for each:

**1. Fit** — How well does this person match the target criteria?
- High: matches all key criteria (role type, seniority, domain, geography)
- Medium: matches most criteria with one significant gap
- Low: mismatches on a core criterion

**2. Signal strength** — How strong are the activity and interest signals?
- High: recent activity, relevant posts, clear domain engagement
- Medium: some activity, profile is informative but quiet
- Low: dormant account or sparse profile

**3. Accessibility** — How easy is it to reach this person?
- High: 1st-degree connection or strong mutual who could introduce
- Medium: 2nd-degree, mutual exists but connection is weak
- Low: 3rd-degree, no warm path

**4. Timeliness** — Is now a good time to reach out?
- High: recently changed role, posted about a relevant topic, visible in your orbit
- Medium: no obvious signal but nothing negative either
- Low: just started a new role (less than 3 months ago), unlikely to be open to opportunities

**5. Strategic value** — Beyond the immediate goal, does this person have long-term value?
- High: hiring manager at a target company, connector with broad network, influential in target domain
- Medium: useful for the immediate goal, limited beyond it
- Low: relevant only for one narrow specific purpose

**Ranking formula (qualitative):**

1. Leads with **High** on Fit + at least Medium on Accessibility = top tier
2. Leads with **High** on Fit + Low on Accessibility = second tier (worth pursuing with more effort)
3. Leads with **Medium** on Fit + High on Accessibility = third tier (quick wins)
4. Everything else = deprioritize or skip

---

### Ranking opportunities (jobs)

Evaluate each opportunity across five dimensions:

**1. Role fit** — How well does the role match the user's target?
- High: title, responsibilities, and seniority are a strong match
- Medium: good match with one stretch area
- Low: requires significant skill gap or mismatched seniority

**2. Company fit** — How aligned is the company with the user's preferences?
- High: target industry, size, stage, and culture match well
- Medium: mostly aligned with one mismatch
- Low: significant mismatch on a preference dimension

**3. Opportunity quality** — How real and strong is this opportunity?
- High: recent posting, clear description, active company, salary listed
- Medium: real but either old, vague, or limited info
- Low: ghost posting signals, poor description, dormant company

**4. Accessibility** — How reachable is this opportunity?
- High: internal contact or mutual connection at the company
- Medium: no contact but company is responsive and well-known
- Low: no contact, small or unknown company, opaque process

**5. Timing** — Is this opportunity well-timed for the user's situation?
- High: aligns with user's target start date, company is in active hiring mode
- Medium: reasonable timing with minor mismatches
- Low: company is early-stage or uncertain, timing is unclear

**Priority order:** Apply the same qualitative ranking as for people leads.

---

## Input Requirements

- A list of candidates or opportunities with profile summaries or qualification assessments already applied
- The user's stated criteria and priorities

---

## Output Format

A ranked list with explicit priority tiers:

```
## Priority 1 (Act now)
1. [Name / Job Title] — [Fit: H, Signal: H, Access: M] — [1-sentence rationale]
2. ...

## Priority 2 (Act this week)
3. [Name / Job Title] — [Fit: H, Signal: M, Access: L] — [1-sentence rationale]
4. ...

## Priority 3 (Monitor / Low effort)
5. ...

## Skip
- [Name / Job Title] — [reason for skipping]
```

---

## Related Skills

- [profile-summary](profile-summary.md) — produces the input data for people ranking
- [opportunity-qualification](opportunity-qualification.md) — produces the input data for opportunity ranking
- [follow-up-planning](follow-up-planning.md) — plans actions based on ranked output

---

## References

- [sourcing-heuristics](../references/sourcing-heuristics.md) — signal definitions for people ranking
- [job-search-heuristics](../references/job-search-heuristics.md) — quality signals for opportunity ranking

---

## Notes and Caveats

- Ranking is advisory, not prescriptive. The user makes the final call on what to act on.
- Do not rank more than 15–20 items in a single session. Above that, revisit the search query.
- Ties at the same priority level should be broken by Accessibility — easier wins first.

---

## Maintenance Notes

Review if the weighting model consistently produces poor recommendations based on user feedback.

Last reviewed: 2026-03-27
