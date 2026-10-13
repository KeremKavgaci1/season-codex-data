# Official sources per game

Where to check for season dates and patch notes. Prefer machine-readable feeds (Steam News API, RSS, JSON). Read official pages like a person would, a few requests per run, and respect robots.txt. Third-party sites (Maxroll, Mobalytics, poe.ninja, wikis) are only for cross-checking and are never copied.

## Path of Exile (id: poe1)

- forum: https://www.pathofexile.com/forum/view-forum/patch-notes
- rss: https://www.pathofexile.com/news/rss
- forum: https://www.pathofexile.com/forum/view-forum/news
- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=238960&count=60&maxlength=100&format=json
- html: https://www.pathofexile.com/developer/docs/changelog
- json api: https://github.com/grindinggear/skilltree-export
- html: https://poedb.tw/us/Version_3.29.0
- season dates: https://www.pathofexile.com/news/rss (official RSS: timelines, release dates, league-end posts, ExileCon posts)
- season dates: https://www.pathofexile.com/forum/view-forum/news (PoE1 Announcements forum in HTML; cross-game posts in the PoE2 forum are missing here)
- season dates: https://www.pathofexile.com/forum/view-thread/3955013 ('Path of Exile 3.29 Expansion Timeline', Jun 8, 2026: GGG Live Jul 16 1 PM PDT, launch Jul 24 1 PM PDT, Mirage end Jul 20 3 PM PDT)
- season dates: https://www.pathofexile.com/forum/view-thread/3982050 ('Path of Exile: Curse of the Allflame Releases on July 24 PDT', Jul 5, 2026)
- season dates: https://api.pathofexile.com/leagues?type=main&realm=pc (legacy no-auth JSON: id, startAt, endAt, registerAt, category.current; also realm=xbox and realm=sony; realm=poe2 is ignored and returns PoE1 da…
- season dates: https://www.pathofexile.com/forum/view-thread/4009902 (ExileCon 2026, Nov 7-8 NZT; keynote 1 PM PST on Nov 6; in the PoE2 'Early Access Announcements' forum)
- season dates: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=238960 (Steam mirror; good for backfilling past league dates)
- season dates: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=2694490 (PoE2 Steam news: 'Path of Exile 2 Fully Releases on December 11!' on Aug 25, 2026, plus PoE2 patch notes)
- season dates: https://timesaver.gg/blog/poe-3-30-release-date-next-league (third-party speculation, Oct 8, 2026: about Nov 13)
- season dates: https://poedb.tw/us/League (third-party league table; 3.30 placeholder 2026-11-14, unconfirmed)

## Path of Exile 2 (id: poe2)

- forum: https://www.pathofexile.com/forum/view-forum/2212
- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=2694490&feeds=steam_community_announcements&count=100&maxlength=0&format=json
- rss: https://store.steampowered.com/feeds/news/app/2694490/
- json api: https://www.poe2wiki.net/w/api.php?action=cargoquery&tables=versions&fields=version,release_date&format=json&limit=20&order_by=release_date%20DESC
- html: https://pathofexile2.com/patchnotes
- other: https://github.com/grindinggear/poe2-skilltree-export
- rss: https://www.pathofexile.com/news/rss
- forum: https://www.pathofexile.com/forum/view-forum/2211
- season dates: Steam News API for app 2694490, which carries official launch-day posts, FAQs, 'Fully Releases on December 11!' and timeline posts: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=2694…
- season dates: poe2wiki Cargo 'events' table, which gives machine-readable league and expansion start and end dates in UTC plus versions (CC BY-NC-SA 3.0): https://www.poe2wiki.net/w/api.php?action=cargoquery&tables…
- season dates: Official PoE2 'Early Access Announcements' forum: https://www.pathofexile.com/forum/view-forum/2211
- season dates: Official GGG API GET /league?realm=poe2 (type=main or type=event). The League object has startAt, endAt, registerAt, event and category.current fields. It needs a confidential OAuth client with scope …
- season dates: poe.ninja public economy endpoint with active league names only and no dates. Per poe.ninja docs, the first entry is the current challenge league: https://poe.ninja/poe2/api/economy/leagues
- season dates: Official ladders page, which shows active league names: https://pathofexile2.com/ladders
- season dates: ggseason.com/poe2/, which is where seasontimer.live/poe2/ now redirects (301). It is a third-party multi-game season tracker. Its current page correctly shows 0.5 ending 2026-12-11 and 1.0 on 2026-12-…
- season dates: GGG livestreams and ExileCon (Nov 7-8 NZT 2026). How far ahead dates are announced varies from about 1 week to about 15 weeks.

## Diablo IV (id: d4)

- json api: https://news.blizzard.com/en-us/api/feed/diablo-4?offset=0
- html: https://news.blizzard.com/en-us/article/24295395/diablo-iv-patch-notes
- html: https://news.blizzard.com/en-us/article/24287406/diablo-iv-patch-notes-3-1
- html: https://news.blizzard.com/en-us/article/24295394/celebrate-30-years-of-diablo-in-season-of-hell-s-legacy
- rss: https://us.forums.blizzard.com/en/d4/groups/blizzard-tracker/posts.rss
- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=2344520&feeds=steam_community_announcements&count=20&format=json
- season dates: Official Blizzard News JSON (https://news.blizzard.com/en-us/api/feed/diablo-4): 'Season Update' and 'Coming Soon' articles give the official start date and usually the time in PT, 3 to 8 days ahead (…
- season dates: PTR articles in the same feed ('PTR' or 'Public Test Realm' category) give 4.5 to 7 weeks of warning that a new season is coming, but no date.
- season dates: Official season page https://diablo4.blizzard.com/en-us/season shows 'Live Now' and the season theme with no start or end dates (verified).
- season dates: Blizzard forum blue tracker RSS https://us.forums.blizzard.com/en/d4/groups/blizzard-tracker/posts.rss for launch-day PSAs (for example 'Season 15 PSA | Login Delay & Issues - September 15, 2026'), wh…
- season dates: Steam announcements (appid 2344520) only as a weak secondary signal: 'Now Live!' posts have been dated days before or after the real launch.
- season dates: Press estimates from the in-game Reliquary countdown: https://blizzardwatch.com/2026/07/17/diablo-4-season-15-start-september-15/ (Blizzard Watch, 2026-07-17) derived 09-15 from the timer and notes th…
- season dates: Third-party end-date estimate: D4 Forge ladder https://d4-forge.com/ladder shows 'Ends Dec 1 (est.)' and '50 days left' for S15. Its ToS bans scraping, so read it manually only.

## Diablo III (id: d3)

- html: https://news.blizzard.com/en-us/feed/diablo-3
- json api: https://news.blizzard.com/en-us/api/news/diablo-3
- forum: https://us.forums.blizzard.com/en/d3/groups/blizzard-tracker/posts.json
- forum: https://us.forums.blizzard.com/en/d3/t/25177.json
- html: https://diablo3.blizzard.com/en-us/
- steam news api: https://store.steampowered.com/api/storesearch/?term=Diablo&cc=us&l=en
- html: https://maxroll.gg/d3
- season dates: https://news.blizzard.com/en-us/article/24301510/season-40-lights-calling-preview (S40 start Oct 2, S39 end Sep 27)
- season dates: https://news.blizzard.com/en-us/article/24287549/season-39-shades-of-the-nephalem-now-live (S39 start June 26; no S38 end date given)
- season dates: https://news.blizzard.com/en-us/article/24262572/season-38-ethereal-memory-has-concluded (S38 start March 27)
- season dates: https://news.blizzard.com/en-us/article/24243442/season-37-the-forbidden-archives-now-live (S37 start Dec 5, 2025)
- season dates: https://news.blizzard.com/en-us/article/24166297 (S34 shifted to Jan 31, 2025; S33 ended Jan 19)
- season dates: https://news.blizzard.com/en-us/api/news/diablo-3 (official JSON feed)
- season dates: https://us.forums.blizzard.com/en/d3/groups/blizzard-tracker/posts.json (staff posts with reliable created_at)
- season dates: https://us.forums.blizzard.com/en/d3/t/67330.json (S39 announcement June 20 for June 26; short-notice complaints)
- season dates: https://us.forums.blizzard.com/en/d3/t/65094.json (S34 delay)
- season dates: https://us.forums.blizzard.com/en/d3/t/64026.json (community theme-rotation wiki)
- season dates: https://maxroll.gg/d3/resources/season-theme (rotation through S39 only; reference, no scraping)
- season dates: https://blizzardwatch.com/2026/07/14/diablo-3-season-40-start/ (third-party; predicted S40 in July, updated Sep 13, 2026)

## Diablo Immortal (id: di)

- json api: https://news.blizzard.com/en-us/api/feed/diablo-immortal?offset=0
- html: https://news.blizzard.com/en-us/feed/diablo-immortal
- html: https://news.blizzard.com/en-us/article/24304159/made-to-suffer-pain-and-anguish-descend-on-lut-gholein
- html: https://news.blizzard.com/en-us/article/24244401/diablo-immortal-bug-fixes-and-patch-notes-for-all-platforms
- forum: https://us.forums.blizzard.com/en/diablo-immortal/t/patch-510-balance-update-sept-17/15425/
- rss: https://us.forums.blizzard.com/en/diablo-immortal/groups/blizzard-tracker/posts.rss
- rss: https://www.reddit.com/r/DiabloImmortal/.rss
- season dates: https://news.blizzard.com/en-us/api/feed/diablo-immortal?offset=0 (bi-weekly and major update articles; these usually include a Battle Pass section with season number, cosmetic set and start time, plu…
- season dates: https://news.blizzard.com/en-us/article/24297201/cross-server-bout-of-realms-returns (Season 56 'Jewel of the Desert' cosmetics 2026-08-27 3:00 a.m. to 2026-09-24 2:59 a.m.; Bout of Realms dates)
- season dates: https://news.blizzard.com/en-us/article/24252016 (Battle Pass Seasons 53-55 cosmetic set 'Delayed Pain', starting June 4 2026)
- season dates: https://news.blizzard.com/en-us/article/24259072 (from Season 50, Battle Pass cosmetics follow a three-season earn/refine/unlock progression)
- season dates: https://news.blizzard.com/en-us/article/24246207/sing-the-ballad-of-the-moon (Season 49 Battle Pass on 2026-02-12 at 3 a.m. server time; Challenge Rift Season 17 dates)
- season dates: https://news.blizzard.com/en-us/article/24295393 (Challenge Rift Season 20, 2026-08-24 to 2026-11-02)
- season dates: https://news.blizzard.com/en-us/article/24304159/made-to-suffer-pain-and-anguish-descend-on-lut-gholein (5.1 maintenance, event and drop-pool end dates; Battleground season length change to 8 weeks)
- season dates: https://news.blizzard.com/en-us/article/24247154/catch-up-on-the-diablo-30th-anniversary-spotlight (official 2026 roadmap)
- season dates: https://us.forums.blizzard.com/en/diablo-immortal/t/2026-bout-of-realms-challenge-of-equals-roadmap/15426/ (official PvP tournament roadmap, posted 2026-09-14 by jadai-11686)
- season dates: https://ggseason.com/diabloimmortal/ (fan tracker: Season 57 start 2026-09-24 10:00 UTC, estimated end 2026-10-22. Its own terms (https://ggseason.com/terms/) forbid republishing 'the season database …
- season dates: https://diablo.fandom.com/api.php?action=parse&page=Battle_Pass_Season_(Diablo_Immortal)&prop=wikitext&format=json (fan wiki history of season numbers, names and dates; the HTML page returns 402 but t…
- season dates: https://www.diablobytes.com/diablo-immortal/2026-roadmap/ (fan roadmap page, 'Updated May 2026'; it is the only source for the 'Andariel Helliquary fight + late-2026 crossover' claim)

## Last Epoch (id: le)

- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=899770&count=20&maxlength=0&format=json
- rss: https://store.steampowered.com/feeds/news/app/899770/
- rss: https://forum.lastepoch.com/c/patch-notes/39.rss
- html: https://lastepoch.com/patchnotes
- rss: https://forum.lastepoch.com/c/news/64.rss
- rss: https://forum.lastepoch.com/c/developer-blogs/38.rss
- html: https://www.lastepochtools.com/news/
- season dates: Official forum News category RSS (Discourse; verified valid RSS): https://forum.lastepoch.com/c/news/64.rss. Carries launch, maintenance (exact downtime times), Twitch Drops, outage and countdown post…
- season dates: Official forum Developer Blogs category (verified, JSON and RSS): https://forum.lastepoch.com/c/developer-blogs/38 and https://forum.lastepoch.com/c/developer-blogs/38.rss. The monthly 'Eterra Monthly…
- season dates: Steam News API (no key needed; verified): https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=899770 and RSS https://store.steampowered.com/feeds/news/app/899770/. Countdown, trailer, Hype…
- season dates: Official site sitemap (static XML; verified): https://lastepoch.com/sitemap.xml. Lists season landing pages (/rage-of-the-frostborn/, /s5rageofthefrostborn/, /shattered-omens/ ...) and patch-note vers…
- season dates: Official season landing page (Nuxt SPA; the HTML shell does include og:title and description): https://lastepoch.com/rage-of-the-frostborn
- season dates: Third-party cross-checks: https://seasondex.com/last-epoch (static HTML, readable; robots.txt disallows only /api/). https://www.arpg-timeline.com/game/last-epoch returned HTTP 429 from a Vercel Secur…

## Torchlight: Infinite (id: tli)

- json api: https://website.xdcdn.net/form/website/torchlight/news.json
- json api: https://website.xdcdn.net/form/website/torchlight/news/en/{id}.json (e.g. https://website.xdcdn.net/form/website/torchlight/news/en/8t9xbvgnO52x.json)
- json api: https://website.xdcdn.net/form/website/torchlight/news/en/dkdc6vpTveGZ.json
- html: https://torchlight.xd.com/ss14pn?lang=en
- rss: https://www.youtube.com/feeds/videos.xml?channel_id=UCQqnkC2MHPZZdRX4dhAAwgQ
- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=1974050&count=30&feeds=steam_community_announcements&format=json
- discord: https://discord.com/invite/torchlight
- html: https://tlidb.com/
- season dates: Official patch-notes microsites state the launch time in the intro: https://torchlight.xd.com/ss14pn?lang=en ('launches globally on October 15 at 7:00 PM PDT') and https://torchlight.xd.com/ss13pn ('l…
- season dates: Official news index JSON (public, CORS *, max-age=120, ETag and Last-Modified): https://website.xdcdn.net/form/website/torchlight/news.json. Locales en, jp, kr, zh-cn and zh-tw are out of sync: zh-tw …
- season dates: Official YouTube channel RSS (machine-readable, gives the earliest signals): https://www.youtube.com/feeds/videos.xml?channel_id=UCQqnkC2MHPZZdRX4dhAAwgQ. It has the season teaser about 3 weeks before…
- season dates: Steam announcements: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=1974050&feeds=steam_community_announcements and RSS at https://steamcommunity.com/games/1974050/rss/. The season po…
- season dates: Official socials, from the site config https://website.xdcdn.net/form/website/common-config/common_227017.json: https://x.com/torchlight_xd, https://discord.com/invite/torchlight, https://www.youtube.…
- season dates: Fan wiki tlidb (says it is 'fan-made and not affiliated with XD'): https://tlidb.com/. It has a season table with GMT+8 start times, a countdown, and patch-note and preview-video links for S1–SS14. It…
- season dates: Press: https://www.invenglobal.com/articles/27019/torchlight-infinite-unveils-ss14-preview (published 2026-10-12; it gives 11:00 on Oct 16, KST) and https://www.pocketgamer.com/torchlight-infinite/ss1…

## Undecember (id: ud)

- html: https://ud.floor.line.games/us/bbs/notice/update_us/1
- html: https://ud.floor.line.games/us/bbs/notice/notice_us/1
- other: https://docs.google.com/spreadsheets/d/e/2PACX-1vSa9MMlvnPacJST8juTzmp2hlM51Dk15E3G9FY2PO-1zKfGVqUUCQ2PSFDJ0l8cPcADaFeUT3t41oRZ/pubhtml
- other: https://docs.google.com/spreadsheets/d/e/2PACX-1vRMhZ-EQIgl7wIKfyfUFyw-Ho90AO7ajstE6iXvSd2Qoo4qRkNdhVjLrcO4dFxY9qZoJsA6FNyqrPSf/pubhtml
- html: https://ud.floor.line.games/kr/bbs/notice/update_kr/1
- html: https://ud.floor.line.games/kr/bbs/notice/Journal_kr/1
- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=1549250&count=20&maxlength=0&format=json
- rss: https://www.youtube.com/feeds/videos.xml?channel_id=UCO1YHH625KZdI66PjAEHDWQ
- html: https://www.line.games/game/UD
- discord: https://discord.com/invite/Q7syAnHfha
- season dates: https://ud.floor.line.games/us/bbs/notice/timetable_us/1 (official Content Schedule board; raid schedules per season back to Season 1 (Apr 27 2023); titles of older posts include date ranges, e.g. 'Se…
- season dates: https://ud.floor.line.games/us/bbs/notice/update_us/1 and https://ud.floor.line.games/kr/bbs/notice/update_kr/1 (season update notices; KR posts first)
- season dates: https://ud.floor.line.games/us/bbs/notice/notice_us/1 (maintenance notices with exact downtime, e.g. /us/bbsCmn/detail/1788867555269005678 for the 9/10 launch; Director's Letters, e.g. vol.24 /us/bbsC…
- season dates: https://ud.floor.line.games/kr/bbs/notice/Journal_kr/1 (Korean Developer Letters: season previews and titles)
- season dates: https://ud.floor.line.games/us/bbs/notice/event_us/1?eventProcessYn=Y and ...?eventProcessYn=N (live and ended events with explicit date ranges: the pre-celebration event's end date = day before the n…
- season dates: https://www.youtube.com/feeds/videos.xml?channel_id=UCO1YHH625KZdI66PjAEHDWQ (official season Update Preview videos, about 6 days ahead)
- season dates: https://www.line.games/game/UD (press release per season, e.g. https://www.line.games/company/news/1362)
- season dates: https://store.steampowered.com/api/appdetails?appids=1549250 (store name carries the season subtitle, currently 'UNDECEMBER: The Farside'; not reliable on its own, since SteamCharts shows '4th Anniver…
- season dates: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=1549250 (Director's Letters and season-end notices historically; no posts since 2026-08-26)
- season dates: https://guide.floor.line.games/UD/en_US/detail/1166867088539300820 (official Ranking guide: rankings stop 7/14 days before a season ends, which gives an in-game end-of-season hint)
- season dates: https://www.arpg-timeline.com/game/undecember (third party; blocked by a Vercel Security Checkpoint (HTTP 429) for scripted requests, so not usable as a backend source)

## Diablo II: Resurrected (id: d2r)

- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=2536520&feeds=steam_community_announcements&count=20&format=json
- json api: https://news.blizzard.com/en-us/api/feed/diablo-2-resurrected?offset=0
- forum: https://us.forums.blizzard.com/en/d2r/groups/blizzard-tracker/posts.rss

## Hero Siege (id: hs)

- steam news api: https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=269210&feeds=steam_community_announcements&count=20&format=json

