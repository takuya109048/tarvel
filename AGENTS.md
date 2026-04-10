# AGENTS.md

## Purpose
- Maintain and update the travel planning report site in this repository.
- Main deliverable is `travel_report.html`, published through GitHub Pages.

## Current Project Shape
- `travel_report.html`: main report page.
- `index.html`: redirects to `travel_report.html`.
- GitHub Pages is expected to serve from `main` branch root.

## User Preferences Captured
- User wants an HTML report that accumulates planning results.
- Output should be visually readable, not just raw notes.
- Arrival target is important and should be stated with concrete times.
- Lunch timing matters more than fixing one lunch location globally.
- Different stop candidates should be handled as separate plans.
- Route map should show realistic driving routes, not straight-line links.

## Planning Rules
- Treat each sightseeing candidate as an independent plan.
- Keep common constraints separate from plan-specific details.
- Lunch location is variable and should be chosen so lunch starts around 12:00.
- Arrival should target around 14:30 and avoid being too early.
- Add practical buffer before major stopovers when requested.
- Use concise comparisons first, then detailed per-plan timetables.

## Current Plans
- Plan A: Dolphin Farm Shimanami + lunch at Marine Oasis Hakata.
- Plan B: Tatara Shimanami Park + lunch at Tatara Restaurant.
- Plan C: HAKKO Park + lunch at HAKKO Park cafe.
- Plan D: Senkoji Ropeway + lunch at Kodani SA.

## Map Behavior
- Use Leaflet + OpenStreetMap.
- Use OSRM routing for road-following car routes.
- Show all plans on one map with color separation.
- If OSRM fails, fall back to dashed simple paths rather than breaking the page.

## Editing Guidance
- Preserve UTF-8 text; this file set broke when encoding drifted.
- Prefer restructuring whole sections over patching around corrupted text.
- Keep report sections clean:
  - Common conditions
  - Plan comparison
  - Per-plan timetable
  - Route map
  - Photos
  - Sources
- When a plan is removed during refactor, restore it explicitly if still in scope.

## Publishing Workflow
- After report changes:
  1. update `travel_report.html`
  2. check `git status`
  3. commit with a specific message
  4. push to `origin main`
- GitHub Pages URL:
  - `https://takuya109048.github.io/tarvel/`

## Notes
- The repository name is `tarvel` (not `travel`).
- If git complains about dubious ownership on this machine, safe.directory may need to be set again.
