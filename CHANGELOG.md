# Changelog

All notable user-facing changes to TabShelf will be documented in this file.

## [Unreleased]
### User-facing

- No unreleased user-facing changes.


## [1.6.0] - 2026-05-14
### User-facing

- Replaced the shelf pin button emoji with a theme-aware monochrome icon that matches the rest of the space header actions.
- Added shelf pinning so favorite spaces stay at the top and keep their pinned state through export and import.
- Added a subtle local date/time line to the TabShelf header using the browser's regional formatting.
- Improved Dynamic Save so enabled recovery snapshots refresh across all normal browser windows when TabShelf loads, regains focus, or sees Dynamic Save enabled from another TabShelf page.
- Added a local space filter in the toolbar so users can quickly narrow the current space list and clear back to the full view.
- Polished the TabShelf header branding, accent treatment, and saved-space focus states while keeping the new-tab UI quiet and functional.
- Improved keyboard accessibility with skip-link navigation, stronger focus states, settings-panel focus return, and reduced-motion behavior.
- Split the new-tab Settings menu into compact Preferences plus dedicated Library and Recovery surfaces for data controls and Dynamic Save actions.
- Refined Active Tabs and shelf header hierarchy with clearer metadata, drag handles, and responsive stacking for narrow layouts.
- Refreshed the TabShelf new-tab and popup surfaces with calmer spacing, clearer button states, stronger focus styling, and more intentional empty states.
- Reduced saved-card action button visual weight so delete and item-menu controls stay quieter until hover or keyboard focus.
- Polished the extension popup with clearer primary and secondary action hierarchy, quieter surfaces, and a compact Theme footer.
- Improved Tight density saved-card action sizing so the item menu remains readable.


## [1.5.0] - 2026-05-04
### User-facing

- Added a `Full Help` action to the existing Quick Tips panel so users can open the bundled local help page from TabShelf.
- Added a `Help` action to the extension popup so users can open bundled local help from the browser toolbar.
- Added bundled local `help.html` guidance so TabShelf can provide task-focused help without network access.
- Added `USER_MANUAL.md` as the canonical user-facing manual for TabShelf workflows, settings, Dynamic Save, privacy, and troubleshooting.
- Improved saved bookmark URL tooltips so short URLs size naturally while very long URLs stay on-screen and visually constrained with ellipsis.
- Added explicit Dynamic Save snapshot conversion so users can save the latest or selected recovery snapshot as a named normal space.
- Added configurable Dynamic Save safety checkpoints that periodically verify recovery history is current while Dynamic Save is enabled.
- Added bounded Dynamic Save snapshot history with selected-snapshot restore and clear-history controls.
- Added a Dynamic Save restore action so users can explicitly reopen the latest valid recovery snapshot without changing saved spaces.
- Added an opt-in Dynamic Save setting that keeps one latest local recovery snapshot of normal HTTP/HTTPS tabs without changing manual Capture Tabs behavior.
- Added a Settings action to rate TabShelf in the appropriate browser store, using Chrome Web Store for Chrome-like browsers and Microsoft Edge Add-ons for Edge.
- Added a Settings maintenance action to delete all TabShelf spaces after a clear backup-aware confirmation.


## [1.4.0] - 2026-04-15
### User-facing

#### Added

- Hovering a saved bookmark card now shows the bookmark URL as a visible TabShelf tooltip for quicker link inspection.
- Hovering an Active Tabs row now shows the tab URL in a scroll-aware tooltip anchored inside the panel.
- Each space header now has a one-click action to open all saved bookmarks in a separate browser window.
- Saved bookmark names now clean common noisy page-title suffixes on save and show compact domain metadata on cards, without overwriting existing custom names.
- Settings now includes a Smart Names preference, enabled by default, for turning automatic bookmark-name cleanup and domain metadata on or off.


## [1.3.0] - 2026-03-30
### User-facing

#### Added

- Bookmark density options in the new-tab Settings menu, with `Compact` as the default plus denser `Dense` and `Tight` card layouts.
- Per-bookmark favicon mode toggles in the saved-item menu so any bookmark can switch between the website favicon and the default TabShelf icon.

#### Changed

- Saved bookmark cards now use a more compact default layout so more items fit in each shelf row before switching to denser modes.
- The new-tab Settings panel now shows each Theme, Density, Root, and favicon option directly instead of cycling through hidden values one click at a time.
- The TabShelf logo and name in the toolbar now read as static branding instead of a clickable button-like control.
- Shelf headers now keep fold/unfold on the title and use a separate grip-style drag handle so reorder is easier to understand.
- Active Tabs saved-link pills now include an explicit details button that reveals the matching space names without opening the panel while users scan or drag the list.
- Active Tabs saved-link details now stay anchored directly above or below the selected row and remain open until explicit dismissal, so they do not disappear while users read the saved-space list.

#### Fixed

- The Active Tabs saved-details popover now uses a readable light-theme surface and text treatment instead of reusing the dark-theme panel colors.
- The floating help button now centers its `?` glyph correctly inside the circular control for consistent tip icon alignment.
- Switching a bookmark's favicon mode now updates the clicked card in place instead of visibly refreshing the whole shelf view.


## [1.2.2] - 2026-03-17
### User-facing

#### Fixed

- Light theme inline text fields now use accessible light-surface backgrounds, borders, and placeholder contrast so typed text remains readable while renaming items or creating spaces.
- Root `TabShelf` bookmark folder creation is now coordinated to avoid duplicate root folders on first install.
- Shelf collapsed state no longer creates visible `tabshelf://meta?...` bookmarks; legacy meta bookmarks are migrated and removed when TabShelf loads.
- Bookmark-root resolution now works on machines where browser bookmark parent IDs differ from the original `1`/`2` assumptions, reducing profile-specific shelf-creation failures on affected installs.
- Blank bookmark parent IDs now fall back to the default top-level root instead of failing with `Can't find bookmark for id`, improving recovery when bookmark profile state is inconsistent.
- Notes for investigation: one reported non-working install was ultimately resolved by rebuilding Chrome's bookmark data, indicating a profile/bookmark-store corruption case in addition to the app-side hardening above.


## [1.2.1] - 2026-03-15
### User-facing

#### Changed

- Popup "Open TabShelf" action now opens the extension's own TabShelf page in a browser-neutral way across supported browsers.

#### Fixed

- Active Tabs hidden-count messaging no longer counts browser new-tab pages as hidden non-http/https tabs.


## [1.2.0] - 2026-03-11
### User-facing

#### Added

- Theme preference setting with `Dark`, `Light`, and `Auto` options in both new-tab Settings and extension popup.

#### Changed

- New-tab and popup styles now adapt to the saved theme preference, with `Auto` following system color scheme.
- Theme preference default is now `Auto` for first-time users.
- Top toolbar controls now use icon + text treatment for Active Tabs visibility, Fold/Unfold, and Settings.

#### Fixed

- Inline bookmark name editing now allows mouse text selection while preventing accidental bookmark drag.
- Theme preference toggle now correctly cycles between `Dark`, `Light`, and `Auto` (was incorrectly stuck on `Auto`).
- Unfold icon alignment now matches Fold icon baseline in the top toolbar.

