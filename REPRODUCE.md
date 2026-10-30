# How this repository was made (Melilla)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Agencia Estatal Boletín Oficial del Estado: legislación consolidada (open-data API) | <https://www.boe.es/datosabiertos/api/legislacion-consolidada> | 2026-10-30 | BOE reuse conditions (licencia tipo, Resolución de 27 de junio de 2024): reuse for commercial and non-commercial purposes with attribution "Basado en datos de la Agencia Estatal Boletín Oficial del Estado" and a link to https://www.boe.es; consolidated texts are informative only. Ley de Propiedad Intelectual art. 13: laws and regulations are not protected. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `estatuto-de-autonomia` | Ley Orgánica 2/1995, de 13 de marzo, de Estatuto de Autonomía de Melilla. | 1 | 1995-03-15 to 1995-03-15 |

The build made 1 commits:

| Commits | Kind |
| ---: | --- |
| 1 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `futuro`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 1 laws in the record.
- 2 tags.

## Dates

Each commit is dated at noon (Africa/Ceuta) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Each version takes effect on the fecha_vigencia that the BOE consolidated text gives the block versions it contains. https://www.boe.es/datosabiertos/api/legislacion-consolidada

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `e6eb4db8dbe63d8a52c91fa2ff0ab5cb6661af9688f2b8176e919dd1dc819209` (43644 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a97ff7ea62c3c7595c5668a297d533da0b74373c`, `check.py` `3e59cb6f05eccb94a9ec14431a7f6781221e83ef`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

1 versions of 1 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Each act is one BOE consolidated text. Its versions are the distinct fecha_vigencia days of its block versions; each version holds, for every block, the latest block version in force on that day.
- Each change is credited to the norm the BOE names on the new block version (id_norma); a block version whose id_norma is not a BOE identifier is left uncredited (committed by the publisher as unexplained).
- Block versions without a real fecha_vigencia (empty or 99999999) cannot be placed in time and are left out. Where a block has two versions on one day, the last in the BOE's order is the text in force that day.
- Units: one file per article, disposition, annex, preamble and signature; the heading blocks (book, title, chapter, section) are kept at the top of the file of the block that follows them.
- A day whose block versions change no words is not a version.
- Included: the Estatuto de Autonomía (an Estatal Ley Orgánica), then the unit's Autonómico norms the BOE consolidates and marks as not exhausted (vigencia_agotada N), oldest first. Repealed norms are left out.
- An act's first commit is its first publication when every block of its earliest version comes from the act itself; otherwise it is the oldest version the BOE holds, naming the norms in it.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- A model (Claude) wrote the fetch and parse code and chose which norms to include; it wrote no law text. Every word of law comes from the BOE consolidated texts.
