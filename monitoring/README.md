<!-- lawwatch: written from data/checks by the check trail; edit the records, not this page -->

# Supervisión: qué se lee y qué resulta

[English](README.en.md)

Cómo supervisa global-law todos los países: [global-law monitoring/](https://github.com/lexifina/global-law/tree/main/monitoring). Esta página hace lo mismo solo para Melilla: cada vez que se lee una fuente oficial, cuándo y qué resultó (normas añadidas, modificadas y retiradas). La forma legible por máquina está en [data/checks/](../data/checks/) (JSON Lines, esquema `lexifina-check/1`), en `git log` como commits `Kind: check`, y mes a mes en [checks/](checks/).

**Última comprobación:** 2026-11-24 07:27 UTC, Legislación consolidada del BOE, comunidades autónomas (datos abiertos): 13 direcciones leídas; 0 añadidas, 0 modificadas, 0 retiradas; sin cambios; 0 sin publicar, 0 de ellas sin motivo.

## Fuentes

| Fuente | Carpetas | Frecuencia | Última comprobación correcta | Último resultado | Estado |
| --- | --- | --- | --- | --- | --- |
| [Legislación consolidada del BOE, comunidades autónomas (datos abiertos)](https://www.boe.es/datosabiertos/api/api.php) | `estatuto-de-autonomia/`, `ley-*/`, `decreto-ley-*/`, `decreto-legislativo-*/`, `…` | diaria | 2026-11-24 07:27 UTC | sin cambios | vigilada |

## Los últimos 30 días

| Inicio (UTC) | Fuente | Leídas | Añadidas | Modificadas | Retiradas | Sin publicar (sin motivo) | Resultado | Commits |
| --- | --- | ---: | ---: | ---: | ---: | ---: | --- | ---: |
| [2026-11-24 07:27](checks/2026-11.md#es-boe-autonomico-20261124t072709z) | boe-autonomico | 13 | 0 | 0 | 0 | 0 (0) | sin cambios | — |
| [2026-11-23 14:02](checks/2026-11.md#es-boe-autonomico-20261123t140223z) | boe-autonomico | 12 | 0 | 0 | 0 | 0 (0) | sin cambios | — |
| [2026-11-23 01:08](checks/2026-11.md#es-boe-autonomico-20261123t010827z) | boe-autonomico | 10 | 0 | 0 | 0 | 0 (0) | sin cambios | — |

## Compruébelo usted mismo

```
python tools/checktrail.py                      # la última comprobación de cada fuente
python tools/checktrail.py --day 2026-11-23     # todas las comprobaciones de un día
python tools/checktrail.py --act <id>           # cuándo se vio y se publicó una norma
git log --grep='^Kind: check' --format='%ci %s'  # las comprobaciones en el historial
```

Solo tiene fuerza jurídica la publicación oficial (el «Boletín Oficial del Estado» y los diarios oficiales autonómicos); los textos de este repositorio son copias para leer y buscar.
