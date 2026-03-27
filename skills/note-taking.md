> **Status: ACTIVE** — This file is current and maintained.

# Skill: note-taking

## What This Skill Does

Provides a structured format for recording the output of any agent session — what was searched, what was found, decisions made, and next actions planned — so that the output can be reused in future sessions or handed off to another agent.

---

## Used By

- [sourcer](../agents/sourcer.md)
- [headhunter](../agents/headhunter.md)
- *(all future agents)*

---

## When to Apply

At the end of every agent session, before closing the conversation. Well-structured session notes are the memory layer of this system. Without them, each session starts from scratch and insights are lost.

---

## Instructions

### 1. Record the session header

Capture the context of this session so it can be interpreted later without memory of what happened.

```
## Session note
Date: [today's date]
Agent: [sourcer / headhunter / etc.]
Goal: [one sentence: what were you trying to accomplish?]
Status: [completed / partial / abandoned]
```

### 2. Record the queries used

Document the exact search queries and filters applied. Future sessions should be able to reproduce or extend this search without rebuilding it from scratch.

```
## Queries used
- Query: [paste the Boolean query]
  Filters: [list of filters applied]
  Result quality: [high / medium / low] — [brief note on why]
```

Record all queries tried, including ones that were discarded and why.

### 3. Record results

For people searches (use [profile-summary](profile-summary.md) format for each entry):

```
## Candidates found
### [Name]
- Role: [title] at [company]
- Degree: [1st / 2nd (mutual: X) / 3rd+]
- Key signals: [bullet points]
- Fit: [strong / moderate / weak]
- Decision: [outreach / research / skip / monitor]
- Notes: [anything worth remembering]
```

For job searches (use [opportunity-qualification](opportunity-qualification.md) output format):

```
## Opportunities found
### [Job Title] at [Company]
- Posted: [date]
- Decision: [apply now / apply soon / monitor / skip]
- Rationale: [1 sentence]
- Flags: [any concerns]
```

### 4. Record open questions and blockers

Capture anything unresolved that should be picked up next time.

```
## Open questions
- [Question or blocker 1]
- [Question or blocker 2]
```

### 5. Record next actions

Be specific. Vague next actions ("follow up later") are not useful. Every action should have a clear target and ideally a date.

```
## Next actions
- [ ] [Specific action] — target date: [date or relative: "this week"]
- [ ] [Specific action] — target date: [date]
```

### 6. Record potential repo improvements

If the session revealed something that should be captured in the repo (new heuristic, updated pattern, missing skill), record it here for routing to `contributor`.

```
## Repo improvement notes
- [Description of the improvement needed] — suggested file: [references/X.md or skills/Y.md]
```

---

## Input Requirements

- The session's goal and outputs (whatever was produced during the session)

---

## Output Format

A structured Markdown note following the template above. Store it outside the repo, in your own notes or files. It is user-owned session state, not repo content.

---

## Related Skills

- [follow-up-planning](follow-up-planning.md) — uses the next actions section as its starting point
- [profile-summary](profile-summary.md) — provides the per-candidate entry format used in the results section
- [opportunity-qualification](opportunity-qualification.md) — provides the per-opportunity format used in results

---

## Notes and Caveats

- Notes are for your future self and for AI agents in subsequent sessions. Write them as if you will not remember this session at all.
- Include exact query strings. "I searched for fintech recruiters" is useless. The actual Boolean query is invaluable.
- Session notes live outside the repo. Never commit personal session notes to this repo.

---

## Maintenance Notes

Review if the fields become insufficient for capturing session context as new agents are added.

Last reviewed: 2026-03-27
