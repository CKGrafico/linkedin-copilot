> **Status: ACTIVE** — This file is current and maintained.

# Workflow: Prepare Outreach

## Purpose

An end-to-end guide for preparing a personalized LinkedIn outreach message for a specific person — from profile reading through drafting to follow-up planning. This workflow exists separately from agent docs because it is the most common cross-skill flow and will eventually span multiple agents (sourcer + outreach-writer).

---

## Trigger

- **User request:** "Help me write a message to [person]"
- **User request:** "I want to reach out to this recruiter / hiring manager / connection"
- **Condition:** A specific person has been identified and a decision to contact them has been made

---

## Participants

- **Agent:** `outreach-writer` (future) — primary
- **Agent:** [sourcer](../.github/instructions/agents/sourcer.instructions.md) — if profile research is needed first

*Until `outreach-writer` is implemented, sourcer can handle this workflow using its skills.*

---

## Skills Invoked

- [profile-summary](../.github/instructions/skills/profile-summary.instructions.md) — Step 1
- [message-personalization](../.github/instructions/skills/message-personalization.instructions.md) — Step 2
- [outreach-drafting](../.github/instructions/skills/outreach-drafting.instructions.md) — Step 3
- [follow-up-planning](../.github/instructions/skills/follow-up-planning.instructions.md) — Step 5
- [note-taking](../.github/instructions/skills/note-taking.instructions.md) — Step 6

---

## Steps

### Step 1: Summarize the recipient's profile

**Agent:** outreach-writer (or sourcer)
**Skill used:** [profile-summary](../.github/instructions/skills/profile-summary.instructions.md)
**Action:** Read the recipient's LinkedIn profile and produce a structured summary: current role, trajectory, activity signals, connection degree, mutual connections.
**Output:** Profile summary including raw hook candidates.

### Step 2: Identify personalization hooks

**Agent:** outreach-writer (or sourcer)
**Skill used:** [message-personalization](../.github/instructions/skills/message-personalization.instructions.md)
**Action:** Work through the hook categories (shared context, recent content, career trajectory, company news) and identify the strongest genuine hook. Verify it is authentic and specific to this person.
**Output:** Primary hook + hook sentence draft.

### Step 3: Draft the message

**Agent:** outreach-writer (or sourcer)
**Skill used:** [outreach-drafting](../.github/instructions/skills/outreach-drafting.instructions.md)
**Action:** Choose the message type (connection request note / direct message / InMail). Structure the message: opening (using the hook), bridge, purpose, close. Calibrate length. Write a clear, low-friction call to action.
**Output:** Complete draft message.

### Step 4: Review the draft

**Agent:** outreach-writer (or sourcer)
**Action:** Before finalizing, verify:
- [ ] The opening references something specific and real about the recipient
- [ ] The purpose is stated clearly (what are you asking for?)
- [ ] The call to action is concrete and easy to respond to
- [ ] The message is under the recommended word count for this message type
- [ ] No generic phrases ("I came across your profile," "I'd love to connect")
- [ ] The message is honest and accurately represents your purpose

If any check fails, revise the draft.
**Output:** Reviewed and finalized draft message.

### Step 5: Plan the follow-up

**Agent:** outreach-writer (or sourcer)
**Skill used:** [follow-up-planning](../.github/instructions/skills/follow-up-planning.instructions.md)
**Action:** Define the follow-up plan:
- If no response after 7–10 days: draft a brief follow-up (2–3 sentences, reference first message, offer graceful exit)
- After follow-up: if still no response, mark as closed
- Success condition: reply received, connection accepted with subsequent conversation
**Output:** Follow-up plan.

### Step 6: Record in session notes

**Skill used:** [note-taking](../.github/instructions/skills/note-taking.instructions.md)
**Action:** Record the outreach in session notes: recipient name, role, company, date sent, message type, hook used, follow-up plan.
**Output:** Session note entry.

---

## Expected Output

- A finalized, personalized outreach message ready to send
- A defined follow-up plan
- A session note entry for tracking

---

## Handoff

- Message is ready to send: user takes the draft and sends it directly on LinkedIn
- If the person responds positively: record the outcome in session notes and update the follow-up plan
- If no response after follow-up: mark as closed in session notes

---

## Failure Modes

- **No strong personalization hook found:** Write a direct, honest message without a forced hook. Clarity and honesty outperform weak personalization.
- **Profile is private or sparse:** Limited hook options. Fall back to connection degree context (shared mutual) or company context.
- **User is uncertain about the purpose of the outreach:** Clarify the goal before drafting. A message without a clear purpose is a message that will be ignored.

---

## Maintenance Notes

Review when LinkedIn changes connection request note length limits or messaging mechanics.

Last reviewed: 2026-03-27
