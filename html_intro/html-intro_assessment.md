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

# 🏆Selbsttest: Wissen und Praxis

````{admonition} Hinweis
:class: hinweis
Diese Übungsaufgaben dienen Ihrer Selbsteinschätzung und helfen Ihnen, das im Kapitel Gelernte zu reflektieren.

Sie können die Fragen in beliebiger Reihenfolge beantworten und auch mehrfach versuchen. 

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en), die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten 

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels noch einmal zu bearbeiten. 

**Geschätzte Zeit**: XX

Viel Erfolg!
````

## Frage 1

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question1 = [
    {
        "question": "Welche Aussagen zu Bilddigitalisaten von Text treffen zu? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Sie bewahren die visuelle Gestalt der Originaldokumente einschließlich Layout und Schriftarten",
                "correct": True,
                "feedback": """✓ Korrekt! Dies ist ein Hauptvorteil:
                - Authentische visuelle Wiedergabe
                - Layout bleibt erhalten
                - Schriftarten und Formatierungen bewahrt
                - Wichtig für historische Dokumente"""
            },
            {
                "answer": "Der Textinhalt ist direkt durchsuchbar und maschinenlesbar",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist eine wichtige Einschränkung:
                - Text ist zunächst NICHT maschinenlesbar
                - Optische Zeichenerkennung (OCR) ist erforderlich
                - Erst nach OCR wird der Text durchsuchbar
                - Dies ist ein Nachteil gegenüber Plain Text"""
            },
            {
                "answer": "Gängige Formate sind PDF, PNG und JPG",
                "correct": True,
                "feedback": """✓ Korrekt! Dies sind die häufigsten Formate:
                - PDF: Für Dokumente
                - PNG: Für verlustfreie Bilder
                - JPG: Für komprimierte Bilder
                - TIFF wird auch verwendet, besonders in Archiven"""
            },
            {
                "answer": "Sie eignen sich besonders für die Archivierung historischer Dokumente",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtiger Anwendungsfall:
                - Authentische Wiedergabe des Originals
                - Langzeitarchivierung möglich
                - Visuelle Details bleiben erhalten
                - Standard in Bibliotheken und Archiven"""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz   )
```

## Frage 2

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Textformate den passenden Beschreibungen zu:",
    descriptions=[
        "Bewahrt die visuelle Gestalt des Originals, aber nicht direkt maschinenlesbar",
        "Einfache, unformatierte Textdatei ohne Stilelemente oder Metadaten",
        "Strukturierte Darstellung mit verschachtelten Tags und semantischer Information",
        "Tabellarisches Format, ideal für annotierte Textdaten mit linguistischen Informationen"
    ],
    options=["Bilddigitalisat", "Plain Text", "HTML", "CSV", "XML"],
    correct_mapping={
        "Bewahrt die visuelle Gestalt des Originals, aber nicht direkt maschinenlesbar": "Bilddigitalisat",
        "Einfache, unformatierte Textdatei ohne Stilelemente oder Metadaten": "Plain Text",
        "Strukturierte Darstellung mit verschachtelten Tags und semantischer Information": "HTML",
        "Tabellarisches Format, ideal für annotierte Textdaten mit linguistischen Informationen": "CSV"
    }
)
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question3 = [
    {
        "question": "Für welchen Anwendungsfall wäre CSV das am besten geeignete Format?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Speicherung von Texten mit linguistischen Annotationen wie Lemma und Wortart",
                "correct": True,
                "feedback": """✓ Korrekt! CSV ist ideal dafür:
                - Tabellarische Struktur für Token und Annotationen
                - Jede Zeile ein Token mit zugehörigen Informationen
                - Einfach mit Analysewerkzeugen zu verarbeiten
                - Standard in der Computerlinguistik"""
            },
            {
                "answer": "Archivierung historischer Dokumente mit originalem Layout",
                "correct": False,
                "feedback": """× Nicht geeignet. Hierfür besser:
                - Bilddigitalisate (PDF, PNG)
                - CSV kann kein Layout speichern
                - CSV ist für tabellarische Daten gedacht
                - Keine visuelle Darstellung möglich"""
            },
            {
                "answer": "Darstellung von Webseiten mit Links und Bildern",
                "correct": False,
                "feedback": """× Nicht geeignet. Hierfür besser:
                - HTML für strukturierte Webinhalte
                - CSV kann keine hierarchischen Strukturen gut abbilden
                - Keine Unterstützung für Hyperlinks
                - Keine Einbettung von Bildern"""
            },
            {
                "answer": "Schnelle Bearbeitung von reinem Text ohne Struktur",
                "correct": False,
                "feedback": """× Nicht optimal. Hierfür besser:
                - Plain Text (TXT) für reinen Text
                - CSV ist für strukturierte, tabellarische Daten
                - CSV hat Overhead durch Tabellenstruktur
                - Einfacher Text benötigt kein CSV"""
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz   )
```

## Frage 4

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die HTML-Tags ihren Funktionen zu:",
    descriptions=[
        "Erstellt einen Hyperlink",
        "Fügt ein Bild ein",
        "Erstellt eine ungeordnete Liste (mit Punkten)",
        "Erstellt eine Tabelle"
    ],
    options=["a", "img", "ul", "table", "div", "p"],
    correct_mapping={
        "Erstellt einen Hyperlink": "a",
        "Fügt ein Bild ein": "img",
        "Erstellt eine ungeordnete Liste (mit Punkten)": "ul",
        "Erstellt eine Tabelle": "table"
    }
)
```

## Frage 5

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question5 = [
    {
        "question": "Was sind HTML-Attribute und wofür werden sie verwendet?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Attribute werden im Start-Tag angegeben und bestehen aus einem Namen und einem Wert",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist die grundlegende Struktur:
                - Format: attributname="wert"
                - Im Start-Tag platziert
                - Liefern zusätzliche Informationen
                - Beispiel: href="https://example.com" """
            },
            {
                "answer": "Attribute können nur bei Bild-Tags verwendet werden",
                "correct": False,
                "feedback": """× Nicht korrekt. Attribute sind universell:
                - Können bei fast allen Tags verwendet werden
                - Nicht nur bei Bildern
                - Beispiele: href bei Links, id/class bei vielen Elementen
                - Vielseitig einsetzbar"""
            },
            {
                "answer": "Häufige Attribute sind 'href' bei Links und 'src' bei Bildern",
                "correct": True,
                "feedback": """✓ Korrekt! Das sind wichtige Beispiele:
                - href: URL für Links
                - src: Quelle für Bilder
                - alt: Alternativtext für Bilder
                - id, class: Für Styling und Identifikation"""
            },
            {
                "answer": "Das 'id' und 'class' Attribut dienen zur Identifizierung und Gestaltung per CSS",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtig für Styling:
                - id: Eindeutige Identifikation
                - class: Gruppierung mehrerer Elemente
                - Ermöglichen CSS-Anwendung
                - Auch für JavaScript wichtig"""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz   )
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question6 = [
    {
        "question": "Was bedeutet 'hierarchische Struktur' in HTML?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "HTML-Elemente können ineinander verschachtelt (nested) werden",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist das Kernprinzip:
                - Tags können innerhalb anderer Tags liegen
                - Schafft Eltern-Kind-Beziehungen
                - Ermöglicht komplexe Strukturen
                - Basis des DOM-Baums"""
            },
            {
                "answer": "Alle HTML-Tags müssen auf der gleichen Ebene stehen",
                "correct": False,
                "feedback": """× Nicht korrekt. Das Gegenteil ist der Fall:
                - Tags werden verschachtelt
                - Verschiedene Ebenen sind normal
                - Hierarchie ist zentral für HTML
                - Flache Struktur wäre sehr limitiert"""
            },
            {
                "answer": "Die hierarchische Struktur bildet einen DOM-Baum (Document Object Model)",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtiges Konzept:
                - DOM-Baum repräsentiert die Struktur
                - Browser nutzen ihn zur Darstellung
                - Programme nutzen ihn zum Parsen
                - Ermöglicht gezielte Auswahl von Elementen"""
            },
            {
                "answer": "Verschachtelte Strukturen sind wichtig für Web Scraping",
                "correct": True,
                "feedback": """✓ Korrekt! Praktische Relevanz:
                - Ermöglicht gezielte Inhaltsauswahl
                - Navigation durch die Struktur
                - Extraktion spezifischer Elemente
                - Basis für CSS-Selektoren und XPath"""
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz   )
```

## Frage 7

**Szenario:** Sie sollen folgenden HTML-Code analysieren:

```html
<div class="article">
    <h2>Nachhaltige Mobilität</h2>
    <p>Die Stadt plant den <strong>Ausbau</strong> des Radwegenetzes.</p>
    <ul>
        <li>50 km neue Radwege</li>
        <li><a href="/details">Mehr Informationen</a></li>
    </ul>
</div>
```

**Ihre Aufgabe:**
1. Beschreiben Sie die hierarchische Struktur (welche Elemente sind in welchen enthalten?)
2. Welche Tags würden Sie verwenden, um nur den Haupttext (ohne Liste) zu extrahieren?
3. Wie würden Sie auf das verlinkte Dokument zugreifen?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('html-1')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. Hierarchische Struktur:**

```
div (class="article")                     (Hauptcontainer)
├── h2                                    (Überschrift, Kind von div)
│   └── "Nachhaltige Mobilität"          (Textinhalt)
├── p                                     (Absatz, Kind von div)
│   ├── "Die Stadt plant den "           (Textinhalt)
│   ├── strong                            (Betonung, Kind von p)
│   │   └── "Ausbau"                     (Textinhalt)
│   └── " des Radwegenetzes."            (Textinhalt)
└── ul                                    (Liste, Kind von div)
    ├── li                                (Listenelement)
    │   └── "50 km neue Radwege"         (Textinhalt)
    └── li                                (Listenelement)
        └── a (href="/details")           (Link, Kind von li)
            └── "Mehr Informationen"      (Textinhalt)
```

**Erklärung:**
- Das div-Element ist der Hauptcontainer
- Es enthält direkt drei Kindelemente: h2, p, und ul
- Das p-Element enthält Text und ein verschachteltes strong-Element
- Das ul-Element enthält zwei li-Elemente
- Das zweite li enthält ein a-Element

**2. Extraktion des Haupttexts (ohne Liste):**

Um nur den Haupttext zu extrahieren, würde man:
- **Das h2-Tag** für die Überschrift auswählen
- **Das p-Tag** für den Absatz auswählen
- Die ul-Liste NICHT auswählen

Mögliche Selektoren:
- CSS: `.article h2` und `.article p`
- XPath: `//div[@class='article']/h2` und `//div[@class='article']/p`
- Oder: Alle direkten Kindelemente außer ul auswählen

**3. Zugriff auf das verlinkte Dokument:**

Um auf das verlinkte Dokument zuzugreifen:
- **Tag:** a (Anchor-Tag für Links)
- **Attribut:** href="/details" 
- **Selektor:** `.article a` oder `//a[@href='/details']`
- Der Wert des href-Attributs ist `/details`
- Dies ist eine relative URL (bezieht sich auf die aktuelle Domain)

Beispiel in Python mit BeautifulSoup:
```python
link = soup.select_one('.article a')
url = link['href']  # Gibt '/details' zurück
```
````

## Frage 8

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8 = [
    {
        "question": "Welche Rolle spielt CSS in Bezug auf HTML?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "CSS (Cascading Style Sheets) wird für das Design und die Gestaltung verwendet",
                "correct": True,
                "feedback": """✓ Korrekt! CSS ist für Styling zuständig:
                - Layout und Positionierung
                - Farben und Schriftarten
                - Abstände und Größen
                - Trennung von Inhalt und Design"""
            },
            {
                "answer": "CSS strukturiert die Inhalte der Webseite",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Unterscheidung:
                - HTML strukturiert die Inhalte
                - CSS gestaltet das Aussehen
                - Trennung von Struktur und Design
                - Verschiedene Zuständigkeiten"""
            },
            {
                "answer": "CSS kann direkt in HTML eingefügt werden",
                "correct": True,
                "feedback": """✓ Korrekt! Es gibt mehrere Möglichkeiten:
                - Inline: style-Attribut im Tag
                - Internal: style-Tag im head
                - External: Separate CSS-Datei
                - Verschiedene Methoden für verschiedene Zwecke"""
            },
            {
                "answer": "HTML und CSS sind völlig unabhängig voneinander",
                "correct": False,
                "feedback": """× Nicht ganz korrekt. Es gibt eine Beziehung:
                - CSS referenziert HTML-Elemente
                - Über id und class Attribute verbunden
                - CSS definiert Aussehen von HTML-Elementen
                - Arbeit Hand in Hand, aber getrennte Rollen"""
            }
        ]
    }
]
display_quiz(question8, colors=colors.jupyterquiz   )
```

## Frage 9

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Schritte zur HTML-Extraktion in die richtige Reihenfolge:",
    descriptions=[
        "Identifikation der HTML-Tags, die den relevanten Text enthalten",
        "Analyse der visuellen Struktur der Website",
        "Auswahl der Tags mittels CSS-Selektoren oder XPath",
        "Extraktion des Textinhalts aus den ausgewählten Tags"
    ],
    options=["2", "4", "1", "3"],
    correct_mapping={
        "Analyse der visuellen Struktur der Website": "1",
        "Identifikation der HTML-Tags, die den relevanten Text enthalten": "2",
        "Auswahl der Tags mittels CSS-Selektoren oder XPath": "3",
        "Extraktion des Textinhalts aus den ausgewählten Tags": "4"
    }
)
```

## Frage 10

**Vergleichende Analyse:** Sie müssen entscheiden, welches Format für folgende Anwendungsfälle am besten geeignet ist:

**Szenario A:** Ein historisches Archiv möchte 10.000 handschriftliche Briefe aus dem 19. Jahrhundert digitalisieren und online verfügbar machen.

**Szenario B:** Ein Linguistik-Team möchte 500 Zeitungsartikel mit grammatischen Annotationen (Wortart, Lemma, syntaktische Funktion) versehen.

**Szenario C:** Eine Forschungsgruppe möchte alle Artikel einer Nachrichtenseite systematisch sammeln und den Haupttext für Textanalysen extrahieren.

**Ihre Aufgabe:** Empfehlen Sie für jedes Szenario das am besten geeignete Format (Bilddigitalisat, Plain Text, HTML, oder CSV) und begründen Sie Ihre Entscheidung.

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('html-2')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**Szenario A: Historische handschriftliche Briefe**

**Empfohlenes Format:** Bilddigitalisat (PDF, PNG, TIFF)

**Begründung:**
- **Visuelle Authentizität:** Handschrift und originales Layout bleiben erhalten
- **Historischer Wert:** Papierqualität, Tintenfarbe, Briefstruktur sind sichtbar
- **Schwierige Transkription:** Handschrift erfordert oft manuelle Transkription
- **Archivstandard:** Bibliotheken und Archive verwenden Bildformate für Originaltreue
- **Langzeitarchivierung:** Etablierte Standards für digitale Bildarchivierung

**Zusätzlich sinnvoll:** 
- Plain Text Transkriptionen (nach manueller Erfassung)
- Metadaten in separater Datei (Datum, Absender, Empfänger)

---

**Szenario B: Zeitungsartikel mit linguistischen Annotationen**

**Empfohlenes Format:** CSV

**Begründung:**
- **Tabellarische Struktur:** Perfekt für Token + Annotationen (Wortart, Lemma, Syntax)
- **Standardformat:** Etabliert in der Computerlinguistik
- **Einfache Verarbeitung:** Mit Statistik- und Analysewerkzeugen gut nutzbar
- **Klare Organisation:** Jede Zeile = ein Token mit allen Annotationen
- **Interoperabilität:** Zwischen verschiedenen Tools austauschbar

**Beispielstruktur:**
```csv
ARTIKEL_ID,TOKEN_ID,TOKEN,LEMMA,POS,SYNTAX
art1,1,Der,der,DET,nsubj
art1,2,Artikel,Artikel,NOUN,ROOT
```

**Alternative:** XML/TEI (wenn hierarchische Strukturen wichtig sind)

---

**Szenario C: Nachrichtenseite systematisch scrapen**

**Empfohlenes Format für Speicherung:** HTML **UND** Plain Text

**Begründung:**

**HTML speichern:**
- **Original bewahren:** Komplette Quelle für Nachvollziehbarkeit
- **Strukturinformation:** Tags, Links, Metadaten erhalten
- **Flexibilität:** Spätere Re-Extraktion mit anderen Methoden möglich
- **Debugging:** Bei Problemen kann Original analysiert werden

**Plain Text extrahieren:**
- **Analysefreundlich:** Direkt für Textanalyse verwendbar
- **Speichereffizient:** Kleinere Dateien als HTML
- **Einfache Verarbeitung:** Keine HTML-Parsing mehr nötig
- **Schnelle Analyse:** Sofort mit NLP-Tools nutzbar

**Empfohlener Workflow:**
1. HTML von Website herunterladen und speichern
2. Relevante Teile identifizieren (z.B. article, div class="content")
3. Plain Text extrahieren und separat speichern
4. Metadaten in CSV speichern (URL, Datum, Titel, Autor)

**Dateistruktur:**
```
corpus/
├── html/
│   ├── article_001.html
│   ├── article_002.html
├── txt/
│   ├── article_001.txt
│   ├── article_002.txt
└── metadata.csv
```

**Warum nicht nur ein Format?**
- Nur HTML: Zu viel Overhead für Textanalyse
- Nur Plain Text: Quellennachweis und Struktur gehen verloren
- Kombination: Best of both worlds
````