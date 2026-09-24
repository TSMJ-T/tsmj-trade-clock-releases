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
