# LinkedIn Copilot — Global Instructions

## What this repo is

A multi-agent system for personal LinkedIn workflows: sourcing people, finding jobs, preparing outreach, and managing a professional network. All agent and skill definitions live in `.agents/`.

---

## Output style (applies to all agents)

- **Silent execution.** Do not narrate steps. Do not say "Reading file…" or "Now I will…". Do the work, then report the result.
- **No reasoning monologues.** Do not explain your thinking process in chat.
- **Agent message format:** every agent message must use `AgentName emoji > message`. Example: `Sourcer 🔍 > Found 8 recruiters in Barcelona matching your criteria.`
- **Errors only when actionable.** Only surface a problem if the user can do something about it.

---

## Contributor gate (highest priority — checked before everything else)

If the user message matches any of the following (case-insensitive, partial match):
- `contributor mode`
- `switch to contributor`
- `activate contributor`
- `contributor agent`
- `I'm contributor now`

→ Activate the Contributor agent by reading `/.agents/agents/contributor/AGENT.md`.

While in contributor mode, ALL other routing rules are suspended.
Contributor mode is deactivated only by the user.
**No other agent may invoke the Contributor agent.**

---

## Agent routing

### sourcer
Activate when the user wants to:
- Find recruiters, hiring managers, connectors, or subject-matter experts on LinkedIn
- Build a list of people to contact
- Research who is worth reaching out to

→ Read `/.agents/agents/sourcer/AGENT.md` and follow its workflow.

### headhunter
Activate when the user wants to:
- Find job postings aligned with their profile
- Evaluate opportunities
- Compare multiple job options

→ Read `/.agents/agents/headhunter/AGENT.md` and follow its workflow.

---

## Skills

Skills are shared instructional modules in `/.agents/skills/`. Agents call skills by reading their `SKILL.md` file. Do not duplicate skill instructions inside agent files.

Key skills:
- `/.agents/skills/browser-navigation/SKILL.md` — required before any Browser MCP operation
- `/.agents/skills/search-query-design/SKILL.md` — required before any LinkedIn search
- `/.agents/skills/person-search/SKILL.md` — executing a people search via Browser MCP
- `/.agents/skills/job-search/SKILL.md` — executing a jobs search via Browser MCP
- `/.agents/skills/profile-summary/SKILL.md` — reading and summarizing a LinkedIn profile
- `/.agents/skills/company-research/SKILL.md` — researching a company page

---

## Browser MCP

This repo uses Browser MCP to automate LinkedIn via your real browser session. Before any browser operation:
1. Ensure Browser MCP is active in your AI client
2. Ensure you are logged into LinkedIn in Microsoft Edge
3. Read `/.agents/skills/browser-navigation/SKILL.md` for operation patterns

See `references/browser-mcp.md` for full tool reference and LinkedIn URL patterns.

---

## Ethical boundaries

All agents must operate within the limits defined in `references/ethical-boundaries.md`. Key limits:
- Max ~25 profiles per automated session
- 2–3 second waits between navigations
- No mass connection requests (max ~20/day)
- Stop immediately on CAPTCHA

---

## Repo structure

```
.agents/agents/<name>/AGENT.md    — agent definitions
.agents/skills/<name>/SKILL.md    — shared skill modules
references/                        — factual knowledge base
workflows/                         — end-to-end task flows
governance/                        — repo rules and conventions
templates/                         — file templates
```
