# <picture><source media="(prefers-color-scheme: dark)" srcset="https://ran.protezionecivile.it/img/logo/bianco_rosso.svg"><img src="https://ran.protezionecivile.it/img/logo/colori.svg" alt="Logo RAN" height="24"/></picture>&nbsp; DPC-Rete-Accelerometrica-Nazionale-RAN

[![GitHub license](https://img.shields.io/badge/License-Creative%20Commons%20Attribution%204.0%20International-blue)](https://github.com/pcm-dpc/DPC-Rete-Accelerometrica-Nazionale-RAN/blob/master/LICENSE)
[![Last update](https://img.shields.io/badge/dynamic/json?url=https://ran.protezionecivile.it/data/json/last_update.json&query=%24.data_ultima_elaborazione&label=last%20update&color=green&cacheSeconds=3600)](https://ran.protezionecivile.it/data/json/last_update.json)
[![GitHub last commit](https://img.shields.io/github/last-commit/pcm-dpc/DPC-Rete-Accelerometrica-Nazionale-RAN?color=orange)](https://github.com/pcm-dpc/DPC-Rete-Accelerometrica-Nazionale-RAN/commits/master)

La **RAN, Rete Accelerometrica Nazionale**, è una rete di monitoraggio gestita dal Dipartimento della Protezione Civile che registra la risposta al terremoto in termini di accelerazioni del suolo.

È costituita da stazioni accelerometriche digitali distribuite sull'intero territorio nazionale. I dati registrati dalle singole stazioni affluiscono ai server presso il Dipartimento, dove vengono acquisiti ed elaborati in maniera automatica per ottenere una stima dei principali parametri della scossa sismica.

Questa repository è dedicata alla pubblicazione degli **opendata** della rete.

## Struttura del repository

```
repo/
└── anagrafica_stazioni/
    ├── file.geojson
    └── file.schema.json
```

## Aggiornamento dei dati

I file vengono generati **ogni giorno**, il commit di aggiornamento viene effettuato **solo in caso di differenze** rispetto alla versione già pubblicata. Ciascun file riporta nel campo `data_elaborazione` il timestamp di generazione.

## Formato dei dati

Tutti i dataset sono **GeoJSON** conformi a [RFC 7946](https://geojson.org/).

Per ogni file `.geojson` è fornito il relativo `.schema.json` ([JSON Schema](https://json-schema.org/) draft 2020-12) che ne descrive e valida la struttura.

| Dataset | Contenuto | Schema |
|---------|-----------|--------|
| [`elenco_stazioni.geojson`](anagrafica_stazioni/elenco_stazioni.geojson) | Una Feature per stazione con i campi anagrafici di base. | [`elenco_stazioni.schema.json`](anagrafica_stazioni/elenco_stazioni.schema.json) |
| [`elenco_stazioni_sim.geojson`](anagrafica_stazioni/elenco_stazioni_sim.geojson) | Anagrafica con struttura annidata stazioni → sensori → canali. | [`elenco_stazioni_sim.schema.json`](anagrafica_stazioni/elenco_stazioni_sim.schema.json) |

## Collegamenti utili

* [Rete Accelerometrica Nazionale – Dipartimento della Protezione Civile](https://rischi.protezionecivile.gov.it/it/sismico/attivita/rete-accelerometrica-nazionale/)
* [Portale RAN](https://ran.protezionecivile.it/)

## Licenza

[CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/deed.it) - [Visualizza licenza](https://github.com/pcm-dpc/DPC-Rete-Accelerometrica-Nazionale-RAN/blob/master/LICENSE)
