# How to update this data

This repository feeds the Season Codex app. Installed apps download `data/` every
few hours, so every change here reaches users. Accuracy matters more than speed:
**if you are not sure, leave the data as it is.**

## Each run

1. Read `data/games.json`, every `data/patches/*.json` and `SOURCES.md`.
2. For each game, check its official sources in `SOURCES.md` for anything newer
   than what the data says:
   - **Next season date.** `tba` or `estimated` becomes `confirmed` only when the
     developer officially announced the date and time. A confirmed date that the
     developer moved gets the new date.
   - **Season rollover.** When the next season has started, it becomes `current`
     (keep its official name, version, start time and source), and `next` becomes the
     season after it: `tba`, or `estimated` with a one-sentence `estimate_note`.
   - **New major patch notes.** When the developer publishes the notes for a new
     season or a new major update, replace `data/patches/<id>.json` with a fresh
     summary of those notes (rules below). Small hotfixes do not replace a summary.
3. If and only if something changed:
   - set `updated_at` in `data/games.json` to the current time in UTC
     (ISO 8601, e.g. `2026-10-14T06:00:00Z`) - the app ignores data whose
     `updated_at` did not move forward;
   - check that every JSON file still parses (for example
     `python3 -m json.tool data/games.json > /dev/null`);
   - commit with a message listing what changed per game, and push to `main`.
4. If nothing changed, do not commit anything.

## Rules for dates

- All times are UTC in ISO 8601 (`2026-10-16T02:00:00Z`). Convert carefully from
  PDT/PST, CDT, GMT+8, KST and so on; watch daylight saving changes.
- `confirmed` needs an official announcement with a date. Otherwise use `estimated`
  (with `starts_at` and a short `estimate_note` explaining the basis) or `tba`.
- `source_url` points at the official announcement.

## Rules for patch summaries

- Write everything in your own words. Never copy sentences from the notes; no quote
  longer than about ten words. Always set `source_url` to the official notes.
- `tldr`: 2-4 plain sentences. `highlights`: 3-5 one-line headline changes.
- `changes`: the 15-35 most important items. Each has `tag` (`new` for new mechanics,
  content, classes, skills or items; `buff`; `nerf`; `qol` for convenience and UI;
  `change` for reworks that are neither clearly a buff nor a nerf), a short `area`
  (class, skill, system) and one `text` sentence with the key numbers exact.
- Skip routine bug fixes unless they matter for gameplay.
- `read_minutes`: about 2-3. `game_id` must match the file name.

## File shapes

`data/games.json`

```json
{
  "updated_at": "2026-10-12T00:00:00Z",
  "games": [
    {
      "id": "tli",
      "name": "Torchlight: Infinite",
      "developer": "XD Inc.",
      "platforms": ["PC", "Android", "iOS"],
      "season_term": "Season",
      "current": { "name": "Afterlight", "version": "SS13", "started_at": "2026-07-17T02:00:00Z", "source_url": "https://..." },
      "next": { "name": "Tartarus", "version": "SS14", "starts_at": "2026-10-16T02:00:00Z", "status": "confirmed", "source_url": "https://..." }
    }
  ]
}
```

`data/patches/<id>.json`

```json
{
  "game_id": "tli",
  "title": "SS14 \"Tartarus\" Season Update Log",
  "version": "SS14",
  "published_at": "2026-10-09",
  "source_url": "https://...",
  "source_name": "Official site",
  "tldr": "...",
  "highlights": ["..."],
  "changes": [{ "tag": "nerf", "area": "Hero traits", "text": "..." }],
  "read_minutes": 3,
  "summarized_at": "2026-10-12"
}
```

Game ids in use: poe1, poe2, d4, d3, di, d2r, le, tli, ud, hs. Do not rename or
remove ids; the app's artwork is keyed by them.
