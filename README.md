# Keuken in Beeld open data 2026

Nederlandstalige, open (CC BY 4.0) datasets van **Keuken in Beeld** (keukeninbeeld.nl), als publicatiepakket: JSON zoals gepubliceerd + CSV-vlakke versie.

English (short): open datasets published by Keuken in Beeld (keukeninbeeld.nl). JSON as published on the site plus flattened CSV. Licence as declared by the site: CC BY 4.0. Please attribute: "Bron: Keuken in Beeld (https://keukeninbeeld.nl/<pagina>) - zie per dataset de pagina-URL hieronder. Voor het keukenzaken-register geldt aanvullend: adresgegevens (c) OpenStreetMap-bijdragers (ODbL).".

## Licentie / License

**CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/)** - Gedeclareerd in de Dataset JSON-LD van de vier index-pagina's en in het veld 'licentie' van de JSON-bestanden: https://creativecommons.org/licenses/by/4.0/ (CC BY 4.0). Het bestand keukenzaken-register.json declareert zelf: 'CC BY 4.0; adresgegevens (c) OpenStreetMap-bijdragers (ODbL)'. Voor het register is geen eigen Dataset-pagina gevonden (https://keukeninbeeld.nl/keukenzaken-register/ geeft 404); de licentie-verklaring komt daarom uitsluitend uit het JSON-bestand zelf.

## Bronvermelding / Required attribution

`Bron: Keuken in Beeld (https://keukeninbeeld.nl/<pagina>) - zie per dataset de pagina-URL hieronder. Voor het keukenzaken-register geldt aanvullend: adresgegevens (c) OpenStreetMap-bijdragers (ODbL).`

Per dataset de door de site zelf voorgeschreven citatie staat bij de dataset hieronder.

## Inhoud / Contents

| Dataset | Canonieke pagina | Bestanden | Rijen |
|---|---|---|---|
| Keukenprijs-index Nederland 2026 | https://keukeninbeeld.nl/keukenprijs-index | `data/keukenprijs-index-per-opstelling.csv`, `data/keukenprijs-index-per-merk.csv`, `data/keukenprijs-index.json` | perOpstelling: 4, perMerk: 15 |
| Aanbetaling-keukenindex Nederland 2026 | https://keukeninbeeld.nl/aanbetaling-keuken-index | `data/aanbetaling-keuken-index.csv`, `data/aanbetaling-keuken-index.json` | datapunten: 15 |
| Keuken-garantie-index Nederland 2026 | https://keukeninbeeld.nl/keuken-garantie-index | `data/keuken-garantie-index.csv`, `data/keuken-garantie-index-niet-gepubliceerd.csv`, `data/keuken-garantie-index.json` | datapunten: 14, nietGepubliceerd: 7 |
| Keuken-levertijdindex Nederland 2026 | https://keukeninbeeld.nl/keuken-levertijd-index | `data/keuken-levertijd-index.csv`, `data/keuken-levertijd-index-niet-gepubliceerd.csv`, `data/keuken-levertijd-index.json` | datapunten: 13, nietGepubliceerd: 5 |
| Keukenzaken-register Nederland | (geen dedicated pagina gevonden) | `data/keukenzaken-register.csv`, `data/keukenzaken-register-groepen.csv`, `data/keukenzaken-register.json` | zaken: 1040, groepen: 1 |

## Keukenprijs-index Nederland 2026

- **Canonieke pagina op de site:** https://keukeninbeeld.nl/keukenprijs-index
- **Download op de site:** JSON, zie `data/keukenprijs-index.json` (hier ongewijzigd opgenomen, gedownload 2026-11-08)
- **Omschrijving (zoals de site):** Richtprijzen voor een complete nieuwe keuken in Nederland, per opstelling en per merk, inclusief apparatuur en montage. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt.
- **Bronvermelding:** `Bron: Keuken in Beeld (https://keukeninbeeld.nl/keukenprijs-index)`
- **Citatie zoals de site die geeft:** Keukenprijs-index 2026, Keuken in Beeld (keukeninbeeld.nl)
- **Actualisering:** Jaarlijks bijgewerkt en tussentijds getoetst (volgens de pagina).

### Methode (letterlijk overgenomen van de site)

> Deze index is samengesteld door Keuken in Beeld op basis van doorlopende analyse van het openbare Nederlandse keukenaanbod: prijsindicaties van fabrikanten en dealers, showroom- en actieprijzen en de landelijke richtprijzen die wij per opstelling, stijl en merk publiceren en bijhouden. Het zijn richtprijzen, geen verkoopdata - voor een exact bedrag is altijd een offerte op maat nodig.
>
> De index wordt jaarlijks bijgewerkt (huidige editie: 2026) en tussentijds getoetst aan het openbare aanbod. Laatste controle: 24 september 2026 - daarbij zijn de instapprijs van eilandkeukens en de LEICHT-band bijgesteld op basis van actuele dealer- en showroomprijzen. Citeren mag vrij, met bronvermelding: Keukenprijs-index, Keuken in Beeld (keukeninbeeld.nl).

**Grondslag (veld `grondslag` in JSON):** Bedragen zijn richtprijzen inclusief btw, apparatuur en montage, tenzij anders vermeld. Het zijn geen verkoopdata: voor een exact bedrag is altijd een offerte op maat nodig.

**Aanvullende opmerkingen:** In het JSON-bestand (niet in de CSV's): landelijkGemiddelde {min 8000, max 25000}, valuta EUR, peildatum 2026-09-24, bijgewerkt 2026-09-24, veld 'n' = 28 (betekenis niet toegelicht in het bestand) en 'toelichting' (opstelling: 'Richtprijzen inclusief apparatuur en montage. Instap = basisapparatuur en kunststof werkblad; premium = A-merk-apparatuur, steen of keramiek.'; merk: 'Vanaf-prijzen voor een rechte tot compacte hoekopstelling; uitgebreide toelichting per merk op de gelinkte merkpagina's.').

### Kolommen - `data/keukenprijs-index-per-opstelling.csv` (4 rijen, afgeleid van JSON-array `perOpstelling`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `opstelling` | Opstelling van de keuken (bijv. Rechte keuken, Hoekkeuken). |
| `segmenten_instap_min` | Richtprijs instap-segment, ondergrens (EUR). |
| `segmenten_instap_max` | Richtprijs instap-segment, bovengrens (EUR). |
| `segmenten_middensegment_min` | Richtprijs middensegment, ondergrens (EUR). |
| `segmenten_middensegment_max` | Richtprijs middensegment, bovengrens (EUR). |
| `segmenten_premium_min` | Richtprijs premium-segment, ondergrens (EUR). |
| `segmenten_premium_max` | Richtprijs premium-segment, bovengrens (EUR). |
| `segmenten_premium_openBovengrens` | 'True' als de bovengrens van premium open is (alleen ingevuld bij 1 rij); anders leeg. |

### Kolommen - `data/keukenprijs-index-per-merk.csv` (15 rijen, afgeleid van JSON-array `perMerk`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `merk` | Merknaam. |
| `segment` | Segment van het merk volgens de index. |
| `vanaf_min` | Vanaf-prijs, ondergrens (EUR). |
| `vanaf_max` | Vanaf-prijs, bovengrens (EUR). |
| `url` | Merkpagina op keukeninbeeld.nl. |
| `vanaf_opmerking` | Opmerking bij de vanaf-prijs (1 rij), anders leeg. |

## Aanbetaling-keukenindex Nederland 2026

- **Canonieke pagina op de site:** https://keukeninbeeld.nl/aanbetaling-keuken-index
- **Download op de site:** JSON, zie `data/aanbetaling-keuken-index.json` (hier ongewijzigd opgenomen, gedownload 2026-11-08)
- **Omschrijving (zoals de site):** Maximale aanbetalingspercentages, betaalmomenten en annuleringsregels bij de aankoop van een keuken, met per cijfer de bron-URL en een letterlijk citaat. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt.
- **Bronvermelding:** `Bron: Keuken in Beeld (https://keukeninbeeld.nl/aanbetaling-keuken-index)`
- **Citatie zoals de site die geeft:** Aanbetaling-keukenindex 2026, Keuken in Beeld (keukeninbeeld.nl)
- **Actualisering:** Jaarlijks bijgewerkt en tussentijds gecontroleerd (volgens de pagina).

### Methode (letterlijk overgenomen van de site)

> Deze index is samengesteld door Keuken in Beeld. Wij hebben de voorwaarden en veelgestelde vragen van de CBW-erkend, publicaties van de ACM en pagina's van aanbieders geopend en alleen cijfers overgenomen die er letterlijk staan. Van elk cijfer bewaren wij de bron-URL, een letterlijk citaat en de leesdatum.
>
> Wat de index niet is: het zijn geen verkoopdata, geen overzicht van wat winkels in de praktijk vragen en geen juridisch advies. De offerte en algemene voorwaarden van uw eigen winkel zijn leidend.
>
> Laatste controle: 7 oktober 2026. De index wordt jaarlijks bijgewerkt en tussentijds gecontroleerd. Citeren mag vrij, met bronvermelding: Aanbetaling-keukenindex 2026, Keuken in Beeld (keukeninbeeld.nl)

**Grondslag (veld `grondslag` in JSON):** Percentages zijn maxima uit branchevoorwaarden en wet of gepubliceerde werkwijzen van aanbieders; ze zijn geen verkoopdata. Het bedrag dat u betaalt staat in uw eigen offerte.

### Kolommen - `data/aanbetaling-keuken-index.csv` (15 rijen, afgeleid van JSON-array `datapunten`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `id` | Stabiele sleutel van het datapunt. |
| `categorie` | Soort datapunt zoals in het bronbestand (bijv. merk, norm, regel, afwijking, wet, annulering, betaalmoment, zekerheid, aanbieder; per index verschillend). |
| `onderwerp` | Waar het cijfer over gaat. |
| `waarde_min` | Ondergrens van de waarde (numeriek, eenheid in 'eenheid'); leeg indien geen numerieke waarde. |
| `waarde_max` | Bovengrens van de waarde (numeriek, eenheid in 'eenheid'); leeg indien geen numerieke waarde. |
| `eenheid` | Eenheid van de waarde (bijv. jaar, weken, dagen, % van de koopsom, moment, regeling). |
| `tekst` | Samenvattende tekst van de waarde zoals de site die toont. |
| `bron_url` | URL van de primaire bron. |
| `bron_citaat` | Letterlijk citaat uit de primaire bron. |
| `bron_gelezen` | Datum (ISO) waarop de primaire bron is gelezen. |
| `bevestiging_url` | URL('s) van aanvullende bevestigende bron(nen); meerdere gescheiden door ' / '. |
| `bevestiging_citaat` | Letterlijk(e) citaat/citaten uit de bevestigende bron(nen); gescheiden door ' / '. |
| `bevestiging_gelezen` | Leesdatum(s) van de bevestigende bron(nen); gescheiden door ' / '. |
| `waarde` | Alleen gevuld bij datapunten zonder numerieke waarde: tekstuele waarde (bijv. 'bij aflevering'). |
| `opmerking` | Toelichting bij het datapunt (indien aanwezig). |
| `merk` | Merk of (bij regels) 'Wet'; leeg als niet van toepassing. |

## Keuken-garantie-index Nederland 2026

- **Canonieke pagina op de site:** https://keukeninbeeld.nl/keuken-garantie-index
- **Download op de site:** JSON, zie `data/keuken-garantie-index.json` (hier ongewijzigd opgenomen, gedownload 2026-11-08)
- **Omschrijving (zoals de site):** Gepubliceerde garantietermijnen van keukenmerken en de regels uit de wet en de CBW-erkend voorwaarden, met per cijfer de bron-URL en een letterlijk citaat. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt.
- **Bronvermelding:** `Bron: Keuken in Beeld (https://keukeninbeeld.nl/keuken-garantie-index)`
- **Citatie zoals de site die geeft:** Keuken-garantie-index 2026, Keuken in Beeld (keukeninbeeld.nl)
- **Actualisering:** Jaarlijks bijgewerkt en tussentijds gecontroleerd (volgens de pagina).

### Methode (letterlijk overgenomen van de site)

> Deze index is samengesteld door Keuken in Beeld. Wij hebben de openbare pagina's van keukenmerken, de voorwaarden van de CBW-erkend en de overheidspagina's over garantie geopend en alleen cijfers overgenomen die er letterlijk staan. Van elk cijfer bewaren wij de bron-URL, een letterlijk citaat en de leesdatum. Een cijfer dat wij niet konden terugvinden op een pagina die wij hebben gelezen, staat er niet in.
>
> Wat de index niet is: het zijn geen verkoopdata, geen ervaringen van klanten en geen garantie voor uw keuken. Het zijn gepubliceerde termijnen. De garantie op uw keuken staat in uw offerte en overeenkomst. Onze lijst is bovendien niet volledig: ontbrekende merken zijn merken zonder cijfer op een pagina die wij lazen, geen merken met een slechte of goede garantie.
>
> Laatste controle: 9 oktober 2026. De index wordt jaarlijks bijgewerkt en tussentijds gecontroleerd. Citeren mag vrij, met bronvermelding: Keuken-garantie-index 2026, Keuken in Beeld (keukeninbeeld.nl)

**Grondslag (veld `grondslag` in JSON):** Garantietermijnen zijn wat merken en fabrikanten zelf publiceren, naast de wettelijke basis; ze zijn geen beoordeling van kwaliteit. De garantie op uw eigen keuken staat in uw koopovereenkomst.

**Aanvullende opmerkingen:** Naast de datapunten bevat het JSON-bestand het array 'nietGepubliceerd' (merken waarvoor bewust geen cijfer is opgenomen, met reden en bron); dit staat in een aparte CSV.

### Kolommen - `data/keuken-garantie-index.csv` (14 rijen, afgeleid van JSON-array `datapunten`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `id` | Stabiele sleutel van het datapunt. |
| `categorie` | Soort datapunt zoals in het bronbestand (bijv. merk, norm, regel, afwijking, wet, annulering, betaalmoment, zekerheid, aanbieder; per index verschillend). |
| `merk` | Merk of (bij regels) 'Wet'; leeg als niet van toepassing. |
| `onderwerp` | Waar het cijfer over gaat. |
| `waarde_min` | Ondergrens van de waarde (numeriek, eenheid in 'eenheid'); leeg indien geen numerieke waarde. |
| `waarde_max` | Bovengrens van de waarde (numeriek, eenheid in 'eenheid'); leeg indien geen numerieke waarde. |
| `eenheid` | Eenheid van de waarde (bijv. jaar, weken, dagen, % van de koopsom, moment, regeling). |
| `tekst` | Samenvattende tekst van de waarde zoals de site die toont. |
| `opmerking` | Toelichting bij het datapunt (indien aanwezig). |
| `bevestiging_url` | URL('s) van aanvullende bevestigende bron(nen); meerdere gescheiden door ' / '. |
| `bevestiging_citaat` | Letterlijk(e) citaat/citaten uit de bevestigende bron(nen); gescheiden door ' / '. |
| `bevestiging_gelezen` | Leesdatum(s) van de bevestigende bron(nen); gescheiden door ' / '. |
| `bron_url` | URL van de primaire bron. |
| `bron_citaat` | Letterlijk citaat uit de primaire bron. |
| `bron_gelezen` | Datum (ISO) waarop de primaire bron is gelezen. |
| `waarde_waarde` | Leeg veld (in het bronbestand een null-waarde bij 'geen vaste wettelijke garantietermijn'); alleen in de garantie-index. |

### Kolommen - `data/keuken-garantie-index-niet-gepubliceerd.csv` (7 rijen, afgeleid van JSON-array `nietGepubliceerd`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `merk` | Merk waarvoor de index bewust geen cijfer opneemt (leeg bij segment-rijen). |
| `toelichting` | Reden waarom geen cijfer is opgenomen, zoals de site die geeft. |
| `bron_url` | URL van de bron waarop die reden berust. |
| `bron_citaat` | Letterlijk citaat uit die bron. |
| `bron_gelezen` | Datum (ISO) waarop de bron is gelezen. |

## Keuken-levertijdindex Nederland 2026

- **Canonieke pagina op de site:** https://keukeninbeeld.nl/keuken-levertijd-index
- **Download op de site:** JSON, zie `data/keuken-levertijd-index.json` (hier ongewijzigd opgenomen, gedownload 2026-11-08)
- **Omschrijving (zoals de site):** Gepubliceerde levertijden van keukenmerken en de fasen van een keukentraject, met per cijfer de bron-URL en een letterlijk citaat. Onafhankelijk samengesteld door Keuken in Beeld, dat zelf geen keukens verkoopt.
- **Bronvermelding:** `Bron: Keuken in Beeld (https://keukeninbeeld.nl/keuken-levertijd-index)`
- **Citatie zoals de site die geeft:** Keuken-levertijdindex 2026, Keuken in Beeld (keukeninbeeld.nl)
- **Actualisering:** Jaarlijks bijgewerkt en tussentijds gecontroleerd (volgens de pagina).

### Methode (letterlijk overgenomen van de site)

> Deze index is samengesteld door Keuken in Beeld. Wij hebben de openbare pagina's van keukenmerken, de voorwaarden van de CBW-erkend en een adviessite geopend en alleen cijfers overgenomen die er letterlijk staan. Van elk cijfer bewaren wij de bron-URL, een letterlijk citaat en de leesdatum. Een cijfer dat wij niet konden terugvinden op een pagina die wij hebben gelezen, staat er niet in.
>
> Wat de index niet is: het zijn geen verkoopdata, geen levertijden uit onze eigen leads en geen garantie voor uw keuken. Het zijn gepubliceerde richtwaarden. De levertijd van uw keuken staat in uw offerte en is bindend als u die als vaste levertijd afspreekt. Onze lijst is bovendien niet volledig: ontbrekende merken zijn merken zonder openbaar cijfer, geen merken met een slechte of goede levertijd.
>
> Laatste controle: 7 oktober 2026. De index wordt jaarlijks bijgewerkt en tussentijds gecontroleerd. Citeren mag vrij, met bronvermelding: Keuken-levertijdindex 2026, Keuken in Beeld (keukeninbeeld.nl)

**Grondslag (veld `grondslag` in JSON):** Levertijden zijn gepubliceerde richtwaarden van fabrikanten, merken en branchevoorwaarden; ze zijn geen garantie en geen verkoopdata. De levertijd van uw eigen keuken staat in uw offerte.

**Aanvullende opmerkingen:** Naast de datapunten bevat het JSON-bestand het array 'nietGepubliceerd' (niet opgenomen cijfers, met reden en bron); dit staat in een aparte CSV.

### Kolommen - `data/keuken-levertijd-index.csv` (13 rijen, afgeleid van JSON-array `datapunten`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `id` | Stabiele sleutel van het datapunt. |
| `categorie` | Soort datapunt zoals in het bronbestand (bijv. merk, norm, regel, afwijking, wet, annulering, betaalmoment, zekerheid, aanbieder; per index verschillend). |
| `merk` | Merk of (bij regels) 'Wet'; leeg als niet van toepassing. |
| `onderwerp` | Waar het cijfer over gaat. |
| `waarde_min` | Ondergrens van de waarde (numeriek, eenheid in 'eenheid'); leeg indien geen numerieke waarde. |
| `waarde_max` | Bovengrens van de waarde (numeriek, eenheid in 'eenheid'); leeg indien geen numerieke waarde. |
| `eenheid` | Eenheid van de waarde (bijv. jaar, weken, dagen, % van de koopsom, moment, regeling). |
| `tekst` | Samenvattende tekst van de waarde zoals de site die toont. |
| `bron_url` | URL van de primaire bron. |
| `bron_citaat` | Letterlijk citaat uit de primaire bron. |
| `bron_gelezen` | Datum (ISO) waarop de primaire bron is gelezen. |
| `opmerking` | Toelichting bij het datapunt (indien aanwezig). |
| `fase` | Fase van het keukentraject (alleen levertijd-index, indien aanwezig). |
| `bevestiging_url` | URL('s) van aanvullende bevestigende bron(nen); meerdere gescheiden door ' / '. |
| `bevestiging_citaat` | Letterlijk(e) citaat/citaten uit de bevestigende bron(nen); gescheiden door ' / '. |
| `bevestiging_gelezen` | Leesdatum(s) van de bevestigende bron(nen); gescheiden door ' / '. |

### Kolommen - `data/keuken-levertijd-index-niet-gepubliceerd.csv` (5 rijen, afgeleid van JSON-array `nietGepubliceerd`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `merk` | Merk waarvoor de index bewust geen cijfer opneemt (leeg bij segment-rijen). |
| `toelichting` | Reden waarom geen cijfer is opgenomen, zoals de site die geeft. |
| `bron_url` | URL van de bron waarop die reden berust. |
| `bron_citaat` | Letterlijk citaat uit die bron. |
| `bron_gelezen` | Datum (ISO) waarop de bron is gelezen. |
| `segment` | Segment (alleen levertijd-index, indien aanwezig). |
| `onderwerp` | Onderwerp (alleen levertijd-index, indien aanwezig). |

## Keukenzaken-register Nederland

- **Canonieke pagina op de site:** niet gevonden (zie opmerking)
- **Download op de site:** JSON, zie `data/keukenzaken-register.json` (hier ongewijzigd opgenomen, gedownload 2026-11-08)
- **Omschrijving (zoals de site):** Register van keukenzaken in Nederland (naam, plaats, postcode, eventueel keten en groep, link naar de vestigingspagina op keukeninbeeld.nl).
- **Bronvermelding:** `Bron: Keuken in Beeld (https://keukeninbeeld.nl/keukenzaken/)`
- **Citatie zoals de site die geeft:** Keuken in Beeld (keukeninbeeld.nl), Keukenzaken-register Nederland
- **Actualisering:** Niet vermeld; elke rij heeft een 'peildatum'.

**Aanvullende opmerkingen:** Voor dit bestand is GEEN dedicated pagina met Dataset JSON-LD gevonden (/keukenzaken-register/ = 404). De omschrijving hierboven is een neutrale beschrijving van de kolommen, geen tekst van de site. De methode van het register is niet op een pagina toegelicht; alleen per rij staat de bron (OpenStreetMap-node, bij 566 van de 1040 rijen) en per groep een citaat met bron. De vestigingspagina's staan onder https://keukeninbeeld.nl/keukenzaken/ . Persoonsgegevens: het bronbestand bevat GEEN telefoonnummers of e-mailadressen (kolommen: naam, plaats, postcode, keten, groep, url, peildatum, bron); er zijn dus geen kolommen verwijderd. Een scan op e-mail/telefoon-patronen in alle waarden gaf 0 treffers. Het zijn bedrijfsgegevens (naam/plaats/postcode); of een bedrijfsnaam een eenmanszaak met een persoonsnaam is kan niet uit het bestand worden afgeleid.

### Kolommen - `data/keukenzaken-register.csv` (1040 rijen, afgeleid van JSON-array `zaken`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `naam` | Naam van de keukenzaak. |
| `plaats` | Plaats. |
| `postcode` | Postcode (zoals in bron). |
| `keten` | Keten waartoe de zaak behoort (394 van 1040 rijen gevuld). |
| `groep` | Moedergroep van de keten (212 van 1040 rijen gevuld). |
| `url` | Vestigingspagina op keukeninbeeld.nl. |
| `peildatum` | Datum (ISO) van de gegevens voor deze rij. |
| `bron` | OpenStreetMap-node-URL (gevuld bij 566 rijen); (c) OpenStreetMap-bijdragers, ODbL. |

### Kolommen - `data/keukenzaken-register-groepen.csv` (1 rijen, afgeleid van JSON-array `groepen`)

Geneste velden zijn vlak gemaakt met `_` als scheidingsteken (bijv. `bron.url` -> `bron_url`); lijsten van bron-objecten zijn per kolom samengevoegd met ` | `. Lege cel = veld afwezig of null in de JSON.

| Kolom | Beschrijving |
|---|---|
| `slug` | Sleutel van de groep. |
| `naam` | Naam van de groep. |
| `bron_url` | URL van de bron voor de groepsindeling. |
| `bron_uitgever` | Uitgever van die bron. |
| `bron_citaat` | Letterlijk citaat. |
| `bron_gecontroleerd` | Datum (ISO) van controle. |

## Persoonsgegevens

Het keukenzaken-register bevat geen telefoonnummers of e-mailadressen (gecontroleerd op kolomnamen en op patronen in alle waarden: 0 treffers); er zijn daarom geen kolommen uit de CSV verwijderd. Zie de opmerking bij het register over bedrijfsnamen.

## Geen garantie / Disclaimer

De data zijn gepubliceerd zoals de site ze aanbiedt; raadpleeg per datapunt de bron-URL. Dit pakket voegt geen eigen feiten, cijfers of claims toe. / The data are redistributed as published on the site; this package adds no facts of its own.
