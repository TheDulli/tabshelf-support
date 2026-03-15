# Changelog
 
## [1.2.1] - 2026-03-15

### Changed
- Popup `Open TabShelf` action now opens the extension's own TabShelf page in a browser-neutral way across supported browsers.

### Fixed
- Active Tabs hidden-count messaging no longer counts browser new-tab pages as hidden non-`http`/`https` tabs.

## [1.2.0] - 2026-03-11
### First public production release

### Added
- Capture open tabs into named spaces for later revisit.
- Create, rename, delete, fold, and reorder spaces.
- Drag saved tabs between spaces.
- Active Tabs panel with drag-to-space support and saved-state highlighting.
- Open all saved tabs in a space with one click.
- Import and export spaces as JSON.
- Settings for root location, favicon behavior, and theme.
- Theme modes: `Dark`, `Light`, `Auto` in both new tab and popup.
- Extension popup with quick capture actions.
- One-click bookmark delete action (with confirmation).

### Changed
- New-tab and popup UI now follow saved theme preference; `Auto` follows system theme.
- Default theme for new users is now `Auto`.
- Top toolbar controls use clearer icon + text labels.
- Active Tabs visibility toggle is remembered between sessions.
- Improved overall layout and toolbar usability.

### Fixed
- Theme toggle now correctly cycles through `Dark`, `Light`, and `Auto`.
- Inline bookmark rename now allows normal mouse text selection without accidental drag.
- Fold/Unfold icon alignment issues corrected.
- Multiple interaction and persistence reliability fixes for drag/drop, ordering, and editing behavior.
- Keyboard accessibility improvements across new tab and popup.
