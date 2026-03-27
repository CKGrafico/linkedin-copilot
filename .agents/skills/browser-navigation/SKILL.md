> **Status: ACTIVE** — This file is current and maintained.

# Skill: browser-navigation

## What This Skill Does

Provides the foundational patterns for operating LinkedIn through Browser MCP — navigating to pages, reading content with Snapshot, interacting with UI elements, and handling common LinkedIn page behaviors. All other browser-enabled skills build on this one.

---

## Used By

- [sourcer((../../agents/sourcer/AGENT.md)
- [headhunter((../../agents/headhunter/AGENT.md)
- *(all future agents that use Browser MCP)*

---

## Prerequisite

Browser MCP must be installed and connected to your AI application. See [references/browser-mcp.md((../../../references/browser-mcp.md) for setup instructions. You must be logged into LinkedIn in **Microsoft Edge** (or whichever browser has the extension installed) before starting any automated session.

---

## When to Apply

At the start of any agent session that uses Browser MCP. This skill defines the standard operating patterns. Other skills (person-search, job-search, etc.) call out specific steps, but those steps rely on the patterns established here.

---

## Instructions

### 1. Verify LinkedIn is accessible

Before starting any workflow:

rrr
navigate: https://www.linkedin.com/feed/
wait: 2
snapshot
rrr

Read the snapshot. If you see the LinkedIn feed, you are logged in and ready. If you see a login page, stop and ask the user to log into LinkedIn first.

### 2. Navigate to a destination

Always navigate using direct URLs where possible (faster and more reliable than clicking through menus). See the URL patterns table in [references/browser-mcp.md((../../../references/browser-mcp.md).

After every rnavigater call:
rrr
wait: 2
snapshot
rrr

Always read the snapshot after navigating to confirm you are on the right page before proceeding.

### 3. Read page content with Snapshot

rsnapshotr returns the accessibility tree of the current page. LinkedIn renders content as a list of elements with roles (e.g., rlistitemr, rlinkr, rheadingr). Key patterns to recognize:

**Search results:** Each result is typically a rlistitemr containing a personrs name (as a link), their headline, their location, and their connection degree. Scan for these elements.

**Profile page:** The headline is near the top. Experience items are in a section labeled "Experience." Activity posts are in a section labeled "Activity."

**Job postings:** Title and company appear near the top. Description is in the main content area. Applicant count and "Easy Apply" status are typically near the apply button.

If the snapshot is truncated or incomplete, the page may still be loading. Call rwait: 2r and rsnapshotr again.

### 4. Click elements

Identify the element from the snapshot (by its accessible name or role), then click it:

rrr
click: [element description from snapshot(
wait: 2
snapshot
rrr

For profile links in search results: click the personrs name link to open their profile.
For filter dropdowns: click the filter button label.
For "Next page" pagination: click the "Next" button or page number.

### 5. Type into search fields

To enter a search query:

rrr
click: [search input field(
type: [your search query(
press_key: Enter
wait: 3
snapshot
rrr

Wait 3 seconds after pressing Enter to allow search results to load.

### 6. Apply LinkedIn filters

LinkedIn filters appear as buttons above search results. To apply a filter:

rrr
click: [filter button label, e.g. "Connections"(
wait: 1
snapshot
rrr

Then select the desired option from the dropdown that appears.

Common filter interaction pattern for multi-step filters (e.g., "All Filters"):
rrr
click: All filters
wait: 1
snapshot
[select options in the panel(
click: Show results
wait: 2
snapshot
rrr

### 7. Navigate between search results and profiles

Standard pattern for reviewing multiple profiles:

rrr
[From search results page(
click: [personrs name link(
wait: 2
snapshot
[Read profile content(
go_back
wait: 2
snapshot
[Continue with next result(
rrr

### 8. Handle pagination

To move to the next page of results:
rrr
click: Next [or the page number(
wait: 3
snapshot
rrr

If there is no "Next" button visible in the snapshot, you have reached the last page of results.

### 9. Taking screenshots for confirmation

Use rscreenshotr sparingly — it is for visual confirmation when the accessibility snapshot is ambiguous. Prefer rsnapshotr for reading content.

### 10. Stopping safely

If LinkedIn shows a CAPTCHA, security check, or rate-limit notice (check the snapshot for these), stop immediately:
- Do not attempt to solve CAPTCHAs automatically
- Report the stop to the user with the current state of any results collected so far
- Save partial results using [note-taking((./rnote-taking.instructions.md)

---

## Input Requirements

- Browser MCP connected and active
- User logged into LinkedIn in the browser
- The navigation destination or task to perform

---

## Output Format

This skill produces navigation state (the agent is now on a specific page) rather than a document output. The output of each step is the snapshot content that subsequent skills consume.

---

## Related Skills

- [person-search((./rperson-search.instructions.md) — uses this skill for people search navigation
- [job-search((./rjob-search.instructions.md) — uses this skill for jobs search navigation
- [profile-summary((./rprofile-summary.instructions.md) — uses this skill to navigate to and read profiles
- [company-research((./rcompany-research.instructions.md) — uses this skill to navigate to company pages

---

## References

- [browser-mcp((../../../references/browser-mcp.md) — available tools, URL patterns, rate guidelines
- [ethical-boundaries((../../../references/ethical-boundaries.md) — behavior limits for automated sessions

---

## Notes and Caveats

- LinkedInrs page structure changes frequently. If a snapshot-based step fails to find an expected element, take a rscreenshotr to see the current state and adapt.
- LinkedIn may show interstitial prompts (e.g., "Add to your network?" dialogs, premium upsell banners). Dismiss these with a click before continuing.
- Do not run automated sessions while actively using LinkedIn yourself in the same browser tab — this creates conflicts.

---

## Maintenance Notes

Review when LinkedIn changes its page layout significantly or when Browser MCP updates its tool interface.

Last reviewed: 2026-03-27
