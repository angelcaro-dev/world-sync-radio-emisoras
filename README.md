# World Sync Radio · emisoras

**EN.** Radio station database used by the World Sync Radio app (by AC Compose). `emisoras.json.gz` is a gzipped JSON list of stations; `resumen.json` has the totals.

**ES.** Base de emisoras de radio que usa la app World Sync Radio (por AC Compose). `emisoras.json.gz` es una lista JSON comprimida con gzip; `resumen.json` trae los totales.

## Fields / Campos
`id`, `nombre` (name), `url`, `url_resuelta` (final URL after redirects), `web`, `pais` (ISO country), `estado` (state/province), `prov` (Spanish province letter), `lugar` (place), `idioma` (language), `lat`, `lon`, `etiquetas` (tags), `logo`.

New / Nuevos:
- `formato`: MP3 / AAC / AAC+ / OGG / FLAC / HLS. `kbps`: quality (kbit/s). (`codec` and `bitrate` are kept as aliases.)
- `suena` (plays: true/false/null), `ultimo_chequeo` (date of last check), `ultimo_chequeo_ok` (date of last good check). Radio-Browser stations carry Radio-Browser's own check; ours are checked by World Sync Radio in turns (a station that fails 3 times in a row gets `suena=false` but is never deleted).
- `estilos`: list of the app's style keys (`and.style.rock`, `mundo.fado`...), computed with the same rules as the app (tags, name, decade, world musics).
- `ambito`: local / comarcal / provincial / regional / nacional / internet (empty if unknown). `cadena`: network (SER, COPE, Onda Cero...) and `madre` (parent network name) for local branches. `frecuencia`: "FM 103.4" / "AM 1017" when known.
- `urls_recambio`: alternative stream URLs of the same station. `lugares_otros`, `provs_otras`: other places the same stream serves.
- `fuente` (`rb`, `propio`, `propio+rb`) and `fuentes` (every source that found it).

## Sources / Origen
- [Radio-Browser](https://www.radio-browser.info/) full list through its API (`/json/stations`), downloaded weekly (export dump as fallback). Radio-Browser: "You may use it in free and non free software." ([api.radio-browser.info](https://api.radio-browser.info/))
- Stations found by World Sync Radio's own search and by hand-checked lists (`fuente = propio`); stations not already in the base are only added after a real connection check that audio arrives.
- Station lists and addresses found by World Sync Radio in Europe (Oct 2026): public web pages and streams of each station, Icecast status pages of known servers, Wikipedia (CC BY-SA 4.0, names and links only), Wikidata (CC0), OpenStreetMap (ODbL).

## Attributions (CC BY and open licences) / Atribuciones
Some stations were located with the help of these open datasets; each such station lists it in `fuentes` (`cc-by:...`):
- **Portugal**: "Rádios em Portugal: websites e histórico de versões no Arquivo.pt", [dados.gov.pt](https://dados.gov.pt/) (Arquivo.pt), licence CC BY.
- **Finland**: Traficom, Radioasematiedot, [opendata.traficom.fi](https://opendata.traficom.fi/api/v1/Radioasematiedot), CC BY 4.0.
- **Greece**: Ethniko Symvoulio Radiotileorasis (ESR), "Radiofonikoi Stathmoi me Vevaiosi Nomimou Leitourgias", [data.gov.gr](https://data.gov.gr/dataset/radiofonikoi-stathmoi-me-vevaiosi-nomimoy-leitoyrgias), CC BY 4.0.
- **Moldova**: Consiliul Audiovizualului, Registrul furnizorilor de servicii media de radiodifuziune sonora, [dataset.gov.md](https://dataset.gov.md/dataset/30ec53f3-5a87-401a-9ced-01a94f86c2b1), CC BY 4.0.
- **Croatia**: Agencija za elektronicke medije (AEM), Popis medijskih usluga radio, [data.gov.hr](https://data.gov.hr/) / [pmu.e-mediji.hr](https://pmu.e-mediji.hr/), Otvorena dozvola RH (open licence of the Republic of Croatia).
- **Czechia**: Cesky telekomunikacni urad (CTU), Prehled rozhlasovych kmitoctu, [data.ctu.gov.cz](https://data.ctu.gov.cz/), CTU open-data terms (attribution).

Updated / Actualizada: see `resumen.json` · Contact: ac.compose@gmail.com
