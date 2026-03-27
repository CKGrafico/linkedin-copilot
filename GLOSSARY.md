# Glossary

> **Status: ACTIVE** — Maintained by rcontributorr. When a new term enters common use across two or more files, it belongs here. Update rCHANGELOG.mdr when entries are added or changed.

This glossary defines terms used across agents, skills, workflows, and references in this repo. Consistent vocabulary prevents drift. When in doubt, check here first.

---

## A

**Active status** — A file that is complete, reviewed, and the authoritative source for its topic. Indicated by the rACTIVEr status banner. See [governance/status-model.md((governance/status-model.md).

**Agent** — A Markdown file that defines a focused AI role: its mission, inputs, outputs, skills used, guardrails, and handoff rules. An agent file is the complete operating manual for one AI persona.

**Archived status** — A file that is no longer maintained, retained only for historical reference. Indicated by the rARCHIVEDr status banner. See [governance/status-model.md((governance/status-model.md).

---

## B

**Boolean query** — A search query that uses Boolean operators (rANDr, rORr, rNOTr) to combine and filter terms. Used extensively in LinkedIn search. See [skills/search-query-design.md((skills/search-query-design.md).

---

## C

**Candidate** — In the context of rsourcerr, a person identified as a potential valuable contact: recruiter, hiring manager, connector, or subject-matter expert. Not to be confused with a job candidate.

**Connection request** — A LinkedIn feature for requesting to connect with someone at 2nd or 3rd degree. Distinct from InMail, which can reach anyone.

**Contributor** — The repo maintenance agent. The only agent authorized to modify repo files. See [agents/contributor.md((agents/contributor.md).

**Contributor request** — A structured request asking rcontributorr to make a specific change to the repo. Submitted using [templates/contributor-request.md((templates/contributor-request.md).

---

## D

**Degree (1st, 2nd, 3rd)** — LinkedInrs connection proximity model. 1st-degree connections are direct connections. 2nd-degree are connections of connections. 3rd-degree are one step further. Search visibility and outreach options vary by degree.

**Deprecated status** — A file that is no longer current, replaced by a newer file. Indicated by the rDEPRECATEDr status banner. See [governance/status-model.md((governance/status-model.md).

**Draft status** — A file that is in progress and should not be relied upon. Indicated by the rDRAFTr status banner. See [governance/status-model.md((governance/status-model.md).

---

## F

**Fit** — How well a person, role, or company aligns with the userrs stated criteria: skills match, seniority, location, culture, domain.

**Follow-up** — A planned subsequent action after an initial contact or search session. See [skills/follow-up-planning.md((skills/follow-up-planning.md).

---

## G

**Guardrails** — Hard constraints on an agentrs behavior. Listed in the **Guardrails** section of every agent file. Non-negotiable rules the agent must never violate.

---

## H

**Handoff** — The process by which one agentrs output becomes another agentrs input. Handoffs are documented in each agentrs **Handoff Rules** section and in [governance/handoff-conventions.md((governance/handoff-conventions.md).

**Headhunter** — The job and opportunity discovery agent. See [agents/headhunter.md((agents/headhunter.md).

**Hiring manager** — A person with authority to make or strongly influence a hiring decision for a specific role.

---

## I

**InMail** — LinkedInrs premium direct messaging feature. Allows contacting anyone on LinkedIn regardless of connection status, subject to monthly credit limits.

---

## K

**Knowledge base** — The rreferences/r folder. Contains factual documents about LinkedIn, sourcing, job search, outreach, and professional norms that agents consult but do not generate.

---

## L

**Lead** — A person or opportunity that has been identified as potentially valuable and is being tracked or prioritized.

**Lead ranking** — The process of prioritizing a list of leads using weighted signals. See [skills/lead-ranking.md((skills/lead-ranking.md).

---

## O

**Opportunity** — A job posting, consulting engagement, or professional opening that the user might pursue.

**Outreach** — A message sent to someone on LinkedIn with the intent of initiating a professional relationship or conversation.

---

## P

**Pipeline** — An informal list of active leads (people or opportunities) being tracked across sessions. Maintained in session notes, not in repo files.

**Profile** — A LinkedIn userrs public page: work history, education, skills, activity, and headline.

---

## R

**Reference** — A Markdown file in rreferences/r containing factual knowledge that agents consult. References describe *what is true*; skills describe *how to do things*.

**Recruiter signal** — Observable LinkedIn activity patterns that indicate a recruiter is actively sourcing. See [references/recruiter-signals.md((references/recruiter-signals.md).

---

## S

**Session notes** — Structured output produced at the end of an agent session using the [note-taking skill((skills/note-taking.md). Stored outside the repo (in the userrs own files). Can be passed to future agent sessions as context.

**Skill** — A reusable instructional module in rskills/r that teaches one discrete capability. Multiple agents can use the same skill.

**Sourcer** — The person discovery agent. See [agents/sourcer.md((agents/sourcer.md).

**Status banner** — A Markdown blockquote at the top of a file declaring the filers lifecycle status: rdraftr, ractiver, rdeprecatedr, or rarchivedr.

---

## T

**Target criteria** — The userrs stated requirements for what they are looking for: industry, role, seniority, geography, company size, etc.

---

## W

**Workflow** — A Markdown file in rworkflows/r describing an end-to-end task flow from trigger to output, naming which agents and skills participate at each step.
