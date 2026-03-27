> **Status: ACTIVE** — This file is current and maintained.

# Skill: outreach-drafting

## What This Skill Does

Provides a framework for drafting effective LinkedIn outreach messages: choosing the right message type, structuring the message, calibrating length and tone, writing a compelling call to action, and avoiding common failure patterns.

---

## Used By

- *(outreach-writer — future agent)*
- [sourcer](../agents/sourcer.instructions.md) *(when preparing initial contact notes)*

---

## When to Apply

When preparing to send a LinkedIn message to someone — whether a connection request note, a direct message, or an InMail. Apply after [profile-summary](./`profile-summary.instructions.md) has been completed and personalization hooks have been identified.

---

## Instructions

### 1. Choose the message type

**Connection request note** (up to 300 characters)
- Used when requesting to connect with a 2nd or 3rd degree contact
- Must be very concise: who you are, why you are connecting, one line only
- Do not ask for anything in the connection note — just establish the connection

**Direct message** (1st degree connections, up to ~2,000 characters practical limit)
- Used for substantive outreach to existing connections
- More space to explain, but brevity is still a virtue
- Maximum effective length: 5–7 sentences

**InMail** (LinkedIn Premium, anyone)
- Used for cold outreach when no connection exists
- Subject line matters — treat it like an email subject
- Body follows the same structure as a direct message

### 2. Structure every message

Follow this structure regardless of message type:

**Opening (1 sentence):** A specific, genuine observation about the recipient. Not a generic compliment. Reference something real: a post they wrote, a career move, a shared connection, a company achievement.

**Bridge (1 sentence):** Connect the opening observation to why you are reaching out. This is the logical link between "why I noticed you" and "why I am writing."

**Purpose (1–2 sentences):** State clearly what you are asking for or proposing. Be direct. Vague asks ("I'd love to connect") are less effective than specific ones ("I'd love 20 minutes to hear about your experience hiring at X stage").

**Close (1 sentence):** A low-friction call to action. Make it easy to say yes or no. "Happy to hop on a quick call, or if email is easier — [email]" is better than "let me know what you think."

### 3. Calibrate length

- Connection request note: 1–2 sentences maximum (300 char limit)
- Direct message to a recruiter: 4–6 sentences
- InMail to a hiring manager: 5–7 sentences
- Cold message to someone you have no context on: lean short (4 sentences)
- Message with strong shared context (alumni, mutual friend): can be up to 8 sentences

**When in doubt, cut.** The most common mistake is writing too much.

### 4. Apply personalization

Before sending, verify the message includes at least one specific detail unique to this recipient. Generic messages are immediately recognizable and get lower response rates. For personalization techniques, see [message-personalization](./`message-personalization.instructions.md).

### 5. Write the call to action correctly

A good call to action:
- Specifies a concrete next step (call, email, coffee, response to one question)
- Makes it easy to decline without awkwardness (low pressure)
- Does not create work for the recipient (do not ask them to find time on your calendar in a first message)

A bad call to action:
- "Let me know your thoughts" (vague, no clear ask)
- "I'd love to pick your brain" (clichéd, no specific value proposition)
- "Please let me know when you are available" (puts effort on them)

---

## Input Requirements

- The recipient's profile summary (from [profile-summary](./`profile-summary.instructions.md))
- The purpose of the outreach (what are you asking for?)
- Personalization hooks (from [message-personalization](./`message-personalization.instructions.md))
- Message type (connection request / direct message / InMail)

---

## Output Format

A complete draft message, labeled with:
- Message type
- Character/word count
- A note on the personalization hook used

---

## Related Skills

- [profile-summary](./`profile-summary.instructions.md) — provides the recipient context needed before drafting
- [message-personalization](./`message-personalization.instructions.md) — provides the personalization hooks used in the opening

---

## References

- [outreach-best-practices](../../../references/outreach-best-practices.md) — what makes outreach effective vs. ignored
- [ethical-boundaries](../../../references/ethical-boundaries.md) — acceptable outreach volume and behavior

---

## Notes and Caveats

- Never use a message template unchanged. Templates are starting points, not finished messages.
- Avoid common phrases that signal a generic message: "I came across your profile," "I hope this message finds you well," "I'd love to connect."
- Do not follow up more than once if there is no response to a cold message. One follow-up after 7–10 days is acceptable. Beyond that, move on.

---

## Maintenance Notes

Review when LinkedIn changes its message interface or character limits.

Last reviewed: 2026-03-27
