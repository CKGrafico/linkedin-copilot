> **Status: ACTIVE** — This file is current and maintained.

# Workflow: Compare Opportunities

## Purpose

A structured process for comparing multiple job opportunities side by side and producing a clear prioritization with rationale. Used when a user has 2–6 opportunities in hand and wants help deciding which to pursue first, which to deprioritize, and why.

---

## Trigger

- **User request:** "I have several job leads — help me figure out which ones to prioritize"
- **User request:** "Compare these opportunities for me"
- **Condition:** Multiple qualified opportunities exist and a decision about priority is needed

---

## Participants

- **Agent:** [headhunter](../.agents/agents/headhunter/AGENT.md)

---

## Skills Invoked

- [opportunity-qualification](../.agents/skills/opportunity-qualification/SKILL.md) — Step 2 (if not already applied)
- [company-research](../.agents/skills/company-research/SKILL.md) — Step 3 (if not already completed)
- [lead-ranking](../.agents/skills/lead-ranking/SKILL.md) — Step 4
- [note-taking](../.agents/skills/note-taking/SKILL.md) — Step 5

---

## Steps

### Step 1: Collect opportunity data

**Agent:** headhunter
**Action:** Gather the available information for each opportunity:
- Job title and company
- Job description (or summary if not available)
- Date posted / application status
- Any company research already completed
- Any prior qualification decisions from previous sessions (check session notes)

Ask the user to fill in any gaps. Do not proceed with incomplete information for Priority 1 candidates.
**Output:** Data package for each opportunity.

### Step 2: Qualify any unqualified opportunities

**Agent:** headhunter
**Skill used:** [opportunity-qualification](../.agents/skills/opportunity-qualification/SKILL.md)
**Action:** For any opportunity that has not yet been through the qualification process, apply the full rubric: hard filters first, then soft signal assessment.
**Output:** Qualification decision and assessment for each opportunity.

### Step 3: Research any unresearched companies

**Agent:** headhunter
**Skill used:** [company-research](../.agents/skills/company-research/SKILL.md)
**Action:** For any opportunity without a company snapshot, produce one: headcount signals, job posting activity, leadership stability, cultural signals, strategic fit.
**Output:** Company snapshot for each opportunity.

### Step 4: Rank opportunities

**Agent:** headhunter
**Skill used:** [lead-ranking](../.agents/skills/lead-ranking/SKILL.md)
**Action:** Apply the opportunity ranking framework across all five dimensions (Role fit, Company fit, Opportunity quality, Accessibility, Timing) for each opportunity. Produce a ranked order with tier assignments.
**Output:** Ranked opportunity list.

### Step 5: Produce the comparison summary

**Agent:** headhunter
**Action:** Produce a structured comparison using this format for each opportunity:

```
## [Job Title] at [Company]
Priority: [1 / 2 / Monitor / Skip]
Role fit: [High / Medium / Low]
Company fit: [High / Medium / Low]
Opportunity quality: [High / Medium / Low]
Accessibility: [High / Medium / Low] — [internal contact? Y/N]
Timing: [High / Medium / Low]

Strengths: [2–3 bullet points]
Concerns: [1–2 bullet points, or "none"]
Recommended action: [apply now / apply soon / monitor / skip]
```

After all individual entries, add a **Summary Recommendation:**
- Rank all opportunities from most to least recommended
- Explain the top-1 recommendation in 2–3 sentences
- Note if two opportunities are close enough that the user's personal preferences should break the tie

### Step 6: Record session notes

**Skill used:** [note-taking](../.agents/skills/note-taking/SKILL.md)
**Action:** Record the comparison session: all opportunities evaluated, qualification decisions, company snapshots, final ranking, and recommended actions.
**Output:** Session note.

---

## Expected Output

- A side-by-side comparison of all opportunities with consistent evaluation criteria
- A ranked priority order
- A clear top recommendation with rationale
- Session notes for future reference

---

## Handoff

- Top-priority opportunity with no internal contact: run [workflows/find-relevant-recruiters.md](find-relevant-recruiters.md) with this company as the target
- Opportunity requiring deeper company research: use `researcher` (future) or `company-scout` (future)
- Ready to apply: user takes the session note as context for application

---

## Failure Modes

- **Insufficient information on one or more opportunities:** Flag missing data explicitly. Do not fabricate or assume details. Ask the user to supply what is missing.
- **All opportunities are roughly equal:** Break ties by Accessibility (warm application path wins) and Timing (fresher posting wins). State clearly that it is a close call.
- **User has more than 6 opportunities:** Consider splitting into two comparison sessions: a first session to eliminate clear misfits, then a second session for the shortlist.

---

## Maintenance Notes

Review if the ranking dimensions become misaligned with the user's actual decision-making criteria. Update via contributor-request.

Last reviewed: 2026-03-27
