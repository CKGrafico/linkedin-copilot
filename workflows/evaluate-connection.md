> **Status: ACTIVE** — This file is current and maintained.

# Workflow: Evaluate a Connection

## Purpose

A structured decision process for determining whether to accept or send a LinkedIn connection request. Prevents automatic acceptance of low-value connections and helps the user be intentional about who is in their 1st-degree network — which directly affects search ranking and outreach quality.

---

## Trigger

- **User request:** "Should I connect with this person?"
- **Condition:** Pending connection request received, or user is considering sending a request

---

## Participants

- **Agent:** [sourcer](../agents/sourcer.md) *(for incoming or outgoing connection evaluation)*

---

## Skills Invoked

- [profile-summary](../skills/profile-summary.md) — Step 1
- [note-taking](../skills/note-taking.md) — Step 4

---

## Steps

### Step 1: Summarize the profile

**Agent:** sourcer
**Skill used:** [profile-summary](../skills/profile-summary.md)
**Action:** Read the person's profile and produce a summary: current role, trajectory, activity signals, mutual connections, and any personalization hooks.
**Output:** Profile summary.

### Step 2: Assess connection value

**Agent:** sourcer
**Action:** Evaluate the connection across three dimensions:

**Relevance:**
- Is this person in your professional domain or a domain you care about?
- Could they be useful in your current goals (job search, networking, sourcing)?
- Is there a plausible reason this person connected with you (shared group, domain overlap, commented on a post)?

**Trust:**
- Does the profile look legitimate? (Real photo, real work history, no red flags from [profile-evaluation-criteria](../references/profile-evaluation-criteria.md))
- Do you have shared context? (mutual connections, shared company, same school)
- Does the request include a personalized note that references real context?

**Risk:**
- Does the profile look like a recruiter who will immediately try to sell you something? (Some people are fine with this; others are not)
- Any signals of spam or fake profile?

**Output:** A brief assessment on each dimension.

### Step 3: Make a recommendation

**Agent:** sourcer
**Action:** Based on the assessment, recommend one of:

- **Connect:** Positive across all three dimensions. Real person, relevant to your goals or network, no red flags.
- **Connect with caution:** Legitimate but likely to lead to immediate solicitation. Connect if you are comfortable with that, skip if your inbox is already noisy.
- **Decline:** Sparse or suspicious profile, no shared context, clear spam signals, or irrelevant to any plausible professional purpose.
- **Defer:** Something is unclear. Revisit in a few days, or check LinkedIn for more context first.

### Step 4: Record if notable

**Agent:** sourcer
**Skill used:** [note-taking](../skills/note-taking.md)
**Action:** If the person is notable — a target company recruiter, a relevant hiring manager, a strong potential connector — record them in session notes even if no action is taken today.
**Output:** Session note entry (optional, only if notable).

---

## Expected Output

- A connection decision recommendation (Connect / Connect with caution / Decline / Defer)
- A 1–2 sentence rationale
- A session note entry if the person is notable

---

## Handoff

- If you decide to connect and want to follow up: plan outreach using [workflows/prepare-outreach.md](prepare-outreach.md)
- If you want to track this person for future reference: add to your session notes pipeline

---

## Failure Modes

- **Profile is private or very sparse:** Default to "Defer" unless you have a strong external reason to connect. Do not connect with unknown people who have no visible profile content.
- **Request is blank (no note) from a stranger:** Apply the Relevance + Trust + Risk check. Blank requests from people with relevant profiles are often worth accepting; blank requests from people with no visible connection to your domain usually are not.

---

## Maintenance Notes

Review when LinkedIn changes what is visible on profiles before accepting a connection.

Last reviewed: 2026-03-27
