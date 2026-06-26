# Agent Guidance

## Project Shape
- This workspace is a single-file static web app: [islamabad-explorer.html](islamabad-explorer.html).
- Keep changes focused in that file unless the user explicitly asks to split code or add supporting assets.
- There is no visible build, test, or package manager setup in the workspace snapshot.

## What To Preserve
- The HTML file contains all structure, styling, data, and behavior in one place.
- DOM ids and classes are tightly coupled to the script. Preserve the existing ids for map, filters, route controls, theme toggle, toast container, and viewpoint cards unless you update every call site together.
- Viewpoints are linked by unique `id` across the map markers, dropdowns, cards, and routing logic. Keep those ids stable and unique.
- The route feature is based on an in-memory graph and straight-line distances, not road network routing. Do not treat it like a driving-directions engine unless you also replace the data source and algorithm.

## Environment Notes
- External dependencies are loaded from CDNs, including Leaflet, Font Awesome, and Google Fonts.
- The page expects to run from a local web server or localhost for geolocation and other browser APIs; `file://` is fragile.
- Theme state is stored in `localStorage` under `islamabad-theme`.

## Editing Guidance
- Prefer minimal, mechanical edits over broad refactors.
- If you rename or restructure UI elements, update the corresponding JavaScript selectors in the same change.
- Preserve the existing visual style and the academic project branding in the footer unless the user asks otherwise.

## Quick Verification
- Open the page and confirm the map loads, section switching works, the filter chips update cards, theme toggle persists, and route calculation still succeeds.
- There is no automated test suite in the workspace snapshot, so manual browser verification is the normal check.
