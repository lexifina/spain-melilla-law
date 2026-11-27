<!-- lawwatch: written from data/checks by the check trail; edit the records, not this page -->

# Monitoring: what is read and what came of it

[Español](README.md)

How global-law monitors every country: [global-law monitoring/](https://github.com/lexifina/global-law/tree/main/monitoring). This page is the same for Melilla only: every time an official source is read, when, and what came of it (acts added, changed and removed). The machine-readable form is [data/checks/](../data/checks/) (JSON Lines, schema `lexifina-check/1`), in `git log` as `Kind: check` commits, and month by month in [checks/](checks/).

**Last check:** 2026-11-27 06:31 UTC, BOE consolidated legislation, autonomous communities (open data): 13 addresses read; 0 added, 0 changed, 0 removed; no change; 0 not published, 0 of them with no reason.

## Sources

| Source | Folders | How often | Last successful check | Last result | State |
| --- | --- | --- | --- | --- | --- |
| [BOE consolidated legislation, autonomous communities (open data)](https://www.boe.es/datosabiertos/api/api.php) | `estatuto-de-autonomia/`, `ley-*/`, `decreto-ley-*/`, `decreto-legislativo-*/`, `…` | daily | 2026-11-27 06:31 UTC | no change | watched |

## The last 30 days

| Started (UTC) | Source | Read | Added | Changed | Removed | Not published (no reason) | Result | Commits |
| --- | --- | ---: | ---: | ---: | ---: | ---: | --- | ---: |
| [2026-11-27 06:31](checks/2026-11.md#es-boe-autonomico-20261127t063128z) | boe-autonomico | 13 | 0 | 0 | 0 | 0 (0) | no change | — |
| [2026-11-26 06:31](checks/2026-11.md#es-boe-autonomico-20261126t063122z) | boe-autonomico | 13 | 0 | 0 | 0 | 0 (0) | no change | — |
| [2026-11-25 06:26](checks/2026-11.md#es-boe-autonomico-20261125t062653z) | boe-autonomico | 13 | 0 | 0 | 0 | 0 (0) | no change | — |
| [2026-11-24 07:27](checks/2026-11.md#es-boe-autonomico-20261124t072709z) | boe-autonomico | 13 | 0 | 0 | 0 | 0 (0) | no change | — |
| [2026-11-23 14:02](checks/2026-11.md#es-boe-autonomico-20261123t140223z) | boe-autonomico | 12 | 0 | 0 | 0 | 0 (0) | no change | — |
| [2026-11-23 01:08](checks/2026-11.md#es-boe-autonomico-20261123t010827z) | boe-autonomico | 10 | 0 | 0 | 0 | 0 (0) | no change | — |

## Check it yourself

```
python tools/checktrail.py                      # the latest check of every source
python tools/checktrail.py --day 2026-11-23     # every check of a day
python tools/checktrail.py --act <id>           # when an act was seen and published
git log --grep='^Kind: check' --format='%ci %s'  # the checks in the history
```

Only the official publication has legal force; the texts here are copies for reading and searching.
