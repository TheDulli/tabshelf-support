# Privacy Policy

Last updated: 2026-06-06

TabShelf is a local-first browser extension.

## What data TabShelf uses

- Open tab metadata (title, URL, favicon URL) when you choose capture/save actions, including TabShelf browser context menu save actions.
- Open tab metadata (title and URL) for local Dynamic Save recovery snapshots only when you enable Dynamic Save.
- Bookmarks created under a local `TabShelf` bookmarks folder.
- Local extension preferences and UI state, such as theme, root-location preference, Active Tabs visibility, shelf fold state, shelf pin state, popup recent-space metadata, and failed external favicon hosts.
- Optional import/export JSON files that you explicitly choose.

## How data is stored

- Shelf/link data is stored locally in your browser bookmarks.
- Preferences and UI state, including shelf pin state, failed external favicon hosts, and the `popupRecentShelfIds` recent-space list, are stored locally in extension storage.
- Dynamic Save stores a bounded local history of recent recovery snapshots in extension storage when enabled.
- Dynamic Save uses a browser alarm only to schedule local safety checkpoints while Dynamic Save is enabled.
- TabShelf uses the `contextMenus` permission only to add save actions to browser page right-click menus.
- Legacy local storage shelf data may be migrated once into bookmarks.

## Data sharing

- TabShelf does not transmit your shelf/bookmark data to a remote server.
- TabShelf does not sell personal information.

## Third-party requests

- Favicon images may be requested from Google favicon service to render bookmark icons in the UI while the browser is online. Hosts whose external favicon image fails to load are remembered locally so TabShelf can use the bundled icon next time. If the favicon service returns a generic placeholder as a successful image, that placeholder may still appear.

## Your control

- You can delete shelves at any time from the extension.
- You can restore the latest or a selected recent Dynamic Save snapshot, clear the latest snapshot, or clear all Dynamic Save history from Settings.
- You can explicitly save a Dynamic Save snapshot as a normal space; that space is then stored in your local browser bookmarks like other TabShelf spaces.
- You can remove all extension data by deleting the `TabShelf` bookmarks folder and uninstalling the extension.

## Contact

For repository issues, use the GitHub Issues page for this project.

