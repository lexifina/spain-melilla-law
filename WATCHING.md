<!-- lawwatch: written from data/checks by the check trail; edit the records, not this page -->

# Vigilancia de las fuentes: qué se vigila para Melilla

[English](WATCHING.en.md)

Cómo vigila global-law las fuentes de cada país: [global-law WATCHING.md](https://github.com/lexifina/global-law/blob/main/WATCHING.md). Esta página hace lo mismo solo para Melilla: cada fuente oficial de la que este repositorio toma texto, qué se lee en ella, con qué frecuencia y cuándo se leyó por última vez. Cada lectura y su resultado: [monitoring/](monitoring/README.md).

| Fuente | Qué se lee | Carpetas | Frecuencia | Última lectura | Estado |
| --- | --- | --- | --- | --- | --- |
| [Legislación consolidada del BOE, comunidades autónomas (datos abiertos)](https://www.boe.es/datosabiertos/api/api.php) | la lista de todas las normas consolidadas (su ámbito, departamento, rango, días de publicación y de entrada en vigor, si su vigencia está agotada y cuándo actualizó el BOE su texto consolidado), y los sumarios diarios del BOE de los últimos 30 días, por las leyes de la sección I aún no consolidadas | `estatuto-de-autonomia/`, `ley-*/`, `decreto-ley-*/`, `decreto-legislativo-*/`, `…` | diaria | 2026-11-28 06:33 UTC | vigilada |

Las fuentes se leen dentro de lo que permiten su robots.txt y sus condiciones, con pausas entre peticiones.
