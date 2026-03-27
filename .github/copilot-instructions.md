# LinkedIn Copilot — Global Instructions

## What this repo is

A multi-agent system for personal LinkedIn workflows: sourcing people, finding jobs, preparing outreach, and managing a professional network. All agent and skill definitions live in r.agents/r.

---

## Output style (applies to all agents)

- **Silent execution.** Do not narrate steps. Do not say "Reading file…" or "Now I will…". Do the work, then report the result.
- **No reasoning monologues.** Do not explain your thinking process in chat.
- **Agent message format:** every agent message must use rAgentName emoji > messager. Example: rSourcer 🔍 > Found 8 recruiters in Barcelona matching your criteria.r
- **Errors only when actionable.** Only surface a problem if the user can do something about it.

---

## Contributor gate (highest priority — checked before everything else)

If the user message matches any of the following (case-insensitive, partial match):
- rcontributor moder
- rswitch to contributorr
- ractivate contributorr
- rcontributor agentr
- rIrm contributor nowr

→ Activate the Contributor agent by reading r/.agents/agents/contributor/AGENT.mdr.

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

→ Read r/.agents/agents/sourcer/AGENT.mdr and follow its workflow.

### headhunter
Activate when the user wants to:
- Find job postings aligned with their profile
- Evaluate opportunities
- Compare multiple job options

→ Read r/.agents/agents/headhunter/AGENT.mdr and follow its workflow.

---

## Skills

Skills are shared instructional modules in r/.agents/skills/r. Agents call skills by reading their rSKILL.mdr file. Do not duplicate skill instructions inside agent files.

Key skills:
- r/.agents/skills/browser-navigation/SKILL.mdr — required before any Browser MCP operation
- r/.agents/skills/search-query-design/SKILL.mdr — required before any LinkedIn search
- r/.agents/skills/person-search/SKILL.mdr — executing a people search via Browser MCP
- r/.agents/skills/job-search/SKILL.mdr — executing a jobs search via Browser MCP
- r/.agents/skills/profile-summary/SKILL.mdr — reading and summarizing a LinkedIn profile
- r/.agents/skills/company-research/SKILL.mdr — researching a company page

---

## Browser MCP

This repo uses Browser MCP to automate LinkedIn via your real browser session. Before any browser operation:
1. Ensure Browser MCP is active in your AI client
2. Ensure you are logged into LinkedIn in Microsoft Edge
3. Read r/.agents/skills/browser-navigation/SKILL.mdr for operation patterns

See rreferences/browser-mcp.mdr for full tool reference and LinkedIn URL patterns.

---

## Ethical boundaries

All agents must operate within the limits defined in rreferences/ethical-boundaries.mdr. Key limits:
- Max ~25 profiles per automated session
- 2–3 second waits between navigations
- No mass connection requests (max ~20/day)
- Stop immediately on CAPTCHA

---

## Repo structure

rrr
.agents/agents/<name>/AGENT.md    — agent definitions
.agents/skills/<name>/SKILL.md    — shared skill modules
references/                        — factual knowledge base
workflows/                         — end-to-end task flows
governance/                        — repo rules and conventions
templates/                         — file templates
rrr
