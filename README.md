# World Sync Radio · emisoras

**EN.** Radio station database used by the World Sync Radio app (by AC Compose). `emisoras.json.gz` is a gzipped JSON list of stations; `resumen.json` has the totals.

**ES.** Base de emisoras de radio que usa la app World Sync Radio (por AC Compose). `emisoras.json.gz` es una lista JSON comprimida con gzip; `resumen.json` trae los totales.

## Fields / Campos
`id`, `nombre` (name), `url`, `url_resuelta`, `web`, `pais` (ISO country), `estado` (state/province), `idioma` (language), `codec`, `bitrate`, `etiquetas` (tags), `lat`, `lon`, `prov` (Spanish province letter) and `lugar` (place), `ultimo_chequeo_ok` (last good check), `fuente` (`rb`, `propio`, `propio+rb`), `fuentes` (list of every source that found it).

## Sources / Origen
- Daily export of [Radio-Browser](https://www.radio-browser.info/) (21-10-2026). Radio-Browser: "You may use it in free and non free software." ([api.radio-browser.info](https://api.radio-browser.info/))
- Stations found by World Sync Radio's own search and by hand-checked lists (`fuente = propio`); stations not already in the base are only added after a real connection check that audio arrives.

Updated / Actualizada: 21-10-2026 · Contact: ac.compose@gmail.com
