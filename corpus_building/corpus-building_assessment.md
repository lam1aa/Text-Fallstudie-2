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
        "question": "Welche Schritte sind beim praktischen Korpusaufbau durch Massenscraping notwendig? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Untersuchung der HTML-Struktur der Zielwebsite (z.B. mit dem Browser-Inspektor)",
                "correct": True,
                "feedback": """✓ Korrekt! Die Strukturanalyse ist der erste Schritt:
                - Identifikation relevanter HTML-Elemente
                - Bestimmung von CSS-Selektoren
                - Verständnis des Seitenaufbaus
                - Basis für die Implementierung"""
            },
            {
                "answer": "Extraktion von Links zu allen relevanten Einzelseiten",
                "correct": True,
                "feedback": """✓ Korrekt! Link-Extraktion ist essentiell:
                - Sammeln aller URLs aus Übersichtsseiten
                - Oft aus Tabellen oder Listen
                - Basis für das systematische Crawling
                - Navigation durch das gesamte Korpus"""
            },
            {
                "answer": "Scraping der Einzelseiten mit Speicherung von HTML und bereinigtem Text",
                "correct": True,
                "feedback": """✓ Korrekt! Doppelte Speicherung ist sinnvoll:
                - HTML: Für Nachvollziehbarkeit und Re-Analyse
                - Bereinigter Text: Für direkte Textanalyse
                - Ermöglicht verschiedene Nutzungsszenarien
                - Best Practice beim Korpusaufbau"""
            },
            {
                "answer": "Sofortige manuelle Korrektur jeder extrahierten Seite",
                "correct": False,
                "feedback": """× Nicht korrekt. Bei Massenscraping:
                - Automatisierung ist das Ziel
                - Manuelle Korrektur bei 50.000+ Dokumenten unmöglich
                - Qualitätskontrolle durch Stichproben
                - Nachbearbeitung nur bei systematischen Problemen"""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz)
```

## Frage 2

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question2 = [
    {
        "question": "Welche Rolle spielt BeautifulSoup beim praktischen Korpusaufbau? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "BeautifulSoup ermöglicht das Parsen von HTML-Dokumenten zu einem navigierbaren Parse-Tree",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist die Kernfunktion:
                - Umwandlung von HTML-String in Baum-Struktur
                - Ermöglicht Navigation durch DOM
                - Basis für Element-Suche
                - Mit Parsern wie 'lxml' oder 'html.parser'"""
            },
            {
                "answer": "BeautifulSoup bietet Methoden wie select() und find() zur Extraktion spezifischer Elemente",
                "correct": True,
                "feedback": """✓ Korrekt! Diese Methoden sind zentral:
                - select(): CSS-Selektoren nutzen
                - find(): Einzelne Elemente finden
                - find_all(): Mehrere Elemente finden
                - Flexible Element-Auswahl"""
            },
            {
                "answer": "BeautifulSoup kann Text aus HTML-Elementen extrahieren (z.B. mit get_text())",
                "correct": True,
                "feedback": """✓ Korrekt! Textextraktion ist wichtig:
                - get_text(): Nur Text ohne Tags
                - strip=True: Leerzeichen entfernen
                - Separator angeben: get_text(' ')
                - Basis für saubere Textdaten"""
            },
            {
                "answer": "BeautifulSoup führt automatisch HTTP-Requests durch",
                "correct": False,
                "feedback": """× Nicht korrekt. Aufgabenteilung:
                - HTTP-Requests: requests-Bibliothek
                - HTML-Parsing: BeautifulSoup
                - Beide arbeiten zusammen
                - Trennung ermöglicht Flexibilität"""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz)
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
        "question": "Warum ist die Implementierung von Retry-Logik und Sleep-Intervallen beim Massenscraping wichtig? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Temporäre Netzwerkfehler können durch wiederholte Versuche überwunden werden",
                "correct": True,
                "feedback": """✓ Korrekt! Netzwerk ist nicht immer stabil:
                - DNS-Fehler können vorübergehend sein
                - Timeouts können auftreten
                - Verbindungsabbrüche sind möglich
                - Mehrere Versuche erhöhen Erfolgsrate"""
            },
            {
                "answer": "Sleep-Intervalle verhindern Überlastung des Servers und mögliche Blockierungen",
                "correct": True,
                "feedback": """✓ Korrekt! Serverfreundliches Verhalten:
                - Vermeidet zu hohe Last
                - Respektiert Rate Limits
                - Verhindert IP-Sperrung (429 Too Many Requests)
                - Ethisch geboten"""
            },
            {
                "answer": "Bei HTTP-Status 404 oder 410 sollte kein Retry durchgeführt werden",
                "correct": True,
                "feedback": """✓ Korrekt! Permanente vs. temporäre Fehler:
                - 404 Not Found: Seite existiert nicht
                - 410 Gone: Seite wurde entfernt
                - Diese sind dauerhaft → kein Retry
                - 5xx, 429: temporär → Retry sinnvoll"""
            },
            {
                "answer": "Retry-Logik und Sleep-Intervalle sind nur für große Projekte relevant",
                "correct": False,
                "feedback": """× Nicht korrekt. Immer wichtig:
                - Auch bei kleinen Projekten können Fehler auftreten
                - Best Practice unabhängig von Größe
                - Stabilität und Zuverlässigkeit
                - Ethische Verantwortung"""
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz)
```

## Frage 4

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question4 = [
    {
        "question": "Welche Scraping-Methode eignet sich für folgende Szenarien am besten? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Für statische Übersichtsseiten mit Links zu Einzelartikeln eignet sich requests + BeautifulSoup",
                "correct": True,
                "feedback": """✓ Korrekt! Diese Kombination ist optimal für:
                - Statisches HTML ohne JavaScript
                - Klar strukturierte Seiten (z.B. Tabellen)
                - Systematisches Durchlaufen von Links
                - Wie im Kapitel gezeigt mit Pressemitteilungen"""
            },
            {
                "answer": "Wenn Inhalte erst beim Scrollen nachgeladen werden, ist Selenium notwendig",
                "correct": True,
                "feedback": """✓ Korrekt! Selenium für dynamische Inhalte:
                - JavaScript-Ausführung erforderlich
                - Simulation von Benutzerinteraktionen
                - Nachladen von Inhalten
                - requests würde nur initialen HTML-Code sehen"""
            },
            {
                "answer": "Für mehrere tausend verlinkte Seiten mit ähnlicher Struktur ist scrapy effizienter als requests",
                "correct": True,
                "feedback": """✓ Korrekt! Scrapy-Vorteile:
                - Integriertes Link-Following
                - Paralleles Crawling möglich
                - Robustes Error-Handling
                - Bessere Performance bei großen Projekten"""
            },
            {
                "answer": "requests + BeautifulSoup kann auch JavaScript-generierte Inhalte problemlos extrahieren",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Einschränkung:
                - requests sieht nur initialen HTML-Code
                - JavaScript wird NICHT ausgeführt
                - Dynamische Inhalte fehlen
                - Für JavaScript: Selenium erforderlich"""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz)
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
        "question": "Warum sollten Metadaten parallel zum Scraping-Prozess systematisch erfasst und gespeichert werden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Bei Unterbrechung des Scraping-Prozesses gehen keine Informationen verloren",
                "correct": True,
                "feedback": """✓ Korrekt! Absicherung gegen Abbrüche:
                - Scraping kann Stunden oder Tage dauern
                - Netzwerkprobleme können auftreten
                - Laufende CSV-Speicherung sichert Fortschritt
                - Wiederaufnahme an letzter Stelle möglich"""
            },
            {
                "answer": "Metadaten ermöglichen spätere Analysen wie Zeitreihen und Quellenvergleiche",
                "correct": True,
                "feedback": """✓ Korrekt! Analytischer Wert:
                - Datum: Zeitreihenanalyse
                - Quelle/Ressort: Vergleich verschiedener Absender
                - URL: Rückverfolgbarkeit
                - Länge: Verteilungsanalysen"""
            },
            {
                "answer": "Metadaten helfen bei der Identifikation von Lücken oder Problemen im Korpus",
                "correct": True,
                "feedback": """✓ Korrekt! Qualitätskontrolle:
                - Übersicht über erfasste Dokumente
                - Erkennung fehlender IDs
                - Debugging bei Problemen
                - Vollständigkeitsprüfung"""
            },
            {
                "answer": "Metadaten sollten erst nach Abschluss des gesamten Scraping-Prozesses erstellt werden",
                "correct": False,
                "feedback": """× Nicht korrekt. Parallele Erfassung ist besser:
                - Schutz vor Datenverlust bei Abbruch
                - Laufende Übersicht über Fortschritt
                - Frühzeitige Problemerkennung
                - Best Practice: incrementelle Speicherung"""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz)
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Schritte des Korpusaufbaus in die richtige Reihenfolge:",
    descriptions=[
        "Untersuchung der HTML-Struktur der Übersichtsseite",
        "Scraping der Einzelseiten mit HTTP-Requests",
        "Extraktion aller Links zu Einzelseiten",
        "Extraktion und Speicherung von Text und Metadaten"
    ],
    options=["3", "1", "4", "2"],
    correct_mapping={
        "Untersuchung der HTML-Struktur der Übersichtsseite": "1",
        "Extraktion aller Links zu Einzelseiten": "2",
        "Scraping der Einzelseiten mit HTTP-Requests": "3",
        "Extraktion und Speicherung von Text und Metadaten": "4"
    }
)
```

## Frage 7

**Szenario:** Sie untersuchen eine Nachrichten-Website und finden folgende HTML-Struktur auf der Übersichtsseite:

```html
<table>
  <tbody>
    <tr>
      <td>15.01.2024</td>
      <td><a href="/artikel/12345.html">Neuer Stadtrat gewählt</a></td>
      <td>Rathaus</td>
    </tr>
    <tr>
      <td>14.01.2024</td>
      <td><a href="/artikel/12344.html">Haushalt beschlossen</a></td>
      <td>Finanzen</td>
    </tr>
  </tbody>
</table>
```

**Aufgaben:**
1. Welchen CSS-Selektor würden Sie verwenden, um alle Tabellenzeilen zu finden?
2. Wie würden Sie aus einer Zeile das Datum, den Titel und den Link extrahieren?
3. Wie würden Sie aus dem relativen Link "/artikel/12345.html" eine vollständige URL machen?
4. Welche Metadaten würden Sie für jeden Artikel erfassen?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('corpus-building-1')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. CSS-Selektor für Tabellenzeilen:**

```python
from bs4 import BeautifulSoup
soup = BeautifulSoup(html_string)
rows = soup.select("table tbody tr")
# oder: soup.select("tbody tr")
# oder: soup.find_all("tr")
```

**Erklärung:**
- `table tbody tr`: Findet alle `<tr>`-Elemente innerhalb von `<tbody>` innerhalb von `<table>`
- Spezifischer Selektor verhindert Fehlextr aktionen
- `select()` gibt eine Liste aller passenden Elemente zurück

---

**2. Extraktion von Datum, Titel und Link:**

```python
for tr in rows:
    # Alle Zellen der Zeile holen
    cells = tr.find_all("td")
    
    # Sicherheitscheck
    if len(cells) < 3:
        continue
    
    # Datum aus erster Zelle
    datum = cells[0].get_text(strip=True)
    
    # Titel und Link aus zweiter Zelle
    anchor = cells[1].find("a", href=True)
    if anchor:
        titel = anchor.get_text(strip=True)
        relative_url = anchor["href"]  # oder: anchor.get("href")
    
    # Quelle aus dritter Zelle
    quelle = cells[2].get_text(strip=True)
```

**Wichtige Methoden:**
- `find_all("td")`: Findet alle Zellen
- `get_text(strip=True)`: Extrahiert Text, entfernt Leerzeichen
- `find("a", href=True)`: Findet Link, nur wenn href vorhanden
- `anchor["href"]`: Zugriff auf Attribut

---

**3. Relative zu absoluter URL:**

**Methode A: Manuelle Konkatenation**
```python
base_url = "https://www.nachrichtenportal.de"
relative_url = "/artikel/12345.html"
vollstaendige_url = base_url + relative_url
# Ergebnis: "https://www.nachrichtenportal.de/artikel/12345.html"
```

**Methode B: urllib.parse.urljoin (empfohlen)**
```python
from urllib.parse import urljoin

base_url = "https://www.nachrichtenportal.de"
relative_url = "/artikel/12345.html"
vollstaendige_url = urljoin(base_url, relative_url)
# Ergebnis: "https://www.nachrichtenportal.de/artikel/12345.html"
```

**Vorteil von urljoin:**
- Behandelt verschiedene URL-Formate korrekt
- Berücksichtigt Protokoll und Domain
- Funktioniert auch mit vollständigen URLs (gibt sie unverändert zurück)

---

**4. Zu erfassende Metadaten:**

**Essentiell:**
- **ID:** Eindeutige Kennung (z.B. aus URL: "12345")
- **URL:** Vollständige Artikel-URL
- **Datum:** Veröffentlichungsdatum ("15.01.2024")
- **Titel:** Artikelüberschrift ("Neuer Stadtrat gewählt")
- **Quelle:** Ressort/Abteilung ("Rathaus")

**Zusätzlich empfohlen:**
- **Dateiname (HTML):** Wo wurde das Original gespeichert
- **Dateiname (TXT):** Wo wurde der bereinigte Text gespeichert
- **Scraping-Zeitpunkt:** Wann wurde der Artikel erfasst
- **Text-Länge:** Anzahl Tokens/Wörter (für Analysen)
- **HTTP-Status:** War der Abruf erfolgreich

**Speicherformat (CSV):**
```csv
id,url,datum,titel,quelle,html_file,txt_file,scraped_at,n_tokens
12345,https://...,15.01.2024,Neuer Stadtrat gewählt,Rathaus,12345.html,12345.txt,2024-01-20,385
12344,https://...,14.01.2024,Haushalt beschlossen,Finanzen,12344.html,12344.txt,2024-01-20,412
```

**Code-Beispiel:**
```python
records = []

for tr in rows:
    cells = tr.find_all("td")
    if len(cells) < 3:
        continue
    
    datum = cells[0].get_text(strip=True)
    anchor = cells[1].find("a", href=True)
    if not anchor:
        continue
    
    titel = anchor.get_text(strip=True)
    relative_url = anchor["href"]
    quelle = cells[2].get_text(strip=True)
    
    # ID aus URL extrahieren
    uid = relative_url.split("/")[-1].split(".")[0]  # "12345"
    
    # Vollständige URL
    vollstaendige_url = urljoin(base_url, relative_url)
    
    # Metadaten sammeln
    records.append({
        'id': uid,
        'url': vollstaendige_url,
        'datum': datum,
        'titel': titel,
        'quelle': quelle,
        'html_file': f"{uid}.html",
        'txt_file': f"{uid}.txt"
    })

\```
# In CSV speichern
\``` python
import pandas as pd
df = pd.DataFrame(records)
df.to_csv('metadata.csv', index=False, encoding='utf-8')
```
````