---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

(corpus-collection_building-our-corpus)=
# Aufbau des Forschungskorpus

```{important}
Dieses Kapitel erklärt **Schritt für Schritt**, wie das Korpus aus Pressemitteilungen des Landes Berlin erzeugt wurde. Die vollständige, ausführbare Pipeline findest du im Notebook `corpus_building/corpus_building_mass_scraping_press-releases.ipynb`.
```

## 1. Ziel und Herangehensweise beim Aufbau des Forschungskorpus

Wir untersuchen die Entwicklung der Verständlichkeit amtlicher Kommunikation. Dafür nutzen wir sämtliche online publizierten Pressemitteilungen, die direkt der Berliner **Exekutive** zuzuordnen sind. Der Beobachtungszeitraum reicht von **2001 bis 24. 06. 2025** (Datum der Datenerhebung).

*Vorteile dieser Quelle*

* kontinuierlicher Publikationsstrom → Zeitreihenanalyse
* heterogene Absender → Vergleich von Stilen
* frei zugänglich & wohldefiniertes HTML

## 2. Ein- und Ausschlusskriterien

### Eingeschlossene Absender

| Kategorie              | Behörden / Institutionen                                                                                                                                                                                                                                                                                                                                                                      |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Senatsverwaltungen** | Presse‑ & Informationsamt • Bildung, Jugend & Familie • Finanzen • Inneres & Sport • Arbeit, Soziales, Gleichstellung, Integration, Vielfalt & Antidiskriminierung • Justiz & Verbraucherschutz • Kultur & Gesellschaftlicher Zusammenhalt • Stadtentwicklung, Bauen & Wohnen • Mobilität, Verkehr, Klimaschutz & Umwelt • Wirtschaft, Energie & Betriebe • Wissenschaft, Gesundheit & Pflege |
| **Bezirksämter**       | Charlottenburg‑Wilmersdorf • Friedrichshain‑Kreuzberg • Lichtenberg • Marzahn‑Hellersdorf • Mitte • Neukölln • Pankow • Reinickendorf • Spandau • Steglitz‑Zehlendorf • Tempelhof‑Schöneberg • Treptow‑Köpenick                                                                                                                                                                               |
| **Landesbeauftragte**  | Integration & Migration • Aufarbeitung der SED‑Diktatur • Bürger‑ & Polizeibeauftragter • Pflegebeauftragte • Tierschutzbeauftragte • Landeswahlleitung                                                                                                                                                                                                                                       |

### Ausgeschlossene Absender

| Grund                                     | Beispiele                                             |
| ----------------------------------------- | ----------------------------------------------------- |
| **Justiz / Strafverfolgung (Judikative)** | Polizei Berlin • Kammergericht • Staatsanwaltschaften |
| **Fachbehörden mit eigenem Rechtsstatus** | Landesamt für Einwanderung • Rechnungshof …           |

*Begründung*: Diese Einheiten unterliegen nicht der unmittelbaren Weisungsbefugnis des Senats.

<!-- ## 3 Technischer Workflow

1. **Filter setzen** im Online‑Formular → alle oben aufgeführten Institutionen anhaken (siehe URL in der Notebook‑Konstante `SEARCH_ROOT`).
2. **Letzte Ergebnisseite ermitteln** via CSS‑Selektor `li.pager-skip-to-last a` (Stand Juni 2025: Seite 5239).
3. **Pagination ablaufen**

   * Trefferzeilen auslesen (`table tbody tr`).
   * Detailseiten abrufen; Haupttext steckt verlässlich in `#layout-grid__area--maincontent` (Fallback: `#article` oder `#content`).
   * HTML + bereinigter Plain‑Text unter `data/html/<id>.html` bzw. `data/txt/<id>.txt` speichern.
   * Metadaten (Datum, Titel, Ressort, Dateinamen, Token‑Zahl) inkrementell in `data/metadata.csv` anhängen (Autosave alle 100 Datensätze).
4. **Resume‑Fähigkeit**: Vor jedem Lauf werden vorhandene UIDs aus der CSV eingelesen → keine Dubletten, unterbrochene Crawls lassen sich fortsetzen.

```{note}
404‑Seiten werden nach drei Fehlversuchen übersprungen und im Log markiert.
```
-->

## 3 Metadatenstruktur

Die Datei `data/metadata.csv` begleitet jede Pressemitteilung mit acht klaren Feldern – damit lässt sich das Korpus bequem filtern, sortieren oder mit externen Daten anreichern.

| Feld            | Datentyp                       | Bedeutung                                                                                              |
| --------------- | ------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `id`            | Integer (string‑repräsentiert) | Fortlaufende Kennziffer aus der URL (`…/pressemitteilung.<id>.php`) – dient als Primärschlüssel.       |
| `url`           | String                         | Vollständige Adresse der Detailseite (permanent).                                                      |
| `date`          | Datumsstring `DD.MM.YYYY`      | Veröffentlichungsdatum, eins‑zu‑eins aus der Trefferliste (kann später als `datetime` geparst werden). |
| `title`         | String                         | Originalüberschrift (UTF‑8, inklusive Sonderzeichen).                                                  |
| `source`        | String                         | Herausgebende Stelle = Ressort/Bezirksamt/Landesbeauftragte.                                           |
| `filename_html` | String                         | Dateiname der gespeicherten Roh‑HTML (`<id>.html`).                                                    |
| `filename`      | String                         | Dateiname der bereinigten Plain‑Text‑Fassung (`<id>.txt`).                                             |
| `n_tokens`      | Integer                        | Grober Umfangsindikator = Anzahl der whitespace‑getrennten Token im Plain‑Text.                        |

> **Praxisnutzen**
>
> * `date` erlaubt Zeitreihen‑Plots;
> * `source` dient zur Gruppierung (z. B. Bezirksamt vs. Senatsverwaltung);
> * `n_tokens` hilft beim Aufspüren von Ausreißern (extrem kurze oder sehr lange Mitteilungen).

## 4. Korpusumfang (23. 06. 2025)

* Pressemitteilungen: **≈ 51 800**
* Zeitspanne: 2001 – 2025
* Ø Länge: 430 Tokens (Median 394)

Dies ist unser Forschungskorpus 🚀

## 5. Reproduzierbarkeit

Der komplette Prozess läuft in Binder/Colab ohne Anpassungen. Zur Aktualisierung genügen zwei Zeilen:

```
from corpus_building.corpus_building_mass_scraping_press_releases import crawl_all_pages
crawl_all_pages()
```

<!-- 

## 5 Nachbearbeitung

Ein separates Skript entfernt Navigations‑ und Footer‑Artefakte aus allen TXT‑Dateien. Dabei wird nur der Block innerhalb von `#layout-grid__area--maincontent` beibehalten.

## 
-->
