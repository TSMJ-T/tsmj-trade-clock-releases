# tsmj-trade-clock-releases

Public version/release info for **TSMJ Trade Clock** (a desktop analog clock
app for traders). This repository intentionally contains no business or
trading-strategy content — only `version.json` and release notes, used by
the app's own built-in "最新版を確認" (check for updates) feature.

## `version.json`

```json
{
  "version": "1.0.0",
  "url": "https://github.com/TSMJ-T/tsmj-trade-clock-releases/releases/latest"
}
```

The app fetches this file at startup (and on manual request from its
right-click menu) and compares `version` against its own build. If newer,
it shows a one-time dialog with the option to open `url`. No auto-download,
no silent install.

To publish a new version: bump `version` here to match the new build, and
publish the built `.exe` under this repo's Releases page (so the `url`
above always resolves to the newest one).

## `calendar-links.html`

A static page listing well-known economic calendar sites (Forex Factory,
Investing.com, Dukascopy Japan, etc.) - the app links out here instead of
pulling in any calendar data itself, so no third-party data-licensing
question applies (a plain outbound link needs no permission). Linked from
the app's own right-click menu. Editing this file and pushing to `main`
updates what every installed copy of the app shows next time someone opens
that menu item - no app rebuild/redistribution needed.

Served via GitHub Pages once enabled for this repo (Settings → Pages →
Deploy from a branch → `main` / root) at:
`https://tsmj-t.github.io/tsmj-trade-clock-releases/calendar-links.html`
