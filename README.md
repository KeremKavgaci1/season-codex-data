# Season Codex data

The data the Season Codex app shows: season dates and patch-note summaries for
seasonal ARPGs. The app downloads these files, so updating them here updates every
installed app within a few hours, without a new app release.

## Layout

```
data/
  games.json            all games, current season, next season (date + status)
  patches/<game-id>.json latest patch summary for one game
```

`games.json` has an `updated_at` timestamp (ISO 8601, UTC). The app only switches
to a newer copy when `updated_at` is later than the one it already has, so
**bump `updated_at` on every change**.

Season status is one of `confirmed` (officially announced date), `estimated`
(our projection; give a short `estimate_note`) or `tba` (no date yet).

Patch summaries are written in our own words from the official notes and always
link the official source in `source_url`. Do not paste official text.

## How the app finds this repository

In the app project, `gradle.properties` holds:

```
seasoncodex.dataUrl=https://raw.githubusercontent.com/<user>/season-codex-data/main/data/
```

Leave it empty to build an app that only uses the data bundled in the APK.
