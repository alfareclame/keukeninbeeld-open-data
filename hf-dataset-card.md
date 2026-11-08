---
license: cc-by-4.0
language:
- nl
pretty_name: Keuken in Beeld open data 2026
size_categories:
- 1K<n<10K
task_categories:
- table-question-answering
tags:
- open-data
- netherlands
- dutch
- keukeninbeeld
configs:
- config_name: keukenprijs-index-per-opstelling
  data_files:
  - split: train
    path: data/keukenprijs-index-per-opstelling.csv
- config_name: keukenprijs-index-per-merk
  data_files:
  - split: train
    path: data/keukenprijs-index-per-merk.csv
- config_name: aanbetaling-keuken-index
  data_files:
  - split: train
    path: data/aanbetaling-keuken-index.csv
- config_name: keuken-garantie-index
  data_files:
  - split: train
    path: data/keuken-garantie-index.csv
- config_name: keuken-garantie-index-niet-gepubliceerd
  data_files:
  - split: train
    path: data/keuken-garantie-index-niet-gepubliceerd.csv
- config_name: keuken-levertijd-index
  data_files:
  - split: train
    path: data/keuken-levertijd-index.csv
- config_name: keuken-levertijd-index-niet-gepubliceerd
  data_files:
  - split: train
    path: data/keuken-levertijd-index-niet-gepubliceerd.csv
- config_name: keukenzaken-register
  data_files:
  - split: train
    path: data/keukenzaken-register.csv
- config_name: keukenzaken-register-groepen
  data_files:
  - split: train
    path: data/keukenzaken-register-groepen.csv
---

# Keuken in Beeld open data 2026

Open datasets van Keuken in Beeld (keukeninbeeld.nl), licentie CC BY 4.0 zoals door de site gedeclareerd. Bronvermelding: `Bron: Keuken in Beeld (https://keukeninbeeld.nl/<pagina>) - zie per dataset de pagina-URL hieronder. Voor het keukenzaken-register geldt aanvullend: adresgegevens (c) OpenStreetMap-bijdragers (ODbL).`

English: open datasets from Keuken in Beeld (keukeninbeeld.nl), CC BY 4.0 as declared by the site. Each configuration is one CSV; the original JSON files are in `data/`.

- **Keukenprijs-index Nederland 2026** - Richtprijzen voor een complete nieuwe keuken in Nederland, per opstelling en per merk, inclusief apparatuur en montage. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt. (pagina: https://keukeninbeeld.nl/keukenprijs-index)
- **Aanbetaling-keukenindex Nederland 2026** - Maximale aanbetalingspercentages, betaalmomenten en annuleringsregels bij de aankoop van een keuken, met per cijfer de bron-URL en een letterlijk citaat. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt. (pagina: https://keukeninbeeld.nl/aanbetaling-keuken-index)
- **Keuken-garantie-index Nederland 2026** - Gepubliceerde garantietermijnen van keukenmerken en de regels uit de wet en de CBW-erkend voorwaarden, met per cijfer de bron-URL en een letterlijk citaat. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt. (pagina: https://keukeninbeeld.nl/keuken-garantie-index)
- **Keuken-levertijdindex Nederland 2026** - Gepubliceerde levertijden van keukenmerken en de fasen van een keukentraject, met per cijfer de bron-URL en een letterlijk citaat. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt. (pagina: https://keukeninbeeld.nl/keuken-levertijd-index)
- **Keukenzaken-register Nederland** - Register van keukenzaken in Nederland (naam, plaats, postcode, eventueel keten en groep, link naar de vestigingspagina op keukeninbeeld.nl). (pagina: geen dedicated pagina)

Let op: het keukenzaken-register declareert aanvullend 'adresgegevens (c) OpenStreetMap-bijdragers (ODbL)'.

Zie README.md in de GitHub-repository voor methode (letterlijk van de site) en kolomwoordenboek. De data bevatten geen persoonsgegevens (geen telefoonnummers of e-mailadressen).
