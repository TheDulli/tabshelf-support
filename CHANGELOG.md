# Changelog

## [1.2.2] - 2026-03-17

### Fixed
- Light theme inline text fields now use accessible light-surface backgrounds, borders, and placeholder contrast so typed text remains readable while renaming items or creating spaces.
- Root `TabShelf` bookmark folder creation is now coordinated to avoid duplicate root folders on first install.
- Shelf collapsed state no longer creates visible `tabshelf://meta?...` bookmarks; legacy meta bookmarks are migrated and removed when TabShelf loads.
- Bookmark-root resolution now works on machines where browser bookmark parent IDs differ from the original `1`/`2` assumptions, reducing profile-specific shelf-creation failures on affected installs.
- Blank bookmark parent IDs now fall back to the default top-level root instead of failing with `Can't find bookmark for id`, improving recovery when bookmark profile state is inconsistent.

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
