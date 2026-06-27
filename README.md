# CUNI FSV Research Repository Explorer

A lightweight, **client-side** web app for searching and browsing research output (theses & dissertations) from **Charles University, Faculty of Social Sciences (FSV)**. The records are harvested from the university's public **DSpace** institutional repository via the **OAI-PMH** protocol and presented in a fast, filterable, sortable table — no backend required.

![HTML5](https://img.shields.io/badge/HTML5-static%20app-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black)
![OAI-PMH](https://img.shields.io/badge/OAI--PMH-DSpace%20harvest-006699)

## What it does

- **Harvests** publication metadata from Charles University's DSpace repository (`dspace.cuni.cz`) over **OAI-PMH** (Dublin Core records).
- **Explores** the harvested records in the browser: full-text **search** across title, author, supervisor and keywords; **sortable** columns (year, title, author, supervisor, institute); and live record counts.
- **Switches** between three bundled datasets:

  | Dataset | Scope |
  |---|---|
  | `records.json` | Political Studies subset (filtered from a ~19.8k-record set) |
  | `all_fsv_records.json` | Full FSV harvest (complete set) |
  | `prague_papers_ir.json` | *Prague Papers in International Relations* |

## Data

Each record follows a **Dublin Core**–style schema harvested from the repository — titles, creators (authors), contributors (supervisors), year, institute and keywords — alongside harvest metadata (source endpoint, harvest date, processed/filtered counts). All records are **public bibliographic data** from the university's open repository.

> `all_fsv_records.json` is the complete harvest and is large (~100 MB); the viewer loads each dataset on demand when you switch to it.

## Run it

It's a static site — no build step:

```bash
# serve the folder with any static server
python3 -m http.server 8000
# then open http://localhost:8000
```

(Opening `index.html` directly also works in most browsers, though some block `fetch()` of local files — hence the static server.)

## Tech

- Vanilla **HTML / CSS / JavaScript** — no framework, no dependencies.
- Data sourced via **OAI-PMH** from a **DSpace** repository (Dublin Core metadata).

## License

MIT — see [`LICENSE`](LICENSE).
