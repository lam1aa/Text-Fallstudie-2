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
        "question": "Welche Komponenten sind an einem HTTP-Request beteiligt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Der Client sendet eine Anfrage an den Server",
                "correct": True,
                "feedback": """✓ Korrekt! Der Client:
                - Ist Ihr Computer oder Browser
                - Initiiert die Kommunikation
                - Sendet den HTTP-Request
                - Wartet auf die Antwort des Servers"""
            },
            {
                "answer": "Die URL (Uniform Resource Locator) spezifiziert die gewünschte Ressource",
                "correct": True,
                "feedback": """✓ Korrekt! Die URL:
                - Ist die Webadresse
                - Enthält Protokoll, Domain, Pfad und ggf. Parameter
                - Identifiziert die angeforderte Ressource
                - Beispiel: https://www.berlin.de/rbmskzl/"""
            },
            {
                "answer": "Die Request-Methode (z.B. GET oder POST) gibt an, welche Aktion erwartet wird",
                "correct": True,
                "feedback": """✓ Korrekt! Die Request-Methode:
                - GET: Daten anfordern ohne Veränderung
                - POST: Daten an den Server senden
                - Definiert die Art der Anfrage
                - Wichtig für die Server-Verarbeitung"""
            },
            {
                "answer": "Der Server ist derjenige, der die Anfrage stellt",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Unterscheidung:
                - Der CLIENT stellt die Anfrage
                - Der SERVER empfängt die Anfrage
                - Der Server antwortet dann mit einer Response
                - Client und Server haben unterschiedliche Rollen"""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz   )
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
        "question": "Was ist der Unterschied zwischen einem GET- und einem POST-Request? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "GET-Requests fordern Daten an, ohne sie zu verändern",
                "correct": True,
                "feedback": """✓ Korrekt! GET-Requests:
                - Nur Daten abrufen
                - Keine Veränderungen am Server
                - Vergleichbar mit einem Katalog bestellen
                - Standard für Webseiten-Aufrufe"""
            },
            {
                "answer": "POST-Requests senden Daten an den Server",
                "correct": True,
                "feedback": """✓ Korrekt! POST-Requests:
                - Übermitteln Daten zum Server
                - Z.B. Formulardaten, Login-Informationen
                - Vergleichbar mit ausgefülltes Formular zurücksenden
                - Daten sind nicht in der URL sichtbar"""
            },
            {
                "answer": "GET-Requests sind in der URL sichtbar, POST-Requests nicht",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtiger Unterschied:
                - GET: Parameter in der URL (z.B. ?suche=Begriff)
                - POST: Daten im Request-Body
                - Sicherheitsaspekt bei sensiblen Daten
                - POST besser für Passwörter etc."""
            },
            {
                "answer": "GET und POST sind völlig identisch in ihrer Funktion",
                "correct": False,
                "feedback": """× Nicht korrekt. Sie haben unterschiedliche Zwecke:
                - GET: Daten abrufen
                - POST: Daten senden
                - Verschiedene Anwendungsfälle
                - Unterschiedliche Sicherheitsaspekte"""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz   )
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die HTTP-Statuscodes den richtigen Bedeutungen zu:",
    descriptions=[
        "Anfrage erfolgreich, hier sind die gewünschten Daten",
        "Die angeforderte Seite existiert nicht",
        "Zugriff verweigert",
        "Interner Server-Fehler"
    ],
    options=["200 (OK)", "404 (Not Found)", "403 (Forbidden)", "500 (Internal Server Error)", "301 (Moved Permanently)"],
    correct_mapping={
        "Anfrage erfolgreich, hier sind die gewünschten Daten": "200 (OK)",
        "Die angeforderte Seite existiert nicht": "404 (Not Found)",
        "Zugriff verweigert": "403 (Forbidden)",
        "Interner Server-Fehler": "500 (Internal Server Error)"
    }
)
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
        "question": "Welche Komponenten enthält eine HTTP-Response? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Einen Statuscode zur Information über den Erfolg der Anfrage",
                "correct": True,
                "feedback": """✓ Korrekt! Der Statuscode:
                - Informiert über Erfolg oder Misserfolg
                - Dreistellige Zahl (z.B. 200, 404)
                - Erste Stelle gibt Kategorie an
                - Ermöglicht Fehlerbehandlung"""
            },
            {
                "answer": "Einen Response-Header mit Metainformationen über die Antwort",
                "correct": True,
                "feedback": """✓ Korrekt! Der Response-Header:
                - Enthält Metainformationen
                - Z.B. Content-Type, Datum, Server-Info
                - Wichtig für die Verarbeitung
                - Nicht der eigentliche Inhalt"""
            },
            {
                "answer": "Einen Response-Body mit dem eigentlichen Inhalt",
                "correct": True,
                "feedback": """✓ Korrekt! Der Response-Body:
                - Enthält den eigentlichen Inhalt
                - Meist HTML-Code für Webseiten
                - Kann auch Bilder, JSON, PDFs sein
                - Was Sie tatsächlich sehen möchten"""
            },
            {
                "answer": "Die URL der nächsten zu besuchenden Seite",
                "correct": False,
                "feedback": """× Nicht standardmäßig. Die Response:
                - Enthält die angeforderten Daten
                - Keine automatische nächste URL
                - Links können im HTML-Body sein
                - Aber nicht als Standard-Komponente"""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz   )
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
        "question": "Was ist der Unterschied zwischen statischen und dynamischen Websites? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Statische Websites sind fertige Dokumente, die unverändert vom Server gesendet werden",
                "correct": True,
                "feedback": """✓ Korrekt! Statische Websites:
                - Liegen fertig vor
                - Werden unverändert gesendet
                - Wie ein Buch aus der Bibliothek
                - Alle Inhalte im HTML-Code"""
            },
            {
                "answer": "Dynamische Websites werden erst bei der Anfrage zusammengestellt",
                "correct": True,
                "feedback": """✓ Korrekt! Dynamische Websites:
                - Werden on-demand erstellt
                - Oft mit JavaScript
                - Inhalte werden nachgeladen
                - Wie ein Koch, der auf Bestellung kocht"""
            },
            {
                "answer": "Statische Websites können leicht mit einfachen Scraping-Methoden extrahiert werden",
                "correct": True,
                "feedback": """✓ Korrekt! Vorteil für Scraping:
                - Alle Inhalte direkt im HTML
                - Einfaches requests reicht oft
                - Kein Browser nötig
                - Schneller und einfacher"""
            },
            {
                "answer": "Dynamische Websites benötigen keine speziellen Scraping-Methoden",
                "correct": False,
                "feedback": """× Nicht korrekt. Dynamische Websites:
                - Benötigen fortgeschrittene Methoden
                - Oft Selenium erforderlich
                - Browser-Simulation nötig
                - JavaScript muss ausgeführt werden"""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz   )
```

## Frage 6


```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Python-Bibliotheken für Web Scraping den passenden Beschreibungen zu:",
    descriptions=[
        "Einfache HTTP-Anfragen für einzelne statische Webseiten",
        "Effizientes Crawlen und Folgen von Links über mehrere Seiten",
        "Simulation von Benutzerinteraktionen und Ausführung von JavaScript"
    ],
    options=["requests", "scrapy", "selenium", "beautifulsoup"],
    correct_mapping={
        "Einfache HTTP-Anfragen für einzelne statische Webseiten": "requests",
        "Effizientes Crawlen und Folgen von Links über mehrere Seiten": "scrapy",
        "Simulation von Benutzerinteraktionen und Ausführung von JavaScript": "selenium"
    }
)
```

## Frage 7

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Welche Aussagen zu den Vor- und Nachteilen der Scraping-Methode 'requests' treffen zu? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Einfach zu implementieren und geringer Ressourcenverbrauch",
                "correct": True,
                "feedback": """✓ Korrekt! Vorteile von requests:
                - Sehr einfache Syntax
                - Wenig Rechenleistung nötig
                - Schnell
                - Gut für Einsteiger"""
            },
            {
                "answer": "Ausreichend für einfache Scraping-Aufgaben mit statischen Seiten",
                "correct": True,
                "feedback": """✓ Korrekt! Anwendungsbereich:
                - Perfekt für statische Seiten
                - Einzelne Seiten abrufen
                - Wenn HTML direkt verfügbar ist
                - Keine komplexen Interaktionen"""
            },
            {
                "answer": "Kann automatisch Links folgen und mehrere Seiten durchsuchen",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist ein Nachteil:
                - Nur einzelne Seiten
                - Keine automatische Navigation
                - Für mehrere Seiten: scrapy besser
                - Manuelle Programmierung nötig"""
            },
            {
                "answer": "Geeignet für dynamisch generierte Inhalte mit JavaScript",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist ein Nachteil:
                - Nur statische Inhalte
                - JavaScript wird nicht ausgeführt
                - Für dynamische Inhalte: selenium nötig
                - Sieht nur den ursprünglichen HTML-Code"""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz   )
```

## Frage 8

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8 = [
    {
        "question": "Wann sollte man Selenium anstelle von requests oder scrapy verwenden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Wenn Inhalte dynamisch mittels JavaScript geladen werden",
                "correct": True,
                "feedback": """✓ Korrekt! Selenium ist nötig für:
                - JavaScript-generierte Inhalte
                - Dynamisches Nachladen
                - Interaktive Elemente
                - Single Page Applications"""
            },
            {
                "answer": "Wenn Benutzerinteraktionen simuliert werden müssen (z.B. Klicken, Scrollen)",
                "correct": True,
                "feedback": """✓ Korrekt! Selenium kann:
                - Buttons klicken
                - Formulare ausfüllen
                - Scrollen
                - Wie ein menschlicher Nutzer agieren"""
            },
            {
                "answer": "Wenn man eine einfache statische Webseite abrufen möchte",
                "correct": False,
                "feedback": """× Nicht optimal. Für statische Seiten:
                - requests ist ausreichend
                - Selenium wäre overkill
                - Zu ressourcenintensiv
                - Zu langsam für einfache Aufgaben"""
            },
            {
                "answer": "Wenn Geschwindigkeit und geringer Ressourcenverbrauch wichtig sind",
                "correct": False,
                "feedback": """× Nicht korrekt. Selenium:
                - Ist deutlich langsamer
                - Benötigt mehr Ressourcen
                - Startet einen echten Browser
                - Für Geschwindigkeit: requests oder scrapy"""
            }
        ]
    }
]
display_quiz(question8, colors=colors.jupyterquiz   )
```

## Frage 9

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question10 = [
    {
        "question": "Welche ethischen und rechtlichen Aspekte müssen beim Web Scraping beachtet werden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die robots.txt-Datei einer Website sollte beachtet werden",
                "correct": True,
                "feedback": """✓ Korrekt! Die robots.txt:
                - Gibt Scraping-Richtlinien vor
                - Zeigt, welche Bereiche erlaubt sind
                - Sollte respektiert werden
                - Liegt meist unter example.com/robots.txt"""
            },
            {
                "answer": "Angemessene Wartezeiten zwischen Anfragen sollten eingehalten werden",
                "correct": True,
                "feedback": """✓ Korrekt! Wartezeiten:
                - Vermeiden Serverüberlastung
                - Zeigen respektvolles Verhalten
                - Typisch: 1-2 Sekunden zwischen Requests
                - Verhindert, als Angriff wahrgenommen zu werden"""
            },
            {
                "answer": "Persönliche Daten dürfen ohne Einwilligung gesammelt werden, wenn sie öffentlich sind",
                "correct": False,
                "feedback": """× Nicht korrekt! Datenschutz beachten:
                - Auch öffentliche Daten unterliegen Datenschutz
                - DSGVO muss beachtet werden
                - Einwilligung oft erforderlich
                - Besondere Vorsicht bei personenbezogenen Daten"""
            },
            {
                "answer": "Urheberrecht und Nutzungsbedingungen der Websites müssen beachtet werden",
                "correct": True,
                "feedback": """✓ Korrekt! Rechtliche Aspekte:
                - Urheberrecht gilt auch im Web
                - Terms of Service lesen
                - Nicht jede öffentliche Information darf genutzt werden
                - Bei Unsicherheit: rechtliche Beratung einholen"""
            }
        ]
    }
]
display_quiz(question10, colors=colors.jupyterquiz   )
```