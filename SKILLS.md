# Skills

> **Status: ACTIVE** — This index is maintained by rcontributorr. Update it whenever a skill is added, deprecated, or archived.

This is the master index of all shared skills in this repo. A skill is a reusable instructional module — a discrete, teachable capability that one or more agents can apply. Skills live here so that improvements benefit every agent that uses them.

---

## Skills Library

| Skill | File | What it does | Used by |
|---|---|---|---|
| rbrowser-navigationr | [.agents/skills/browser-navigation/SKILL.md((.agents/skills/browser-navigation/SKILL.md) | Foundational Browser MCP operation patterns: login check, navigate, snapshot, click, paginate | all browser-enabled skills |
| rsearch-query-designr | [.agents/skills/search-query-design/SKILL.md((.agents/skills/search-query-design/SKILL.md) | Constructs effective LinkedIn search queries using Boolean operators, filters, and keyword strategies | rsourcerr, rheadhunterr |
| rperson-searchr | [.agents/skills/person-search/SKILL.md((.agents/skills/person-search/SKILL.md) | Searches for people on LinkedIn via Browser MCP: filter selection, result interpretation, lead identification | rsourcerr |
| rjob-searchr | [.agents/skills/job-search/SKILL.md((.agents/skills/job-search/SKILL.md) | Searches for job postings via Browser MCP: parameters, freshness evaluation, noise filtering | rheadhunterr |
| rprofile-summaryr | [.agents/skills/profile-summary/SKILL.md((.agents/skills/profile-summary/SKILL.md) | Extracts key information from a LinkedIn profile via Browser MCP: role, trajectory, signals, fit indicators | rsourcerr, rheadhunterr |
| ropportunity-qualificationr | [.agents/skills/opportunity-qualification/SKILL.md((.agents/skills/opportunity-qualification/SKILL.md) | Evaluates whether a job or opportunity is worth pursuing given stated criteria | rheadhunterr |
| rcompany-researchr | [.agents/skills/company-research/SKILL.md((.agents/skills/company-research/SKILL.md) | Researches a company via Browser MCP: size, growth, hiring patterns, culture | rheadhunterr |
| rlead-rankingr | [.agents/skills/lead-ranking/SKILL.md((.agents/skills/lead-ranking/SKILL.md) | Ranks and prioritizes a list of people or opportunities using weighted signals | rsourcerr, rheadhunterr |
| routreach-draftingr | [.agents/skills/outreach-drafting/SKILL.md((.agents/skills/outreach-drafting/SKILL.md) | Drafts effective LinkedIn outreach messages: structure, length, tone, call to action | *(outreach-writer, sourcer)* |
| rmessage-personalizationr | [.agents/skills/message-personalization/SKILL.md((.agents/skills/message-personalization/SKILL.md) | Personalizes messages using profile data: hooks, shared context, authentic connection points | *(outreach-writer)* |
| rnote-takingr | [.agents/skills/note-taking/SKILL.md((.agents/skills/note-taking/SKILL.md) | Records structured session outputs for reuse in future sessions | all agents |
| rfollow-up-planningr | [.agents/skills/follow-up-planning/SKILL.md((.agents/skills/follow-up-planning/SKILL.md) | Plans next steps and follow-up actions after a search or outreach session | rsourcerr, rheadhunterr |

---

## How to add a new skill

1. Copy [rtemplates/skill-template.mdr((templates/skill-template.md) to rskills/your-skill-name.mdr.
2. Fill in all sections. Be precise about inputs, outputs, and which agents use it.
3. Set status to rdraftr.
4. Submit a [rcontributor-requestr((templates/contributor-request.md) to have rcontributorr review, update this index, and set status to ractiver.

---

## Key rules

- Skills are shared. If an instruction appears in more than one agent doc, it must become a skill.
- Skills are instructional. Factual knowledge belongs in rreferences/r, not rskills/r.
- Skills may reference each other directionally. No circular references.
- Only rcontributorr may add or remove entries from this index.

See [governance/naming-conventions.md((governance/naming-conventions.md) for naming rules.
