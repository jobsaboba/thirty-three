# 33% — Top Trainers

Every horse whose trainer is on **horseracing.net's Hot Trainers table**
(https://www.horseracing.net/stats) with a **33%+ strike rate** — the site's
own rule: "best strike rate from at least 2 wins in the last 14 days".
Listed race by race: race, selection, trainer, and the stats that earned
the pick.

- The site's hot-trainers table is fetched at publish time and snapshotted
  per day (`racing-scripts/cache/horseracing_net/{date}.json`), so each
  day's list is exactly what the site showed that morning.
- Cards come from horseracing.net's own racecards — every race, any size
  (7-runner evening races included), trainers spelled exactly as the hot
  list spells them — also snapshotted per day. Race day files record
  `card_source` (site cards or the family's settled sheets).
- Fallback matching (sheet days) handles the sheets' initials and titles
  ("Nicky Richards" ↔ "N G Richards", "Sandy Thomson" ↔ "A M Thomson",
  "Ann Hamilton" ↔ "Mrs A Hamilton"), with first-initial disambiguation
  so Emmet Mullins never picks Willie Mullins' horses.
- Days before the snapshot record began (and fetch failures) fall back to
  the same rule computed from the family's settled 8+-runner sheets —
  labelled "computed from results" in the app.
- Refreshed every morning (~05:55) with the day's card, and again every
  30 min through the afternoon (13:00–22:00) as results land.
- The whole season since 1 Jan is backfilled; swipe the day strip.

Installable PWA — blue on black, like the rest of the family.
