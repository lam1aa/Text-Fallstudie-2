(corpus-collection_text_as_digital_objects)=
# Elemente von Korpora: Texte als digitale Objekte
```{admonition} Feinlernziel(e) dieses Kapitels
:class: lernziele
Sie kennen unterschiedliche Realisierungsweisen und Formate von Text im Digitalen.
```

Texte können digital auf sehr unterschiedliche Weisen gespeichert, prozessiert und repräsentiert werden. Die vielfältige Formen von Text im Digitalen weisen dabei jeweils spezifische Eigenschaften und Einsatzmöglichkeiten auf. In diesem Abschnitt werden vier weit verbreitete Erscheinungsformen digitaler Texte vorgestellt: 

- Bilddigitalisate von Text (z.B. PDF, PNG, JPG, TIFF)
- Reiner Text, auch "Plain Text" (TXT)
- Textinhalte auf Websites (HTML) 
- CSV

## Bilddigitalisate von Text

**Charakteristika:**

- **Repräsentation:** Bilddigitalisate sind digitale Abbildungen von physischen Texten. Sie bewahren die visuelle Gestalt der Originaldokumente, einschließlich Layout, Schriftarten und Illustrationen.
- **Formate:** Die gängigsten Formate sind PDF, PNG und JPG.
- **Nutzung:** Diese Form ist besonders nützlich für die Archivierung und den Zugang zu historischen Dokumenten, da sie eine authentische visuelle Wiedergabe des Originals ermöglicht.
- **Einschränkungen:** Der Textinhalt ist in diesen Formaten nicht direkt durchsuchbar oder maschinenlesbar, es sei denn, es wird eine optische Zeichenerkennung (OCR) angewendet.

**Beispiel:**

```{figure} ../book_images/corpus-collection_text_as_digital_objects_image-example.png
---
height: 200
name: Snippet eines Bilddigitalisats
---
```

*Beispiel für ein Bilddigitalisat von Text, hier ein Ausschnitt eines historischen Zeitungsartikels als PNG-Datei*


## Reiner Text, "Plain Text"

**Charakteristika:**

- **Repräsentation:** Plain Text ist eine einfache, unformatierte Textdatei, die nur den reinen Text ohne jegliche Stilelemente oder Metadaten enthält.
- **Formate:** Das gängigste Format ist TXT.
- **Nutzung:** Plain Text ist ideal für einfache Textanalysen und die Datenverarbeitung, da er leicht zu bearbeiten und in verschiedene Softwareumgebungen zu importieren ist.
- **Einschränkungen:** Es fehlen strukturelle und semantische Informationen, etwa in Form von Textauszeichnungen, die für komplexere Analysen oder Darstellungen notwendig sind. 

**Beispiel:**

`
Europäischer Aktionstag zur Gleichstellung von Menschen mit Behinderungen
Wir laden Sie herzlich ein, den „Aktionstag BUNT VERBINDET“ am Freitag den 3. Mai 2024 von 12:00 bis 17:00 Uhr, auf dem Hermann-Ehlers-Platz, auf unserem Straßenfest zu feiern. Der Aktionstag findet anlässlich des Europäischen Protesttages zur Gleichstellung von Menschen mit Behinderungen statt. Ein ganz besonderes Highlight ist unser LeseZelt, in dem Geschichten durch Gebärdensprache, Tastbücher und Leichte Sprache erzählt werden. Hören, sehen, fühlen und verstehen sind für alle gleichermaßen erlebbar.
`
*Beispiel für Reinen Text ohne jede Formatierung, üblicherweise als TXT-Datei gespeichert*

## Textinhalte auf Websites (HTML)

**Charakteristika:**

- **Repräsentation:** Hypertext Markup Language (HTML) ist eine textbasierte Auszeichnungssprache zur strukturierten Repräsentation von Inhalten wie Text, Bilder, Hyperlinks etc. Die Inhalte werden über verschachtelte Tags organisiert, die die semantische Struktur und Metadaten enthalten.
- **Formate:** Dateien im HTML-Format, meist mit der Endung `.html` oder `.htm`. 
- **Nutzung:** HTML bildet das Grundgerüst nahezu jeder Webseite und wird von Browsern (wie Firefox oder Chrome) interpretiert, um Inhalte wie Texte, Bilder und Links darzustellen.
- **Einschränkungen:** Die Erstellung und Verarbeitung von HTML-Dokumenten erfordert eine genaue Kenntnis der Auszeichnungssprache.

**Beispiel:**

```html
<h2 class="title" id="headline_1_0" >Europäischer Aktionstag zur Gleichstellung von Menschen mit Behinderungen</h2>
<div class="text">
    <div class="textile">
        <p>
            <strong>Wir laden Sie herzlich ein, den „Aktionstag BUNT VERBINDET“ am Freitag den 3. Mai 2024 von 12:00 bis 17:00 Uhr, auf dem Hermann-Ehlers-Platz, auf unserem Straßenfest zu feiern.</strong>
        </p>
        <p>
            Der Aktionstag findet anlässlich des <a href="https://www.bpb.de/kurz-knapp/hintergrund-aktuell/520659/5-mai-europaeischer-protesttag-fuer-die-gleichstellung-von-menschen-mit-behinderung/" class="extern" target="_blank" title="Informationen zum Europäischen Protesttag 5. Mai der Bundeszentrale für politische Bildung (Öffnet in neuem Fenster)" rel="noreferrer">Europäischen Protesttages zur Gleichstellung von Menschen mit Behinderungen</a> statt.
        </p>
        <p>
    Ein ganz besonderes Highlight ist unser <strong>LeseZelt</strong>, in dem Geschichten durch Gebärdensprache, Tastbücher und Leichte Sprache erzählt werden. Hören, sehen, fühlen und verstehen sind für alle gleichermaßen erlebbar.
        </p>
    </div>
</div>
```

*Beispiel für ein Ausschnitt aus einem HTML-Dokument, hier ein Ausschnitt einer Pressemitteilung des Bezirkamts Steglitz-Zehlendorf*



## CSV für annotierte Texte

**Charakteristika:**

- **Repräsentation:** CSV (Comma-Separated Values) ist ein tabellarisches Datenformat, bei dem jeder Eintrag in einer Zeile einer Tabelle durch ein Trennzeichen (meist ein Komma) getrennt ist. Es eignet sich gut für die Speicherung von Daten, die aus Texten extrahiert und annotiert wurden.
- **Formate:** Dateien im CSV-Format, oft mit der Endung .csv.
- **Nutzung:** CSV-Dateien werden häufig in der Computerlinguistik verwendet, um annotierte Textdaten zu speichern, wie z.B. Wortformen, Lemmas, syntaktische Strukturen oder semantische Annotationen. Sie sind leicht mit Statistik- und Analysewerkzeugen zu verarbeiten.
- **Einschränkungen:** CSV-Dateien sind weniger flexibel für komplexe Textstrukturen und eignen sich besser für flache, tabellarische Daten.

**Beispiel:** 

```
ID,TOKEN,LEMMA,POS
0,Europäischer,europäisch,ADJ
1,Aktionstag,Aktionstag,NOUN
2,zur,zu,ADP
3,Gleichstellung,Gleichstellung,NOUN
4,von,von,ADP
5,Menschen,Mensch,NOUN
6,mit,mit,ADP
7,Behinderungen,Behinderung,NOUN
```

*CSV-Datei, bei der in der ersten Zeile ein Tabellenkopf steht, in den dann folgenden Zeilen jeweils zunächst eine durchzählende ID, dann ein Wort, gefolgt von  weiteren linguistischen Informationen: der Grundform ("Lemma") und der Wortart ("POS", "Part of Speech")*


| ID  | TOKEN          | LEMMA           | POS   |
|-----|----------------|-----------------|-------|
| 0   | Europäischer   | europäisch      | ADJ   |
| 1   | Aktionstag     | Aktionstag      | NOUN  |
| 2   | zur            | zu              | ADP   |
| 3   | Gleichstellung | Gleichstellung  | NOUN  |
| 4   | von            | von             | ADP   |
| 5   | Menschen       | Mensch          | NOUN  |
| 6   | mit            | mit             | ADP   |
| 7   | Behinderungen  | Behinderung     | NOUN  |
*CSV-Datei lassen sich, wie hier zu sehen, mit üblichen Programmen wie Open Office oder MS Office auch als Tabellen darstellen*


## Zusammenfassung
Jedes der vorgestellten Formate hat eigene Stärken und Schwächen und ist für unterschiedliche Anwendungszwecke geeignet. Während Bilddigitalisate die visuelle Authentizität bewahren, bieten Plain Text und CSV einfache Möglichkeiten zur maschinellen Verarbeitung. HTML hingegen ermöglicht eine detaillierte und semantisch reiche Darstellung von Texten. Das Verständnis dieser Formate ist essentiell für die effektive Arbeit mit digitalen Texten in den Digital Humanities.
