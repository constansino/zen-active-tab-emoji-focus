# Active Tab Emoji Focus for Zen Browser

Make the current tab obvious at a glance.

This mod adds a centered emoji marker, a stronger border, and glow to the active tab while slightly dimming inactive tabs.

![Preview](https://raw.githubusercontent.com/constansino/zen-active-tab-emoji-focus/master/image.png)

## Features

- Center emoji marker on the active tab.
- Accent color follows each tab's container color (`--identity-icon-color`).
- Stronger active border and glow.
- Subtle dimming for inactive tabs.
- User-customizable options in Zen Mod preferences.

## Preferences

- `mod.active_tab_emoji_focus.active_marker`
  Example: `✨`, `🔥`, `✅`, `🧠`
- `mod.active_tab_emoji_focus.marker_size`
  Number in px, example: `11`, `13`, `16`
- `mod.active_tab_emoji_focus.inactive_opacity`
  Number from `0` to `100`
- `mod.active_tab_emoji_focus.border_width`
  Number in px, example: `2`, `3`

## Manual Install

1. Open your Zen profile folder.
2. Open `chrome/` (create it if missing).
3. Copy content from `chrome.manual.css` into `userChrome.css`.
4. Ensure `toolkit.legacyUserProfileCustomizations.stylesheets=true`.
5. Restart Zen Browser completely.

## Optional: Dynamic Container Labels

If you also want container badges like `01`, `02`, `03` to show on tabs without
hardcoding container IDs, use the files under
`optional/dynamic-container-labels/`.

1. Append `optional/dynamic-container-labels/container-labels.css` to your
   `userChrome.css`.
2. Copy `optional/dynamic-container-labels/autoconfig.cfg` to your Zen install
   root (next to `zen.exe`).
3. Copy `optional/dynamic-container-labels/defaults/pref/autoconfig.js` to
   `defaults/pref/` inside your Zen install directory.
4. Restart Zen Browser completely.

The AutoConfig script writes each tab's live container name into
`data-identity-name`, and the CSS reads that attribute. This keeps the badges in
sync with `containers.json` automatically, even if Firefox / Zen skips internal
container IDs.

## Files for Zen Theme Store Submission

- `chrome.css`
- `preferences.json`
- `README.md`
- `image.png` (`600x400` PNG)

## Optional Local Files

- `optional/dynamic-container-labels/container-labels.css`
- `optional/dynamic-container-labels/autoconfig.cfg`
- `optional/dynamic-container-labels/defaults/pref/autoconfig.js`
