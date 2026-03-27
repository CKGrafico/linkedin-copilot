> **Status: ACTIVE** — This file is current and maintained.

# Skill: follow-up-planning

## What This Skill Does

Plans concrete next steps after a search or outreach session — what to follow up on, when, what the success condition looks like, and what to do if there is no response.

---

## Used By

- [sourcer](../../agents/sourcer/AGENT.md)
- [headhunter](../../agents/headhunter/AGENT.md)

---

## When to Apply

At the end of any session that produced actionable output — a candidate list, an opportunity list, or an outreach draft. Follow-up planning converts a list of results into a set of time-bound commitments.

---

## Instructions

### 1. Review the session output

Start from the ranked output of [lead-ranking](./`lead-ranking.instructions.md) or the decisions from [opportunity-qualification](./`opportunity-qualification.instructions.md). Separate items into three buckets:

- **Act this week:** Priority 1 items. Concrete actions with a specific date.
- **Act this month:** Priority 2 items. Scheduled but not urgent.
- **Monitor:** Lower-priority items that should be checked again after a defined interval.

### 2. For each "Act this week" item, define the specific action

Vague follow-ups fail. For each item, specify:
- **What:** The exact action (send a connection request, send a message, submit an application)
- **When:** A specific date or day of the week, not "soon"
- **Success condition:** What does a good outcome look like? (received a reply, interview scheduled, application submitted)
- **If no response:** What is the plan if nothing happens after X days?

Example:
```
Action: Send connection request to [Name] with a note referencing their post on [topic]
When: [specific date]
Success condition: Connection accepted and replies to follow-up message
If no response: After 7 days, send one brief direct message. If still no response, mark as passive monitor.
```

### 3. For each "Monitor" item, set a check-in date

Do not leave monitored items in an undefined state. Every monitored item needs:
- A specific date to revisit it
- A trigger condition that would move it to "Act" (e.g., "if they post something relevant" or "if the job is still open in 2 weeks")

### 4. Handle the "no response" protocol

For outreach:
- First attempt: [date]
- One follow-up if no response: 7–10 days after first attempt
- Final status: if no response after follow-up, mark as **closed** and move on. Do not send a third message.

For job applications:
- After applying, set a 2-week check-in to see if there has been any ATS activity or recruiter contact
- If nothing after 3 weeks, treat as no-response and continue the pipeline

### 5. Record all plans in session notes

All follow-up commitments should be written into the **Next actions** section of the session note (see [note-taking](./`note-taking.instructions.md)). They should be specific enough that they can be executed without recalling the session.

---

## Input Requirements

- The ranked or qualified output from the current session
- Any existing follow-up items from previous sessions

---

## Output Format

A structured follow-up plan embedded in the session note:

```
## Follow-up plan

### This week
- [ ] [Action] — [Date] — Success: [condition] — If no response: [plan]

### This month
- [ ] [Action] — [Date] — Success: [condition]

### Monitor
- [ ] [Name or opportunity] — Check-in: [date] — Trigger: [condition to escalate]

### Closed (no action required)
- [Name or opportunity] — Reason: [no response / not a fit / filled]
```

---

## Related Skills

- [lead-ranking](./`lead-ranking.instructions.md) — produces the prioritized list this skill plans around
- [note-taking](./`note-taking.instructions.md) — the follow-up plan is embedded in the session note

---

## References

- [outreach-best-practices](../../../.references/outreach-best-practices.md) — follow-up cadence norms

---

## Notes and Caveats

- One follow-up is acceptable. Two or more is not. The repo's ethical boundaries apply here.
- "Monitor" items should have a defined sunset. If you have not acted on a monitored item after 30 days, drop it.
- Follow-up plans only work if they live in a place you will actually see them (your notes, task manager, or calendar). The session note is the starting point — transfer to wherever you manage your own tasks.

---

## Maintenance Notes

Review if follow-up norms change significantly (e.g., LinkedIn changes message visibility or follow-up etiquette evolves).

Last reviewed: 2026-03-27
