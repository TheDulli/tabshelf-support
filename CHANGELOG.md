# Changelog

## [1.4.0] - 2026-04-15

### Added
- Bookmark cards now show the saved URL in a TabShelf tooltip when hovered, making links easier to inspect before opening.
- Active Tabs rows now show the tab URL in a tooltip while you hover them.
- Each space header now includes a one-click action to open all saved bookmarks from that space in a separate browser window.
- New saved bookmarks can use cleaner names by removing common noisy page-title suffixes, while still keeping existing custom names intact.
- Bookmark cards can now show compact domain metadata for faster scanning.
- Settings now includes a Smart Names preference, enabled by default, for automatic bookmark-name cleanup and domain metadata.

## [1.3.0] - 2026-03-30

### Added
- Bookmark density options in the new-tab Settings menu, with `Compact` as the default plus denser `Dense` and `Tight` card layouts.
- Per-bookmark favicon mode toggles in the saved-item menu so any bookmark can switch between the website favicon and the default TabShelf icon.

### Changed
- Saved bookmark cards now use a more compact default layout so more items fit in each shelf row before switching to denser modes.
- The new-tab Settings panel now shows each Theme, Density, Root, and favicon option directly instead of cycling through hidden values one click at a time.
- The TabShelf logo and name in the toolbar now read as static branding instead of a clickable button-like control.
- Shelf headers now keep fold/unfold on the title and use a separate grip-style drag handle so reorder is easier to understand.
- Active Tabs saved-link pills now include an explicit details button that reveals the matching space names without opening the panel while users scan or drag the list.
- Active Tabs saved-link details now stay anchored directly above or below the selected row and remain open until explicit dismissal, so they do not disappear while users read the saved-space list.

### Fixed
- The Active Tabs saved-details popover now uses a readable light-theme surface and text treatment instead of reusing the dark-theme panel colors.
- The floating help button now centers its `?` glyph correctly inside the circular control for consistent tip icon alignment.
- Switching a bookmark's favicon mode now updates the clicked card in place instead of visibly refreshing the whole shelf view.

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
