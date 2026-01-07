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
        "question": "Was versteht man unter 'Operationalisierung' im Kontext der Digital Humanities? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Entwicklung eines Erkennungs- oder Messverfahrens für ein theoretisches Konzept",
                "correct": True,
                "feedback": """✓ Korrekt! Operationalisierung bezeichnet genau diesen Prozess:
                - Theoretische Konzepte werden messbar gemacht
                - Es wird ein konkretes Verfahren entwickelt
                - Dies ermöglicht empirische Überprüfung
                - Essentiell für quantitative Analysen"""
            },
            {
                "answer": "Die Brücke zwischen qualitativen Fragestellungen und quantitativen Methoden",
                "correct": True,
                "feedback": """✓ Korrekt! Die Operationalisierung ist tatsächlich diese Brücke:
                - Verbindet 'numbers' mit 'meaning'
                - Ermöglicht quantitative Analyse qualitativer Fragen
                - Zentral für Digital Humanities-Projekte
                - Macht geisteswissenschaftliche Konzepte messbar"""
            },
            {
                "answer": "Die technische Implementierung von Analysealgorithmen",
                "correct": False,
                "feedback": """× Nicht korrekt. Die technische Implementierung ist ein späterer Schritt:
                - Operationalisierung findet VOR der technischen Umsetzung statt
                - Sie definiert WAS gemessen werden soll
                - Die Implementierung beschäftigt sich mit dem WIE
                - Operationalisierung ist konzeptionelle Arbeit"""
            },
            {
                "answer": "Die Dokumentation der verwendeten Software und Tools",
                "correct": False,
                "feedback": """× Nicht korrekt. Dokumentation ist wichtig, aber nicht Operationalisierung:
                - Operationalisierung definiert Messverfahren
                - Dokumentation beschreibt die Umsetzung
                - Beides sind getrennte Schritte im Forschungsprozess
                - Operationalisierung ist konzeptionell, Dokumentation ist deskriptiv"""
            },
            {
                "answer": "Ein Prozess, der immer eindeutig und unstrittig ist",
                "correct": False,
                "feedback": """× Nicht korrekt. Operationalisierung ist diskutabel:
                - Verschiedene Operationalisierungen sind möglich
                - Die Wahl muss begründet und reflektiert werden
                - Grenzen und Beschränkungen müssen erkannt werden
                - Teil der wissenschaftlichen Reflexion"""
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
        "question": "Welche Aussagen zum Konzept der 'Leichten Sprache' und kommunikativen Barrierearmut sind korrekt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Leichte Sprache ist seit der Ratifizierung der UN-Behindertenrechtskonvention 2009 in Deutschland rechtlich relevant",
                "correct": True,
                "feedback": """✓ Korrekt! Die UN-Behindertenrechtskonvention:
                - Wurde 2009 in Deutschland ratifiziert
                - Ist verbindliches Recht
                - Beinhaltet Verpflichtung zur barrierefreien Kommunikation
                - Gab Leichter Sprache rechtliche Bedeutung"""
            },
            {
                "answer": "Kommunikative Barrierearmut ist ein binäres Konzept: Entweder eine Kommunikation ist barrierefrei oder nicht",
                "correct": False,
                "feedback": """× Nicht korrekt. Barrierearmut ist graduell:
                - Sprache kann mehr oder weniger verständlich sein
                - Es gibt verschiedene Grade der Komplexität
                - Nicht entweder-oder, sondern ein Kontinuum
                - Dies ermöglicht die Messung von Veränderungen"""
            },
            {
                "answer": "Leichte Sprache bezieht sich nur auf die Wortebene (z.B. Vermeidung von Fremdwörtern)",
                "correct": False,
                "feedback": """× Nicht korrekt. Leichte Sprache umfasst mehrere Ebenen:
                - Wortebene (gelaufige Wörter, keine Fremdwörter)
                - Satzebene (Verbalstil, einfache Strukturen)
                - Textebene (Gliederung, Zusammenfassungen)
                - Alle Ebenen tragen zur Verständlichkeit bei"""
            },
            {
                "answer": "Die gesellschaftliche Aufmerksamkeit für Leichte Sprache hat in den letzten Jahren zugenommen",
                "correct": True,
                "feedback": """✓ Korrekt! Dies zeigt sich beispielsweise:
                - In der Zunahme des Begriffs im Google Books-Korpus
                - In der Entwicklung von Regelwerken und Standards
                - In der DIN SPEC von März 2025
                - In vermehrten Angeboten von Behörden"""
            },
            {
                "answer": "Leichte Sprache betrifft ausschließlich Menschen mit Behinderungen",
                "correct": False,
                "feedback": """× Nicht korrekt. Leichte Sprache hat breitere Relevanz:
                - Betrifft Grundfragen gesellschaftlicher Teilhabe
                - Relevant für verschiedene Zielgruppen
                - Fördert allgemeine Verständlichkeit
                - Nicht auf eine Gruppe beschränkt"""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz )
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
        "question": "Welche Aussagen zu Lesbarkeitsindizes treffen zu? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Lesbarkeitsindizes nutzen häufig durchschnittliche Wortlänge und Satzlänge als Parameter",
                "correct": True,
                "feedback": """✓ Korrekt! Diese Parameter:
                - Sind zentral für viele Lesbarkeitsindizes
                - Lassen sich objektiv messen
                - Korrelieren mit Textkomplexität
                - Werden auch in der Leichte-Sprache-Forschung verwendet"""
            },
            {
                "answer": "Lesbarkeitsindizes erfassen alle Aspekte der Leichten Sprache vollständig",
                "correct": False,
                "feedback": """× Nicht korrekt. Lesbarkeitsindizes sind begrenzt:
                - Sie erfassen nur ausgewählte Indikatoren
                - Metaphern, Fremdwörter etc. werden oft nicht berücksichtigt
                - Textebene (Gliederung) ist schwer messbar
                - Die Operationalisierung wählt bewusst ein Set aus Indikatoren"""
            },
            {
                "answer": "Steigende Werte in Lesbarkeitsindizes bedeuten immer höhere Verständlichkeit",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Interpretation hängt vom Index ab:
                - Manche Indizes messen Komplexität (höher = schwieriger)
                - Andere messen Lesbarkeit (höher = leichter)
                - Die Interpretation muss jeweils definiert werden
                - In unserer Fallstudie: höhere Komplexität = weniger barrierefrei"""
            },
            {
                "answer": "Lesbarkeitsindizes ermöglichen die Messung zeitlicher Entwicklungen in Textkomplexität",
                "correct": True,
                "feedback": """✓ Korrekt! Dies ist zentral für unsere Fragestellung:
                - Quantitative Werte können über Zeit verglichen werden
                - Trends lassen sich statistisch erfassen
                - Veränderungen werden messbar
                - Grundlage für die Beantwortung unserer Forschungsfrage"""
            },
            {
                "answer": "Lesbarkeitsindizes sind die einzige Möglichkeit, Textkomplexität zu operationalisieren",
                "correct": False,
                "feedback": """× Nicht korrekt. Es gibt verschiedene Ansätze:
                - Lesbarkeitsindizes sind eine mögliche Operationalisierung
                - Andere Indikatoren wären denkbar (z.B. Fremdwortanteil)
                - Die Wahl muss begründet werden
                - Alternative Operationalisierungen sind legitim"""
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz )
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
        "question": "Welches der folgenden Kriterien war NICHT ausschlaggebend für die Wahl der Pressemitteilungen des Berliner Senats als Korpus?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Öffentliche Zugänglichkeit und maschinelle Aggregierbarkeit",
                "correct": False,
                "feedback": """× Dies war ein wichtiges Kriterium:
                - Pressemitteilungen sind online verfügbar
                - Systematisches Scraping ist möglich
                - Notwendig für den Korpusaufbau
                - Eines der vier definierten Kriterien"""
            },
            {
                "answer": "Funktion als Kommunikation der Behörden mit der Öffentlichkeit",
                "correct": False,
                "feedback": """× Dies war zentral für die Auswahl:
                - Pressemitteilungen sind öffentliche Kommunikation
                - Richten sich an Bürger:innen
                - Repräsentativ für Behördenkommunikation
                - Eines der vier definierten Kriterien"""
            },
            {
                "answer": "Homogenität der Textsorte",
                "correct": False,
                "feedback": """× Dies war ein wichtiges Kriterium:
                - Vermeidet Verzerrungen durch unterschiedliche Konventionen
                - Ermöglicht valide Vergleiche über Zeit
                - Pressemitteilungen folgen ähnlichen Mustern
                - Eines der vier definierten Kriterien"""
            },
            {
                "answer": "Maximale Länge der Einzeltexte",
                "correct": True,
                "feedback": """✓ Korrekt! Die Textlänge war KEIN definiertes Kriterium:
                - Die vier Kriterien waren: Zugänglichkeit, Kommunikationsfunktion, Homogenität, zeitliche Situierbarkeit
                - Textlänge spielt für die Analyse mit Lesbarkeitsindizes keine ausschlaggebende Rolle
                - Kurze und lange Texte können beide analysiert werden"""
            },
            {
                "answer": "Präzise zeitliche Situierbarkeit der Einzeltexte",
                "correct": False,
                "feedback": """× Dies war essentiell:
                - Pressemitteilungen haben klare Publikationsdaten
                - Ermöglicht Analyse zeitlicher Entwicklungen
                - Zentral für die Forschungsfrage
                - Eines der vier definierten Kriterien"""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz )
```

## Frage 5

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die folgenden Empfehlungen für Leichte Sprache der entsprechenden Ebene zu:",
    descriptions=[
        "Verwenden geläufiger Wörter, Vermeiden von Fremdwörtern",
        "Eher Verbalstil, Vermeiden von Negationen",
        "Klare Absatzgliederung, vorangestellte Zusammenfassung"
    ],
    options=["Wortebene", "Satzebene", "Textebene", "Dokumentebene"],
    correct_mapping={
        "Verwenden geläufiger Wörter, Vermeiden von Fremdwörtern": "Wortebene",
        "Eher Verbalstil, Vermeiden von Negationen": "Satzebene",
        "Klare Absatzgliederung, vorangestellte Zusammenfassung": "Textebene"
    }
)
```

## Frage 6

**Szenario:** Ein Forschungsteam möchte untersuchen, ob wissenschaftliche Zeitschriften in den letzten 20 Jahren verständlicher geworden sind. Sie planen, dies anhand von Abstracts zu untersuchen.

**Ihre Aufgabe:** Skizzieren Sie eine mögliche Operationalisierung dieser Fragestellung. Berücksichtigen Sie dabei:
1. Die Wahl des Korpus und Begründung
2. Die Auswahl geeigneter Messverfahren
3. Potenzielle Einschränkungen Ihrer Operationalisierung

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('research-question-1')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. Korpus:**
- Abstracts aus repräsentativen wissenschaftlichen Zeitschriften
- Zeitraum: 2005-2025 (20 Jahre)
- Auswahl nach Disziplinen (z.B. je 3-5 Zeitschriften pro Fachgebiet)
- Begründung: 
  - Abstracts sind homogene Textsorte
  - Zeitlich präzise datierbar
  - Öffentlich zugänglich
  - Repräsentativ für wissenschaftliche Kommunikation

**2. Messverfahren:**
- Lesbarkeitsindizes (z.B. Flesch Reading Ease, LIX)
- Durchschnittliche Wort- und Satzlänge
- Eventuell: Anteil an Fachwörtern (falls operationalisierbar)
- Begründung:
  - Objektiv messbar
  - Zeitliche Vergleiche möglich
  - Etablierte Verfahren

**3. Einschränkungen:**
- Lesbarkeitsindizes erfassen nicht alle Aspekte von Verständlichkeit
- Disziplinäre Unterschiede müssen berücksichtigt werden
- Abstracts repräsentieren nicht den gesamten Artikel
- Verständlichkeit ist kontextabhängig (Fachpublikum vs. Laien)
- Alternative Operationalisierungen wären möglich und legitim

**Wichtig:**
- Transparente Dokumentation der Entscheidungen
- Reflexion der Grenzen
- Begründung der Auswahlkriterien
````

## Frage 7

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Welche Aussagen zur Reflexion von Operationalisierungen in Digital Humanities-Projekten sind zutreffend? Wählen Sie alle korrekten Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Reflexion der Grenzen und Beschränkungen der eigenen Operationalisierung ist essentieller Bestandteil von DH-Projekten",
                "correct": True,
                "feedback": """✓ Korrekt! Wissenschaftliche Reflexion bedeutet:
                - Bewusstsein für die Grenzen der eigenen Methode
                - Transparente Dokumentation von Entscheidungen
                - Diskussion alternativer Ansätze
                - Teil der wissenschaftlichen Integrität"""
            },
            {
                "answer": "Jede Operationalisierung ist diskutabel und könnte auch anders erfolgen",
                "correct": True,
                "feedback": """✓ Korrekt! Dies ist wichtig zu verstehen:
                - Es gibt selten die eine 'richtige' Operationalisierung
                - Verschiedene Ansätze haben unterschiedliche Stärken
                - Die Wahl muss begründet werden
                - Wissenschaftlicher Diskurs ist erwünscht"""
            },
            {
                "answer": "Quantitative Methoden erfassen alle Aspekte qualitativer Phänomene vollständig",
                "correct": False,
                "feedback": """× Nicht korrekt. Dies ist eine wichtige Einsicht:
                - Quantifizierung bedeutet immer Reduktion
                - Nicht alle Aspekte sind messbar
                - Qualitative Dimensionen können verloren gehen
                - Deshalb ist Reflexion so wichtig"""
            },
            {
                "answer": "Die Operationalisierung sollte nur dann reflektiert werden, wenn die Ergebnisse unerwartet sind",
                "correct": False,
                "feedback": """× Nicht korrekt. Reflexion ist immer notwendig:
                - Unabhängig von den Ergebnissen
                - Teil des Forschungsprozesses von Anfang an
                - Stärkt die wissenschaftliche Qualität
                - Ermöglicht informierte Interpretation"""
            },
            {
                "answer": "Eine gute Operationalisierung macht die Forschungsfrage für quantitative Analyse adressierbar",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist die Kernfunktion:
                - Verbindet qualitative Fragen mit quantitativen Methoden
                - Macht abstrakte Konzepte messbar
                - Ermöglicht empirische Überprüfung
                - 'From numbers to meaning'"""
            },
            {
                "answer": "Einschränkungen der Operationalisierung bedeuten, dass die Forschung wertlos ist",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Differenzierung:
                - Jede Operationalisierung hat Grenzen
                - Dies schmälert nicht den Wert der Forschung
                - Wichtig ist die bewusste Reflexion
                - Transparenz über Grenzen erhöht die wissenschaftliche Qualität"""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz )
```

## Frage 8

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die folgenden Schritte zur Operationalisierung der Forschungsfrage in die richtige Reihenfolge:",
    descriptions=[
        "Definition des Korpus",
        "Formulierung der Forschungsfrage",
        "Auswahl geeigneter Messverfahren",
        "Reflexion der Grenzen der Operationalisierung",
        "Definition des zu messenden Konzepts"
    ],
    options=["3", "1", "5", "2", "4"],
    correct_mapping={
        "Formulierung der Forschungsfrage": "1",
        "Definition des zu messenden Konzepts": "2",
        "Auswahl geeigneter Messverfahren": "3",
        "Definition des Korpus": "4",
        "Reflexion der Grenzen der Operationalisierung": "5"
    }
)
```

## Frage 9

**Kritische Reflexion:** Bewerten Sie die folgende Operationalisierung kritisch:

*"Um die Entwicklung der Barrierearmut in der Behördenkommunikation zu untersuchen, werden alle Texte der Berliner Senatsverwaltung aus den letzten 50 Jahren gesammelt und mit einem einzelnen Lesbarkeitsindex analysiert. Wenn der Index niedriger wird, ist die Kommunikation barriereärmer geworden."*

**Ihre Aufgabe:** Identifizieren Sie mindestens vier problematische Aspekte dieser Operationalisierung und schlagen Sie Verbesserungen vor.

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('research-question-2')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung - Problematische Aspekte und Verbesserungsvorschläge:**

**1. "Alle Texte" - zu heterogen:**
- Problem: Verschiedene Textsorten (Pressemitteilungen, Formulare, Berichte) haben unterschiedliche Konventionen
- Verbesserung: Beschränkung auf eine homogene Textsorte (z.B. nur Pressemitteilungen)
- Begründung: Vermeidet Verzerrungen durch Textsorten-Konventionen

**2. "50 Jahre" - praktisch problematisch:**
- Problem: Digitale Verfügbarkeit für ältere Texte unklar, sehr großes Datenvolumen
- Verbesserung: Fokussierung auf einen relevanten, gut dokumentierten Zeitraum (z.B. seit 2011)
- Begründung: Praktikabilität und Nachvollziehbarkeit

**3. "Einzelner Lesbarkeitsindex" - zu eng:**
- Problem: Ein Index erfasst nur ausgewählte Aspekte der Komplexität
- Verbesserung: Verwendung mehrerer Indizes zur Triangulation
- Begründung: Robustere Ergebnisse, umfassendere Erfassung

**4. "Niedriger = barriereärmer" - zu simpel:**
- Problem: 
  - Interpretation hängt vom spezifischen Index ab
  - Kausale Schlussfolgerung ohne Begründung
  - Keine Reflexion alternativer Erklärungen
- Verbesserung: 
  - Klare Definition der Interpretation für den gewählten Index
  - Vorsichtige Formulierung (Korrelation, nicht Kausalität)
  - Diskussion möglicher Störfaktoren

**5. Fehlende Reflexion:**
- Problem: Keine Diskussion der Grenzen und alternativen Ansätze
- Verbesserung: Explizite Reflexion über:
  - Was erfasst wird und was nicht
  - Welche Annahmen getroffen werden
  - Welche alternativen Operationalisierungen möglich wären
  - Welche Einschränkungen die Interpretation beeinflussen

**Allgemeine Verbesserung:**
Eine wissenschaftlich fundierte Operationalisierung sollte transparent, begründet und reflektiert sein, mit klaren Kriterien für Korpusauswahl und Messmethodik.
````

## Frage 10

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question10 = [
    {
        "question": """Ein Forschungsteam möchte untersuchen, ob sich die "Emotionalität" politischer Reden im Bundestag über die Zeit verändert hat. Welche der folgenden Operationalisierungen wäre am sinnvollsten?""",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Auszählen aller Wörter mit Ausrufezeichen in den Protokollen",
                "correct": False,
                "feedback": """× Zu eng gefasst:
                - Erfasst nur einen sehr spezifischen Aspekt
                - Interpunktion ist nicht immer zuverlässig transkribiert
                - Emotionalität äußert sich vielfältiger
                - Würde wichtige Dimensionen übersehen"""
            },
            {
                "answer": "Verwendung von Sentimentanalyse-Tools zur Messung positiver/negativer Emotionen und Analyse emotionaler Wörter",
                "correct": True,
                "feedback": """✓ Gute Operationalisierung, weil:
                - Sentimentanalyse ist etabliertes Verfahren
                - Erfasst verschiedene emotionale Dimensionen
                - Quantitativ messbar und vergleichbar über Zeit
                - Kann durch weitere Indikatoren ergänzt werden
                - Trotzdem: Grenzen müssen reflektiert werden (z.B. Kontextabhängigkeit, Ironie)"""
            },
            {
                "answer": "Befragung von Politiker:innen, wie emotional sie ihre Reden empfinden",
                "correct": False,
                "feedback": """× Nicht für diese Fragestellung geeignet:
                - Subjektive Einschätzungen statt objektiver Messung
                - Retrospektive Befragung über lange Zeiträume unmöglich
                - Keine Vergleichbarkeit über Jahrzehnte
                - Passt nicht zum quantitativen Methodenparadigma der Korpusanalyse"""
            },
            {
                "answer": "Zählen der Zwischenrufe und Reaktionen im Protokoll",
                "correct": False,
                "feedback": """× Misst etwas anderes:
                - Erfasst Reaktionen des Publikums, nicht Emotionalität der Rede selbst
                - Protokollierung von Zwischenrufen kann sich über Zeit ändern
                - Nur indirekter Indikator
                - Könnte ergänzend interessant sein, aber nicht als Hauptoperationalisierung"""
            },
            {
                "answer": "Messung der Lautstärke in Audioaufnahmen",
                "correct": False,
                "feedback": """× Praktisch problematisch:
                - Audioaufnahmen nicht für alle Zeiträume verfügbar
                - Aufnahmequalität variiert stark
                - Lautstärke ≠ Emotionalität
                - Technische statt inhaltliche Messung"""
            }
        ]
    }
]
display_quiz(question10, colors=colors.jupyterquiz )
```