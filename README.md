# Life OS Workspace

A Notion-style multi-page Life OS web app for entrepreneurship planning, study systems, tasks, and generated operating outputs. Single-file static site — zero build, zero dependencies beyond Google Fonts.

## Pages

Client-side routing via URL hash (`#/dashboard`, `#/planner`, ...) — safe for deployment behind any static host.

- **Dashboard** (`#/dashboard`) — KPI tiles, mission, agenda of open tasks, horizon timeline.
- **Planner** (`#/planner`) — Mission editor, page properties (profile, horizon, study hours, venture thesis), fully editable milestone table (add/delete rows, inline edits, status dropdown).
- **Study** (`#/study`) — Three study tracks, constraints, cadence, energy posture, and a derived weekly-budget split (Build · Learn · Distribute) that updates live.
- **Tasks** (`#/tasks`) — Add/check/delete tasks bound to study tracks; All / Open / Done filters; progress flows to the Dashboard tile.
- **Generator** (`#/generator`) — Produces an operating brief, primary risk, 30-day plan, timeline, and study output from the current inputs.
- **Exports** (`#/exports`) — Live JSON preview of all state; Copy, Download, and paste-to-restore import.

## Shared state

All pages read and write a single in-memory state object. The sandbox blocks `localStorage`, `sessionStorage`, and cookies, so persistence happens through JSON export/import instead.

- Editing any field in Planner/Study immediately updates the Dashboard tiles, Study budget, Details panel, and Exports JSON preview.
- Changing **Horizon** in Planner swaps the milestone table to the matching 3/7/12-year template only when the table is still at a known template, so custom edits are preserved.
- `Generate` in the topbar or on the Generator page refreshes output cards and stamps a timestamp.

## Inputs & outputs

**Input workflows:**
- Rich-text style mission editor
- Structured forms (selects, number inputs, textareas) with focus rings
- Fully editable milestone table with inline cells and add/delete rows
- Task input with track assignment, checkbox toggle, delete
- JSON paste-area with validation

**Output workflows:**
- Live KPI tiles (focus ratio, milestone count, task progress bar, last generated)
- Dashboard agenda card of next open tasks
- Timeline with accent-dotted rail
- Generated brief, risk, 30-day plan, and study output cards
- JSON state preview with Copy and Download

## Keyboard shortcuts

- `1`–`6` — jump between pages
- `G` — regenerate outputs
- `T` — toggle theme

## Responsive

- ≥1200px: three-pane layout (nav · content · details)
- 820–1200px: hides right-hand details panel
- <820px: collapses to single column with a hamburger-driven slide-in sidebar and backdrop

## Run locally

Open `index.html` directly in a browser, or serve the folder with any static server. No build step.

## References

- Notion dashboards: https://www.notion.com/help/dashboards
- Notion layouts: https://www.notion.com/help/layouts
- Notion writing and editing basics: https://www.notion.com/help/writing-and-editing-basics
