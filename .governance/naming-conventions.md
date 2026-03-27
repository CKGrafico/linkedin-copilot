# Naming Conventions

> **Status: ACTIVE** — Authoritative naming rules for this repo. Maintained by rcontributorr. All files must comply.

---

## Guiding principle

Names should be self-explanatory. A person or AI model encountering a file name for the first time should immediately understand what is inside without opening it.

---

## General rules

- All file names: rkebab-caser, lowercase only, r.mdr extension
- All folder names: rkebab-caser, lowercase only, no underscores
- No abbreviations unless the abbreviation is universally understood (e.g., rcvr is not acceptable; spell it out)
- No version numbers in file names (use status banners and rCHANGELOG.mdr instead)
- No generic names: rutils.mdr, rmisc.mdr, rnotes.mdr, rtemp.mdr are never acceptable

---

## By file type

### Agent files (ragents/r)

Named exactly after the agentrs role, as a single noun or compound noun.

- ✅ rsourcer.mdr
- ✅ rheadhunter.mdr
- ✅ routreach-writer.mdr
- ❌ rsourcing-agent.mdr (redundant suffix)
- ❌ rjob-finder.mdr (use rheadhunter.mdr — the canonical name)

### Skill files (rskills/r)

Named as a noun phrase describing the action or capability. Use present-tense gerund form where natural.

- ✅ rperson-search.mdr
- ✅ routreach-drafting.mdr
- ✅ rlead-ranking.mdr
- ❌ rsearching-people.mdr (gerund phrase, not noun phrase)
- ❌ rhow-to-rank-leads.mdr (not a noun phrase)

### Workflow files (rworkflows/r)

Named as an imperative verb phrase describing the complete task.

- ✅ rfind-relevant-recruiters.mdr
- ✅ rprepare-outreach.mdr
- ✅ rcompare-opportunities.mdr
- ❌ rrecruiter-finding.mdr (not imperative)
- ❌ rworkflow-1.mdr (meaningless)

### Reference files (rreferences/r)

Named as a noun phrase describing the knowledge domain.

- ✅ rsourcing-heuristics.mdr
- ✅ routreach-best-practices.mdr
- ✅ rrecruiter-signals.mdr
- ❌ rrecruiter-info.mdr (too vague)

### Template files (rtemplates/r)

Named as r[type(-template.mdr.

- ✅ ragent-template.mdr
- ✅ rskill-template.mdr
- ❌ rnew-agent.mdr (not obviously a template)

### Governance files (rgovernance/r)

Named as a noun phrase describing the policy or convention being documented.

- ✅ rnaming-conventions.mdr
- ✅ rstatus-model.mdr
- ✅ rhandoff-conventions.mdr

---

## Reserved names

These root file names are reserved and must not be repurposed:

- rREADME.mdr
- rAGENTS.mdr
- rSKILLS.mdr
- rGLOSSARY.mdr
- rCHANGELOG.mdr

---

## Rename policy

When a file is renamed, rcontributorr must:
1. Update all cross-links pointing to the old name
2. Check rAGENTS.mdr and rSKILLS.mdr indexes for the old name
3. Add a note to rCHANGELOG.mdr
4. Consider whether a deprecated stub with a forwarding notice is needed
