# QA Inventory — Life OS full-function upgrade

## User-visible claims to verify
- Six-page hash-routed navigation works across Dashboard, Planner, Study, Tasks, Generator, and Exports.
- Planner, Study, and Tasks inputs update shared outputs across Dashboard, Details, Generator, and Exports.
- Generator refreshes operating outputs and timestamps.
- JSON export and restore work for persistence in the sandbox.
- Keyboard shortcuts 1–6, G, and T work.
- Mobile layout uses a slide-in sidebar without horizontal overflow.

## Controls and expected state changes
- Sidebar nav links and route-link buttons change the active page and breadcrumbs.
- Planner form fields change KPI tiles, details panel, and JSON preview.
- Milestone table add/delete/edit changes milestone count, dashboard timeline, and exports.
- Study inputs change weekly budget and detail values.
- Task add/toggle/delete/filter changes task list, dashboard agenda, and progress tiles.
- Generator buttons update output cards and last-generated timestamps.
- Export copy/download and restore textarea/file input affect JSON persistence flow.
- Theme toggle and keyboard shortcut T switch appearance.
- Keyboard shortcuts 1–6 change pages; G regenerates outputs.
- Mobile nav toggle and backdrop open/close the sidebar.

## Exploratory checks
- Custom milestone edits should survive horizon changes unless still on a default template.
- Empty/invalid import payload should not silently corrupt state.
