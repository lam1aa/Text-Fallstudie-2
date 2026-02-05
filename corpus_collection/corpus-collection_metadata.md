(corpus-collection_metadata)=
# Metadaten
```{admonition} Feinlernziel(e) dieses Kapitels
:class: lernziele
Sie sind mit der Idee von Metadaten vertraut und kennen basale Metadatenschemata für Korpora und Korpus-Elemente.
```

Metadaten sind Daten über Daten. Sie liefern kontextuelle Informationen, die helfen, die Bedeutung, Herkunft, Struktur und Nutzungsmöglichkeiten eines Datensatzes besser zu verstehen. In den Digital Humanities sind Metadaten unerlässlich, um die Volltextkorpora systematisch zu organisieren, auffindbar zu machen und deren inhaltliche und strukturelle Qualität zu sichern.

**Metadatenschemata**

Es gibt verschiedene Metadatenschemata, die entwickelt wurden, um spezifische Anforderungen unterschiedlicher Disziplinen und Anwendungen zu erfüllen. Zu den bekanntesten gehören:

1. **<a href="https://www.dublincore.org/specifications/dublin-core/dces/" class="external-link" target="_blank">Dublin Core</a>**: Ein einfaches und weit verbreitetes Schema, das 15 grundlegende Elemente umfasst, wie Titel, Autor, Thema und Datum.
2. **<a href="https://tei-c.org/" class="external-link" target="_blank">TEI (Text Encoding Initiative)</a>**: Speziell für Texte entwickelt, bietet TEI detaillierte Richtlinien zur Auszeichnung von Texten und zur Erfassung von deren Metadaten im [`<teiHeader>`](https://tei-c.org/release/doc/tei-p5-doc/de/html/ref-teiHeader.html).
3. **<a href="https://www.loc.gov/standards/mods/" class="external-link" target="_blank">MODS (Metadata Object Description Schema)</a>**: Von der Library of Congress entwickelt, bietet MODS eine umfangreichere Beschreibung als Dublin Core und ist besonders für bibliographische Informationen geeignet.
4. **<a href="https://www.loc.gov/standards/mets/" class="external-link" target="_blank">METS (Metadata Encoding and Transmission Standard)</a>**: Ein Standard zur Kodierung und Übertragung von Digitalisaten und deren Metadaten, häufig in Bibliotheken und Archiven verwendet.

## Metadaten zur Beschreibung eines Korpus

Bei der Beschreibung eines gesamten Korpus sind die Metadaten entscheidend, um den Kontext, den Umfang und die Struktur des Korpus zu dokumentieren. Wichtige Aspekte sind unter anderem:

- **Titel und Beschreibung**: Um das Korpus eindeutig zu identifizieren und dessen Inhalt zu beschreiben.
- **Ersteller:innen und/oder Herausgeber:innen**: Angaben zu den Personen oder Institutionen, die das Korpus erstellt und veröffentlicht haben.
- **Datum**: Zeitangaben zur Erstellung und Veröffentlichung des Korpus.
- **Umfang und Format**: Informationen über die Anzahl der enthaltenen Dokumente und deren Dateiformate.
- **Sprache**: Die im Korpus vertretenen Sprachen.
- **Thematik und Schlagworte**: Stichworte, die die inhaltlichen Schwerpunkte des Korpus beschreiben.

**Beispiel unter Verwendung Dublin Core**

Ein beispielhaftes Metadaten-Set für ein Korpus könnte unter Verwendung von Dublin Core so aussehen:

- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/title/" class="external-link" target="_blank">DC.title</a>**: "Korpus der Pressemitteilungen des Lands Berlin von 2011-2024"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/description/" class="external-link" target="_blank">DC.description</a>**: "Eine Sammlung der digital veröffentlichen Pressemitteilungen publiziert über die Website berlin.de aus den Jahren 2011 bis 2024"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/creator/" class="external-link" target="_blank">DC.creator</a>**: "Henny Sluyter-Gäthje, Daniil Skorinkin, Peer Trilcke für QUADRIGA. Berlin-Brandenburgische Datenkompetenzzentrum für Digital Humanities und Verwaltungswissenschaft"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/publisher/" class="external-link" target="_blank">DC.publisher</a>**: "<a href="https://www.berlin.de" class="external-link" target="_blank">www.berlin.de</a>" 
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/date/" class="external-link" target="_blank">DC.date</a>**: "2025-04-04"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/format/" class="external-link" target="_blank">DC.format</a>**: "HTML, TXT"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/language/" class="external-link" target="_blank">DC.language</a>**: "Deutsch"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/subject/" class="external-link" target="_blank">DC.subject</a>**: ""
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/coverage/" class="external-link" target="_blank">DC.coverage</a>**: "21. Jahrhundert, Deutschland"

## Metadaten für einzelne Korpus-Elemente

Für einzelne Elemente eines Korpus, wie beispielsweise einzelne Artikel oder Dokumente, sind spezifische Metadaten notwendig, um diese präzise zu identifizieren und zu kontextualisieren. Wichtige Metadaten umfassen hier z.B.:

- **Titel und Autor:innen**: Um das Dokument eindeutig zu identifizieren.
- **Datum der Veröffentlichung**: Für zeitliche Einordnung.
- **Quelle**: Angaben zur ursprünglichen Publikation oder Fundort.
- **Sprache**: Die im Dokument verwendete Sprache.
- **Identifier**: Ein eindeutiger Identifikator wie eine DOI oder eine andere Art von Kennung.

**Beispiel unter Verwendung von Dublin Core**

Für eine einzelne Pressemitteilung könnten die Metadaten so aussehen:

- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/title/" class="external-link" target="_blank">DC.title</a>**: "Straßenfest auf dem Hermann-Ehlers-Platz am 03.05.2024 zum 'Aktionstag BUNT VERBINDET'"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/creator/" class="external-link" target="_blank">DC.creator</a>**: "N.N."
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/date/" class="external-link" target="_blank">DC.date</a>**: "2024-04-19"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/source/" class="external-link" target="_blank">DC.publisher</a>**: "Bezirksamt Steglitz-Zehlendorf"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/subject/" class="external-link" target="_blank">DC.subject</a>**: "Gleichstellung"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/coverage/" class="external-link" target="_blank">DC.coverage</a>**: "2024, Berlin"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/language/" class="external-link" target="_blank">DC.language</a>**: "Deutsch"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/language/" class="external-link" target="_blank">DC.source</a>**: "https://www.berlin.de/ba-steglitz-zehlendorf/aktuelles/pressemitteilungen/2024/pressemitteilung.1438914.php"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/identifier/" class="external-link" target="_blank">DC.identifier</a>**: "30281"

Durch die sorgfältige Erfassung und Verwaltung von Metadaten auf beiden Ebenen – sowohl für das gesamte Korpus als auch für einzelne Elemente – wird die Nutzbarkeit und Nachnutzbarkeit von Forschungsdaten in den Digital Humanities erheblich verbessert. Dies trägt zur besseren Auffindbarkeit, Nachvollziehbarkeit und langfristigen Erhaltung der Daten bei.
