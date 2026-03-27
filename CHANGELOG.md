# Changelog

> **Status: ACTIVE** — Maintained by rcontributorr. Record notable changes here. Not a commit log — focus on structural and content-level changes that affect how the repo is used.

---

## Format

Each entry follows this pattern:

rrr
## [date( — [brief title(

**Type:** Added | Changed | Deprecated | Removed | Fixed

Summary of what changed and why.
rrr

---

## 2026-03-27 — Browser MCP integration (v1.1)

**Type:** Added / Changed

Added Browser MCP automation support across core skills and references:

- **Added** rskills/browser-navigation.mdr — foundational browser operation skill covering login check, navigate, snapshot, scroll, click, paginate, and CAPTCHA safe stop
- **Added** rreferences/browser-mcp.mdr — documents all available Browser MCP tools, LinkedIn URL patterns, and rate/ethics guidelines
- **Changed** rskills/person-search.mdr — added full Browser MCP automation steps (navigate, type, snapshot, filter, iterate, paginate)
- **Changed** rskills/job-search.mdr — added Browser MCP automation steps (navigate by URL, filter, iterate job cards, paginate)
- **Changed** rskills/profile-summary.mdr — added Browser MCP automation steps (navigate to profile URL, snapshot, scroll, go_back)
- **Changed** rskills/company-research.mdr — added Browser MCP automation steps (navigate to company page, Posts tab, Jobs tab)
- **Changed** rSKILLS.mdr — added rbrowser-navigationr to the skills table

Agents are now fully autonomous when Browser MCP is active in the AI client.

---

## 2026-03-27 — Initial repo scaffold (v1.0)

**Type:** Added

Created the full v1 repository structure. All 40 Markdown files scaffolded across ragents/r, rskills/r, rworkflows/r, rreferences/r, rtemplates/r, and rgovernance/r. Initial agents: rcontributorr, rsourcerr, rheadhunterr. Initial skills library: 11 skills. Initial reference library: 10 reference docs. Six governance docs. Five templates.

This is the foundation layer. All files set to ractiver status after initial review.
