# World Sync Radio · emisoras

**EN.** Radio station database used by the World Sync Radio app (by AC Compose). `emisoras.json.gz` is a gzipped JSON list of stations; `resumen.json` has the totals.

**ES.** Base de emisoras de radio que usa la app World Sync Radio (por AC Compose). `emisoras.json.gz` es una lista JSON comprimida con gzip; `resumen.json` trae los totales.

## Fields / Campos
`id`, `nombre` (name), `url`, `url_resuelta`, `web`, `pais` (ISO country), `estado` (state/province), `idioma` (language), `codec`, `bitrate`, `etiquetas` (tags), `lat`, `lon`, `ultimo_ok` (last good check), `fuente` (`rb`, `propio`, `propio+rb`).

## Sources / Origen
- Daily export of [Radio-Browser](https://www.radio-browser.info/) (21-10-2026). Radio-Browser: "You may use it in free and non free software." ([api.radio-browser.info](https://api.radio-browser.info/))
- Stations found by World Sync Radio's own search (`fuente = propio`).

Updated / Actualizada: 21-10-2026 · Contact: ac.compose@gmail.com
