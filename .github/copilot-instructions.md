# Copilot Instructions for AI Coding Agents

## Project Overview
This is a simple web application with a minimal structure. The main files are:
- `index.html`: The entry point and main UI for the app.
- `manifest.json`: PWA manifest for app metadata and icons.
- `sw.js`: Service worker for offline support and caching.
- `icon-192.png`, `icon-512.png`: App icons for PWA usage.

## Architecture & Data Flow
- The app is a static site, likely a Progressive Web App (PWA).
- All logic is contained in the HTML and service worker files. There is no backend or build system.
- The service worker (`sw.js`) handles caching and offline functionality. It communicates with the browser via standard PWA APIs.
- The manifest (`manifest.json`) defines app metadata, icons, and display behavior for installation.

## Developer Workflows
- **No build step required**: All files are static and can be served directly.
- **Testing**: Manual testing is done by opening `index.html` in a browser. For service worker changes, use browser dev tools to unregister/reload the worker.
- **Debugging**: Use browser dev tools (Console, Application tab for service workers, Manifest, and Cache Storage).
- **Deployment**: Upload all files to a static hosting provider (e.g., GitHub Pages, Netlify, Vercel).

## Project-Specific Conventions
- All logic is in vanilla HTML/JS; no frameworks or external dependencies are present.
- Service worker registration and caching logic should be kept simple and readable.
- Manifest and icons must be updated together if branding changes.
- No custom build scripts, linters, or test runners are present.

## Integration Points
- The app integrates with browser PWA APIs only. No external APIs or libraries are used.
- All cross-component communication is via standard browser events (e.g., service worker messages).

## Examples & Patterns
- To update offline behavior, edit `sw.js` and test in the browser.
- To change app metadata or icons, update `manifest.json` and the PNG files.
- To add new features, modify `index.html` and ensure service worker logic supports them if needed.

## Key Files
- `index.html`: Main UI and entry point.
- `sw.js`: Service worker logic.
- `manifest.json`: PWA metadata.
- `icon-192.png`, `icon-512.png`: App icons.

---
For questions or unclear conventions, review the above files for examples. If a new pattern is needed, document it here for future agents.
