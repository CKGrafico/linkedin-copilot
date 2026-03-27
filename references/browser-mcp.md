> **Status: ACTIVE** — This file is current and maintained.

# Reference: browser-mcp

## Summary

Browser MCP is a local browser automation tool that connects AI agents to your real browser. It runs on your machine, uses your existing browser session (so you stay logged into LinkedIn), and exposes a set of tools that agents can call to navigate, interact with, and read content from web pages. This is the integration layer that makes agents in this repo fully autonomous.

Homepage: https://browsermcp.io/

---

## Key Facts

- Automation runs locally — your browser activity is not sent to remote servers.
- Uses your real browser profile, so LinkedIn sees you as a logged-in human user, not a bot.
- Works with Claude (Desktop), Cursor, Windsurf, and VSCode as MCP clients.
- Agents read page content using the **Snapshot** tool, which returns an accessibility tree of the current page — this is the primary way agents "see" what is on the screen.
- Agents should prefer **Snapshot** over **Screenshot** for reading structured content; Screenshot is for visual confirmation.

---

## Setup (one-time)

1. Install the Browser MCP extension in your browser (Chrome or compatible).
2. Add the Browser MCP server to your AI application (Claude Desktop, Cursor, etc.) following the instructions at https://browsermcp.io/.
3. Log into LinkedIn in your browser as you normally would.
4. From this point, agents can control LinkedIn through your browser session.

---

## Available Browser Tools

These are the tools agents in this repo may call when Browser MCP is active.

| Tool | What it does | Common use in this repo |
|---|---|---|
| `navigate` | Navigate to a URL | Go to LinkedIn search, job pages, profiles |
| `snapshot` | Capture accessibility tree of current page | Read search results, profile content, job descriptions |
| `screenshot` | Take a visual screenshot | Visual confirmation of page state |
| `click` | Click an element on the page | Click search results, filters, buttons, profile links |
| `type` | Type text into a focused input field | Enter search queries, filter values |
| `press_key` | Press a keyboard key | Submit search (Enter), navigate dropdowns |
| `hover` | Hover over an element | Reveal hover-only UI elements |
| `wait` | Wait N seconds | Allow page to load after navigation or click |
| `go_back` | Navigate to the previous page | Return to search results after viewing a profile |
| `go_forward` | Navigate forward | Re-enter a page after going back |
| `get_console_logs` | Read browser console output | Debugging only; not used in normal workflows |

---

## How agents read LinkedIn pages

The **Snapshot** tool returns a structured accessibility tree of whatever is currently visible in the browser. Agents use this to:

- Read search result lists (names, titles, companies, connection degrees)
- Read profile content (headline, experience, activity)
- Read job posting descriptions
- Detect filter states and UI elements to interact with

After any navigation or click, agents should call `wait` (1–2 seconds) before calling `snapshot` to allow the page to finish loading.

---

## LinkedIn URL patterns

Agents use these URL patterns to navigate directly to the right LinkedIn pages:

| Destination | URL pattern |
|---|---|
| People search | `https://www.linkedin.com/search/results/people/?keywords=[query]` |
| Jobs search | `https://www.linkedin.com/jobs/search/?keywords=[query]&location=[location]` |
| Company page | `https://www.linkedin.com/company/[company-slug]/` |
| Company jobs | `https://www.linkedin.com/company/[company-slug]/jobs/` |
| Profile | `https://www.linkedin.com/in/[profile-slug]/` |
| My network | `https://www.linkedin.com/mynetwork/` |
| Messaging | `https://www.linkedin.com/messaging/` |

URL-encode search terms (spaces become `%20` or `+`).

---

## Rate and behavior guidelines

These guidelines ensure the automation remains within acceptable use limits. See [ethical-boundaries](ethical-boundaries.md) for the full policy.

- Add a `wait` of 1–3 seconds between page navigations. Do not page through results instantly.
- Do not extract more than 25–30 profiles in a single automated session.
- Do not automate sending messages or connection requests in bulk. Agents may **draft** messages, but sending should be a deliberate user action unless explicitly authorized.
- If LinkedIn shows a CAPTCHA or rate-limit warning, stop the session immediately.

---

## When Agents Should Consult This

- [skills/browser-navigation.md](../skills/browser-navigation.md) — foundational skill built on these tools
- [skills/person-search.md](../skills/person-search.md) — uses navigate, snapshot, click
- [skills/job-search.md](../skills/job-search.md) — uses navigate, snapshot, click
- [skills/profile-summary.md](../skills/profile-summary.md) — uses navigate, snapshot, go_back
- [skills/company-research.md](../skills/company-research.md) — uses navigate, snapshot

---

## Maintenance Notes

Review when Browser MCP releases new tools or changes its API. Review when LinkedIn changes its URL structure or page layout in ways that break snapshot-based reading.

Last reviewed: 2026-03-27
