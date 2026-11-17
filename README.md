# 33% — Top Trainers

Every horse whose trainer is on **horseracing.net's Hot Trainers table**
(https://www.horseracing.net/stats) with a **33%+ strike rate** — the site's
own rule: "best strike rate from at least 2 wins in the last 14 days".
Listed race by race: race, selection, trainer, and the stats that earned
the pick.

- The site's table is fetched at publish time and snapshotted per day
  (`racing-scripts/cache/horseracing_net/{date}.json`), so each day's list
  is exactly what the site showed that morning.
- Site trainer names are matched onto the day's cards ("Nicky Richards" ↔
  "N G Richards") by surname, with first-initial disambiguation so
  Emmet Mullins never picks Willie Mullins' horses.
- Days before the snapshot record began (and fetch failures) fall back to
  the same rule computed from the family's settled 8+-runner sheets —
  labelled "computed from results" in the app.
- Refreshed every morning (~05:55) with the day's card, and again every
  30 min through the afternoon (13:00–22:00) as results land.
- The whole season since 1 Jan is backfilled; swipe the day strip.

Installable PWA — blue on black, like the rest of the family.
