# EVERYTHING ENGINE

A local-first, installable PWA for building small apps from reusable components, data tables, and configurable workflows.

## Run locally

Because service workers require a secure context, use a local web server instead of opening `index.html` directly.

### Python
```bash
python -m http.server 8000
```
Open `http://localhost:8000`.

Or publish the folder to GitHub Pages / any static HTTPS host.

## Included features

- Visual app canvas with reusable blocks and inspector settings
- Desktop/mobile canvas preview
- App library: create, rename, duplicate, open, and delete projects
- Starter templates
- Local persistence with automatic save
- Undo and redo for canvas changes
- Data Studio with custom tables, fields, editable records, and CSV export
- Workflow editor with triggers, conditions, and supported actions
- Theme workshop with live accent/background/radius controls
- Portable JSON project import/export
- Workspace backup and restore
- Standalone HTML export for supported components
- Responsive layout and offline shell caching
- No external runtime dependencies

## Data and backend readiness

The current build stores workspace state in browser `localStorage`. Projects use versioned, JSON-serializable structures that can later be mapped to an API or database. No cloud server, authentication, remote sync, or shared collaboration is configured. Export a workspace backup regularly if the data matters.

## Standalone export limitations

The standalone HTML export contains the selected app's current layout and supported basic interactions. Workflows and workspace data tables are exported as descriptive metadata, not as a complete cloud-connected runtime. External API calls and server-dependent features are not embedded.

## Offline behavior

The service worker caches the app shell after the first successful visit on a supported secure origin. Google Fonts are an optional visual enhancement; the app uses local fallback fonts if unavailable.
