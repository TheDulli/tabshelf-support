# TabShelf User Manual

TabShelf replaces the browser new-tab page with a workspace for saving, organizing, and reopening tabs as named spaces.

## Quick Start

1. Open a new tab to see TabShelf.
2. Use `Capture Tabs` to prepare a new space from the current window's open tabs.
3. Name the space in the placeholder and choose `Create`.
4. Drag rows from `Active Tabs` into any space to save individual tabs.
5. Click a saved bookmark card to open it in the current tab.

## Spaces

Spaces are named groups of saved links.

- `New Space` scrolls to the placeholder so you can create an empty space.
- The extension popup `Create empty space` action prompts for a name and creates an empty space from the browser toolbar.
- The extension popup `Open last used space` action reopens the most recent space created or captured from the popup.
- The extension popup `Recent spaces` list shows up to three recent popup spaces so you can reopen a specific one.
- `Filter spaces` narrows the current visible space list by space name or saved-link text. Clear the filter to show every space again.
- Drag the space header to reorder spaces.
- Use the fold button on the left side of a space header to fold or unfold that space.
- `Fold All` folds or unfolds every visible space; while filtering, hidden spaces are left unchanged.
- Space header actions include the pin icon to pin or unpin the space, open all saved bookmarks, open the space in a new window, rename the space, or delete it.
- Pinned spaces stay grouped at the top of the space list. Unpinning a space moves it to the top of normal spaces.
- Deleting a space removes that TabShelf space from the local browser bookmark folder.

## Capture Tabs

`Capture Tabs` is the intentional save flow for the current browser window.

1. Open the tabs you want to keep.
2. Choose `Capture Tabs`.
3. Enter a space name in the placeholder.
4. Choose `Create`.

Only normal `http` and `https` URLs are saved. Browser-internal pages such as `chrome://` pages are skipped.

## Active Tabs

The `Active Tabs` panel shows the normal tabs in the current browser window.

- Drag a tab from `Active Tabs` into a space to save it.
- Saved indicators show when an active tab already exists in one or more spaces.
- The details button on a saved active tab shows which spaces contain that URL.
- The toolbar Active Tabs control hides or shows the panel and remembers your preference.

## Saved Bookmarks

Saved bookmarks appear as cards inside spaces.

- Right-click inside a page, open the TabShelf menu, and choose a space to save that page directly.
- Click a card to open the link.
- Hover a card to preview its URL. Long URLs are visually shortened in the tooltip, but the stored URL is not changed.
- Use the card menu to rename the bookmark, edit its URL, copy it to another space, or switch between the website favicon and the TabShelf icon.
- Drag a saved bookmark to another space to move it. Hold Ctrl on Windows/Linux or Option on macOS while dragging to copy it instead.
- Use the delete button on a card to remove that saved bookmark after confirmation.
- Saved and edited URLs must be normal `http` or `https` URLs. If a context-menu save points to a URL already in the target space, TabShelf leaves the existing bookmark unchanged.

## Dynamic Save

Dynamic Save is an optional recovery safety net. It is off by default and does not replace `Capture Tabs`.

When Dynamic Save is on, TabShelf keeps a bounded local history of recent recovery snapshots for normal `http` and `https` tabs across normal browser windows. Snapshots are stored in local extension storage, not bookmarks.

Dynamic Save can:

- keep recent recovery snapshots
- restore the latest snapshot into new browser windows
- restore a selected older snapshot
- save the latest snapshot as a named normal space
- save a selected snapshot as a named normal space
- clear the latest snapshot
- clear all Dynamic Save history

Dynamic Save does not automatically create spaces. A snapshot becomes a normal bookmark-backed space only when you explicitly choose `Save as Space` or `Save Selected` and provide a space name.

### Recovery History

TabShelf keeps up to 10 recent Dynamic Save snapshots, removes snapshots older than 7 days, skips adjacent duplicate states, and keeps Dynamic Save storage bounded.

### Safety Checkpoints

Dynamic Save uses a browser alarm only while Dynamic Save is enabled. The checkpoint verifies the recovery state at the selected interval and skips unchanged snapshots.

Available checkpoint intervals are `5 min`, `15 min`, and `30 min`.

TabShelf also refreshes the latest recovery snapshot when TabShelf loads or becomes active, so newly opened normal windows are included without turning Dynamic Save on again in each window.

## Import and Export

Use `Settings` -> `Library` to export or import spaces as JSON.

- `Export Spaces` downloads a JSON backup of your current spaces.
- `Import Spaces` lets you choose a JSON file to restore.
- Shelf pinned/unpinned state is included in exports and restored on import.
- Invalid or duplicate URLs are reported before import so you can choose whether to continue and skip them.

Export before destructive maintenance actions if you want a backup.

## Settings

Open `Settings` from the toolbar to adjust TabShelf behavior.

The compact Settings menu is focused on quick preferences:

- `Theme`: choose `Dark`, `Light`, or `Auto`.
- `Density`: choose `Compact`, `Dense`, or `Tight`.
- `External Favicons`: allow or block Google favicon fallback for website icons.
- `Smart Names`: clean noisy saved bookmark names and show source domains.
- `Library`: open bookmark root, backup, and maintenance controls.
- `Recovery`: open Dynamic Save enablement, checkpoint interval, snapshot status, restore, Save as Space, and clear controls.
- `Rate TabShelf`: open the appropriate browser store review page.

Use `Library` for `Bookmark Root`, `Export Spaces`, `Import Spaces`, and `Delete All Spaces`. `Delete All Spaces` removes all TabShelf spaces after backup-aware confirmation.

## Privacy and Data Storage

TabShelf is local-first.

- Spaces and saved links are stored in your local browser bookmarks under a `TabShelf` folder.
- Preferences and UI state, including failed external favicon hosts, are stored in local extension storage.
- Dynamic Save snapshots are stored locally in extension storage only when Dynamic Save is enabled.
- Dynamic Save checkpoints use the browser `alarms` permission only for local scheduling while Dynamic Save is enabled.
- Browser page right-click save actions use the `contextMenus` permission only to add TabShelf entries to that browser menu.
- TabShelf does not transmit your shelf or bookmark data to a remote server.
- External favicon fallback may request favicon images from Google's favicon service when enabled. Hosts that fail to load are remembered locally so TabShelf can use the bundled TabShelf icon for that site next time. If the favicon service returns a generic placeholder as a successful image, that placeholder may still appear.

To remove TabShelf data, delete the `TabShelf` bookmarks folder and uninstall the extension.

## Troubleshooting

### A tab did not save

Only `http` and `https` tabs are saved. Browser pages, extension pages, blank tabs, and other internal URLs are skipped.

### A saved bookmark name looks different from the page title

`Smart Names` is on by default. It cleans common noisy suffixes from newly saved bookmark names. Turn `Smart Names` off in Settings if you want future saves to keep raw page titles.

### I cannot find my spaces in bookmarks

Check the `Bookmark Root` setting. TabShelf can store spaces under `Bookmarks Bar` or `Other Bookmarks`.

### I want to back up my spaces

Use `Settings` -> `Export Spaces` and keep the downloaded JSON file.

### Dynamic Save did not create a space

That is expected. Dynamic Save is a recovery history. Use `Save as Space` or `Save Selected` to intentionally convert a snapshot into a normal space.

## Support

Use the GitHub Issues page for bug reports, feature requests, and support questions:

https://github.com/TheDulli/tabshelf-support/issues

