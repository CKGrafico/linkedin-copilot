> **Status: ACTIVE** — This file is current and maintained.

# Workflow: Maintain Prospect Pipeline

## Purpose

A structured review process for keeping your active prospect and opportunity lists current — identifying what is stale, what is hot, what needs follow-up, and what should be closed. This workflow prevents the common failure mode where session notes pile up but nothing gets acted on.

---

## Trigger

- **User request:** "Help me review my current pipeline"
- **User request:** "I want to catch up on my job search / sourcing — what do I still need to do?"
- **Condition:** One or more prior session notes exist and the user wants to review current status across their active leads

---

## Participants

- **Agent:** [sourcer](../.agents/agents/sourcer/AGENT.md) *(for people pipelines)*
- **Agent:** [headhunter](../.agents/agents/headhunter/AGENT.md) *(for opportunity pipelines)*
- *(The agent depends on what type of pipeline is being reviewed. Both can be invoked in sequence.)*

---

## Skills Invoked

- [note-taking](../.agents/skills/note-taking/SKILL.md) — Step 1 (reading prior notes)
- [follow-up-planning](../.agents/skills/follow-up-planning/SKILL.md) — Steps 2–4
- [lead-ranking](../.agents/skills/lead-ranking/SKILL.md) — Step 3 (re-prioritization)

---

## Steps

### Step 1: Collect existing session notes

**Action:** Gather all session notes from previous relevant sessions. Attach them as context for the reviewing agent.

Look for:
- Outstanding next actions that have not been completed
- Follow-up commitments with dates that have passed
- Items marked "Monitor" with a check-in date that has arrived
- Items with unclear status

**Output:** A consolidated view of all active items.

### Step 2: Triage by urgency

**Agent:** sourcer or headhunter
**Skill used:** [follow-up-planning](../.agents/skills/follow-up-planning/SKILL.md)
**Action:** Sort all active items into four buckets:

**Overdue:** Next action date has passed with no update.
- What happened? If action was taken, update the status. If it was missed, reschedule.

**Due this week:** Next action falls within the next 7 days.
- Confirm these are still worth acting on. Verify the posting / profile is still active.

**Monitor:** Items flagged for a future check-in.
- Has the trigger condition been met? If yes, move to active. If not, extend the check-in date.

**Stale (30+ days with no movement):** Items that have been sitting with no action.
- Evaluate: is there still a reason to keep this item? If not, close it.

**Output:** Triaged item list.

### Step 3: Re-rank active items

**Agent:** sourcer or headhunter
**Skill used:** [lead-ranking](../.agents/skills/lead-ranking/SKILL.md)
**Action:** Apply the ranking framework to the current active list. Priorities may have shifted since the last session:
- Has a job posting aged out? Downgrade or close.
- Has a person become more accessible? (Mutual connection appeared, posted something relevant) Upgrade.
- Has a company announced news that changes the fit assessment? Update.

**Output:** Updated priority order.

### Step 4: Close stale items

**Agent:** sourcer or headhunter
**Action:** For each item that has been in the pipeline for 30+ days with no engagement, make a close decision:
- **Close — no response:** Outreach was sent, no response after follow-up.
- **Close — no longer relevant:** Role was filled, person changed jobs, opportunity expired.
- **Close — deprioritized:** Other items are higher priority; this can wait indefinitely.
- **Keep — reason:** State the specific reason this item should remain active.

**Output:** Closed items list + reasons.

### Step 5: Update session notes

**Skill used:** [note-taking](../.agents/skills/note-taking/SKILL.md)
**Action:** Produce an updated session note that reflects the current state of the pipeline:
- Remove or archive closed items
- Update status on active items
- Record new follow-up commitments with dates
- Note any pipeline gaps that suggest a new search session is needed

**Output:** Updated session note.

---

## Expected Output

- A current, triaged pipeline with clear status on every active item
- A follow-up plan for the next 7–14 days
- A list of closed items with closure reasons
- An updated session note reflecting current state

---

## Handoff

- Pipeline is too thin: run [workflows/find-relevant-recruiters.md](find-relevant-recruiters.md) or [workflows/find-jobs-worth-applying.md](find-jobs-worth-applying.md) to add new leads
- An active lead is ready for outreach: run [workflows/prepare-outreach.md](prepare-outreach.md)

---

## Failure Modes

- **No existing session notes:** This workflow requires prior session notes. If none exist, start with a search workflow first.
- **Pipeline is entirely stale:** Everything is >30 days old with no movement. Close it all and start fresh searches. A stale pipeline is a signal to restart, not to nurse old leads.
- **Too many overdue items:** Triage ruthlessly. It is better to close 10 stale items and focus on 3 strong ones than to maintain a long list of low-probability leads.

---

## Maintenance Notes

Review if the pipeline management approach needs to evolve as the user's job search or networking strategy changes.

Last reviewed: 2026-03-27
