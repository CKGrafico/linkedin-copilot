> **Status: ACTIVE** — This file is current and maintained.

# Reference: linkedin-usage-patterns

## Summary

Documents how LinkedIn works as a platform — its visibility mechanics, search ranking behavior, connection degree effects, messaging options, and activity dynamics. Agents consult this to understand the rules of the environment they are operating in.

---

## Key Facts

- LinkedIn search results are personalized. Two users running the same query will see different results based on their networks, activity, and account type.
- 2nd-degree connections are the most actionable target for sourcing: warm enough to approach, broad enough to be useful.
- Connection request notes are limited to 300 characters and are often the first impression.
- LinkedIn limits free InMail; premium InMail credits are monthly and do not roll over indefinitely.
- Profiles that are actively maintained (recent updates, recent activity) rank higher in search results.
- LinkedIn's algorithm deprioritizes profiles not logged into regularly — dormant accounts may not appear in searches.

---

## Detailed Notes

### Search result ranking

LinkedIn's People search ranks results based on several factors:
- **Network proximity:** 1st and 2nd degree connections rank higher than 3rd+
- **Profile completeness:** More complete profiles are surfaced more often
- **Activity recency:** Recently active users rank higher
- **Keyword relevance:** Profiles are indexed on all text, not just the headline
- **Premium status:** Premium account holders may appear higher in some contexts

Practical implication: a highly relevant person with a sparse, dormant profile may not appear in your search results at all.

### Connection degrees

- **1st degree:** Direct connections. Can message freely. Already in your network.
- **2nd degree:** Mutual connections exist. Can send a connection request (with optional note). Warm path possible via mutual.
- **3rd degree+:** No direct connection path. Can send InMail (premium) or follow them to build visibility before a connection request. Response rates are lower.
- **Open profiles:** Some users set their profile to "Open" which allows anyone to message them for free via InMail credits.

### Visibility and privacy

- LinkedIn shows profile viewers to the person viewed (unless viewing in private mode). Private browsing mode hides your identity but you also lose the ability to see who viewed you.
- Some users hide their connection count. This limits your ability to assess network breadth from their profile.
- A profile with "500+ connections" is the maximum displayed. No way to know exact network size.

### Activity signals

- The "Activity" section shows recent posts, comments, and likes (with some privacy controls)
- Users who have posted in the last 30 days are generally more "active" on the platform
- Commenting on another user's content is visible to their connections — a non-intrusive way to get into someone's peripheral awareness before outreach
- Following a user (without connecting) adds you to their follower count and can trigger profile view notifications

### Messaging mechanics

- **Connection request note:** 300 characters. Shown before the recipient accepts.
- **Direct message:** Available to 1st-degree connections. Practical limit ~2,000 characters for readable messages.
- **InMail:** LinkedIn Premium feature. Reaches anyone. Monthly credit limit (15 for basic premium). Credits are refunded if the recipient responds.
- **Message requests (non-premium):** If someone follows you or if you are in the same LinkedIn Group, you can message without a connection in some cases.

---

## When Agents Should Consult This

- [sourcer](../.agents/agents/sourcer/AGENT.md) — for understanding search ranking and outreach channel selection
- [headhunter](../.agents/agents/headhunter/AGENT.md) — for understanding job search visibility and company page signals
- [.agents/skills/search-query-design/SKILL.md](../.agents/skills/search-query-design/SKILL.md) — for understanding how queries interact with ranking

---

## Sources and Basis

Platform behavior observed through direct use. LinkedIn's official documentation is sparse; most patterns are empirical.

---

## Maintenance Notes

LinkedIn changes its interface and algorithm frequently. Review this file when significant platform changes are announced or observed. Key things to watch: search filter changes, messaging limit changes, activity visibility changes.

Last reviewed: 2026-03-27
