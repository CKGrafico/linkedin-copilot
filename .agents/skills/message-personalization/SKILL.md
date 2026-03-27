> **Status: ACTIVE** — This file is current and maintained.

# Skill: message-personalization

## What This Skill Does

Identifies personalization hooks in a recipient's LinkedIn profile — shared context, genuine conversation starters, and authentic connection points — and teaches how to use them to make outreach feel specific rather than generic.

---

## Used By

- *(outreach-writer — future agent)*
- [sourcer](../../agents/sourcer/AGENT.md) *(when preparing contact notes)*

---

## When to Apply

After [profile-summary](./`profile-summary.instructions.md) has been completed and before drafting the message with [outreach-drafting](./`outreach-drafting.instructions.md). Personalization hooks are the input to the opening line of any outreach message.

---

## Instructions

### 1. Identify the strongest hook type

Work through these hook categories in order. Use the first strong match you find. Do not use more than one hook per message — multiple hooks dilute focus.

**Category A: Shared context (highest trust)**
- Went to the same university or school
- Worked at the same company (overlapping or sequential)
- Share a mutual connection who you know well
- Are in the same professional group or community

Use: *"We both worked at [Company] — though I think our time there just missed overlapping."*

**Category B: Their recent content (high relevance)**
- They published a post or article in the last 30 days
- They commented on something you also have views on
- They shared a company announcement or milestone

Use: *"I read your post on [topic] — your point about [specific thing] resonated with how I think about it too."*

**Category C: Their career trajectory (shows you actually read their profile)**
- A recent role transition that is meaningful
- An unusual or impressive career move
- A specific company or project in their background that is notable

Use: *"I noticed you moved from [Company A] to [Company B] — that transition from [domain X] to [domain Y] seems like an interesting path."*

**Category D: Their company or team (contextual relevance)**
- Their company just announced something publicly relevant (funding, product launch, hiring)
- Their team is working on something you have genuine interest in

Use: *"I saw [Company] recently announced [news] — congrats on that milestone."*

### 2. Verify the hook is genuine

A personalization hook only works if it is authentic. Ask:
- Would this observation make sense in a face-to-face introduction?
- Is it specific enough that the recipient knows you actually looked at their profile?
- Is it relevant to the purpose of your message, or is it forced?

Discard any hook that fails this test.

### 3. Do not fabricate or exaggerate

Never claim a connection or interest you do not have. Never say "I've been following your work for a long time" unless it is true. Recipients can tell. Fake personalization is worse than no personalization.

### 4. Identify a secondary hook as backup

Sometimes the strongest hook is too sensitive or too personal for a first message (e.g., a recent layoff). Identify a secondary hook in case the primary is unsuitable.

---

## Input Requirements

- The recipient's profile summary (from [profile-summary](./`profile-summary.instructions.md))
- Context about your relationship to them (do you share background, connections, or interests?)
- The purpose of the outreach

---

## Output Format

```
Primary hook: [Category] — [specific observation]
Hook sentence draft: "[One sentence using the hook, as it would appear in the message opening]"
Secondary hook (if applicable): [Category] — [specific observation]
```

---

## Related Skills

- [profile-summary](./`profile-summary.instructions.md) — prerequisite; provides the profile data this skill analyzes
- [outreach-drafting](./`outreach-drafting.instructions.md) — uses the hook output in the message opening line

---

## References

- [outreach-best-practices](../../../references/outreach-best-practices.md) — personalization depth benchmarks
- [profile-evaluation-criteria](../../../references/profile-evaluation-criteria.md) — reading profile signals for hooks

---

## Notes and Caveats

- "Personalization" does not mean mentioning their first name. That is table stakes, not personalization.
- A hook based on their content (Category B) signals that you engaged with their ideas, which is more flattering and persuasive than noting a factual background overlap.
- If no strong hook exists, it is better to write a direct, honest message without a forced hook than to use a weak one.

---

## Maintenance Notes

Review if LinkedIn changes what profile information is publicly visible (activity, posts, background details).

Last reviewed: 2026-03-27
