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
        "question": "Welche Aussagen über Parameter auf Wortebene zur Berechnung der Textkomplexität sind korrekt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Anzahl der Buchstaben auf 100 Wörter berücksichtigt die Gleichverteilung der Textschwierigkeit",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtige Differenzierung:
                - Nicht nur absolute Wortlänge
                - Text wird in Abschnitte unterteilt
                - Misst Konsistenz der Schwierigkeit
                - Verwendet im Coleman-Liau-Index
                - Unterscheidet sich von einfacher durchschnittlicher Wortlänge"""
            },
            {
                "answer": "Wörter mit mehr als drei Silben gelten in den meisten Indizes als schwer",
                "correct": True,
                "feedback": """✓ Korrekt! Standard-Schwellenwert:
                - 1-2 Silben = leicht
                - 3+ Silben = schwer
                - Verwendet in Wiener Sachtextformel
                - Sprachabhängig (Silbentrennung)
                - Wichtiger Parameter für Komplexität"""
            },
            {
                "answer": "Die absolute Wortlänge in Buchstaben ist aussagekräftiger als die Silbenzahl",
                "correct": False,
                "feedback": """× Nicht generell korrekt. Wichtige Unterscheidung:
                - Beide haben Vor- und Nachteile
                - Silbenzahl: Sprachabhängig, näher an Aussprache
                - Buchstabenzahl: Sprachunabhängig, einfacher zu berechnen
                - ARI nutzt Buchstaben, Flesch nutzt Silben
                - Keine klare Überlegenheit"""
            },
            {
                "answer": "Schwierige Wörter werden immer über ein vordefiniertes Wörterbuch ermittelt, nie über Wortlänge oder Silbenzahl",
                "correct": False,
                "feedback": """× Nicht korrekt. Verschiedene Ansätze:
                - Wiener Sachtextformel: Wörterbuch-basiert
                - Andere Indizes: Über Länge/Silben
                - Beide Methoden existieren parallel
                - Wörterbuch ist EIN Ansatz, nicht der einzige"""
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
        "question": "Welche Aussagen über Parameter auf Satzebene zur Berechnung der Textkomplexität sind korrekt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Anzahl der Sätze auf 100 Wörter ist ein indirektes Maß für die Satzlänge",
                "correct": True,
                "feedback": """✓ Korrekt! Clevere Umkehrung:
                - Mehr Sätze pro 100 Wörter = kürzere Sätze
                - Weniger Sätze pro 100 Wörter = längere Sätze
                - Verwendet im Coleman-Liau-Index
                - Normalisierung ermöglicht Vergleichbarkeit
                - Alternative Perspektive zur direkten Satzlänge"""
            },
            {
                "answer": "Der Durchschnitt wird berechnet, indem man die Längen aller Sätze summiert und durch die Anzahl der Sätze teilt",
                "correct": True,
                "feedback": """✓ Korrekt! Standardberechnung:
                - Summe aller Satzlängen / Anzahl Sätze
                - Glättet Extremwerte
                - Repräsentativer Wert für gesamten Text
                - Verwendet in Flesch, Wiener, ARI
                - Basis für die meisten Berechnungen"""
            },
            {
                "answer": "Kürzere Sätze führen immer zu einem niedrigeren Textkomplexitätsscore in allen Indizes",
                "correct": False,
                "feedback": """× Nicht präzise genug. Wichtige Nuance:
                - Richtung hängt vom Index ab
                - Flesch: Höherer Score = leichter (kürzere Sätze)
                - Wiener/ARI: Niedrigerer Score = leichter (kürzere Sätze)
                - Nicht einheitlich über alle Indizes
                - Die Beziehung ist konsistent, aber Skalen unterscheiden sich"""
            },
            {
                "answer": "Die maximale Satzlänge im Text ist wichtiger als die durchschnittliche Satzlänge",
                "correct": False,
                "feedback": """× Nicht korrekt. Standard-Praxis:
                - Durchschnitt ist der Standard-Parameter
                - Maximum würde Verzerrung erzeugen
                - Einzelner langer Satz = nicht repräsentativ
                - Indizes verwenden durchschnittliche Werte
                - Robuster gegenüber Ausreißern"""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz)
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Lesbarkeitsindizes den passenden Beschreibungen zu:",
    descriptions=[
        "Am weitesten verbreitet, operiert auf Satzlänge und Silbenanzahl",
        "Speziell für deutsche Sachtexte entwickelt, nutzt schwierige Wörter",
        "Operiert rein auf Längenmaßen (Zeichen, Wörter, Sätze)",
        "Basiert auf Buchstaben und Sätzen pro 100 Wörter"
    ],
    options=["Flesch-Lesbarkeitsindex", "Wiener Sachtextformel", "Automated Readability Index (ARI)", "Coleman-Liau-Index", "SMOG-Index"],
    correct_mapping={
        "Am weitesten verbreitet, operiert auf Satzlänge und Silbenanzahl": "Flesch-Lesbarkeitsindex",
        "Speziell für deutsche Sachtexte entwickelt, nutzt schwierige Wörter": "Wiener Sachtextformel",
        "Operiert rein auf Längenmaßen (Zeichen, Wörter, Sätze)": "Automated Readability Index (ARI)",
        "Basiert auf Buchstaben und Sätzen pro 100 Wörter": "Coleman-Liau-Index"
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
        "question": "Was ist die korrekteste Aussage über die Interpretation von Lesbarkeitsindizes?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die meisten Scores lassen sich in eine Klassenstufe oder Bildungsniveau übersetzen, wobei ein niedriger Score meist einen schweren Text und ein hoher Score einen leichten Text bedeutet",
                "correct": False,
                "feedback": """× Teilweise korrekt, aber umgekehrt! Wichtige Korrektur:
                - Niedriger Score = leichter Text (bei den meisten Indizes)
                - Hoher Score = schwerer Text
                - Flesch kann je nach Version variieren
                - Die Richtung ist entscheidend!"""
            },
            {
                "answer": "Die meisten Scores lassen sich in eine Klassenstufe übersetzen, und ein niedriger Score bedeutet meist einen leichten Text",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist die Standardinterpretation:
                - Niedriger Score = leichter Text
                - Hoher Score = schwerer Text
                - Klassenstufen-Zuordnung (z.B. 5. Klasse bis Uni)
                - Praktisch für Zielgruppenbestimmung
                - Wichtig: Skalen unterscheiden sich zwischen Indizes!"""
            },
            {
                "answer": "Alle Lesbarkeitsindizes verwenden dieselbe Skala von 0-100, was den Vergleich erleichtert",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtiger Hinweis:
                - Unterschiedliche Skalen: Flesch (0-180), Wiener (4-15), ARI (1-14+)
                - NICHT direkt vergleichbar
                - Wichtig für korrekte Interpretation
                - Jeder Index hat eigene Normierung"""
            },
            {
                "answer": "Höhere Textkomplexität bedeutet immer bessere Textqualität, unabhängig von der Zielgruppe",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Differenzierung:
                - Komplexität ≠ Qualität
                - Zielgruppenabhängig
                - Barrierefreiheit erfordert oft niedrige Komplexität
                - Einfache Texte können hochwertig sein"""
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

question6 = [
    {
        "question": "Was ist der Hauptvorteil von Liniendiagrammen gegenüber Balkendiagrammen für die Darstellung zeitlicher Entwicklungen?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Liniendiagramme zeigen Häufigkeiten in diskreten Zeitintervallen besser",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist tatsächlich umgekehrt:
                - Balkendiagramme: Gut für diskrete Intervalle
                - Liniendiagramme: Besser für kontinuierliche Entwicklungen
                - Häufigkeiten in Intervallen → Balken besser geeignet
                - Zeitliche Trends → Linien besser geeignet"""
            },
            {
                "answer": "Liniendiagramme ermöglichen die bessere Erkennung von Trends und Mustern über Zeit, da die Verbindung zwischen Zeitpunkten visualisiert wird",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist der zentrale Vorteil:
                - Kontinuität wird sichtbar gemacht
                - Trends leicht erkennbar (steigend/fallend)
                - Minima und Maxima deutlich
                - Verbindungslinien zeigen Entwicklung
                - Ideal für diachrone Analysen"""
            },
            {
                "answer": "Liniendiagramme können keine Zeitachse auf der X-Achse darstellen",
                "correct": False,
                "feedback": """× Nicht korrekt. Im Gegenteil:
                - X-Achse wird typisch für Zeit verwendet
                - Natürliche chronologische Darstellung
                - Verschiedene Zeiteinheiten möglich
                - Standard für Zeitreihen"""
            },
            {
                "answer": "Liniendiagramme zeigen einzelne Datenpunkte genauer als Balkendiagramme",
                "correct": False,
                "feedback": """× Nicht der Hauptvorteil. Wichtig:
                - Beide zeigen Datenpunkte
                - Genauigkeit ist ähnlich
                - Der Hauptvorteil liegt in der Trendvisualisierung
                - Verbindungslinien = zentrales Element"""
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz)
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Wie wird eine diachrone Analyse der Textkomplexität durchgeführt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Textkomplexität wird für jede Pressemitteilung einzeln berechnet",
                "correct": True,
                "feedback": """✓ Korrekt! Individuelle Berechnung:
                - Jeder Text erhält eigenen Score
                - Basis für weitere Aggregation
                - Ermöglicht detaillierte Analyse
                - Notwendiger erster Schritt"""
            },
            {
                "answer": "Die Werte werden dann über Zeiteinheiten akkumuliert (z.B. Wochen, Monate, Jahre)",
                "correct": True,
                "feedback": """✓ Korrekt! Zeitliche Aggregation:
                - Gruppierung nach Zeitabschnitten
                - Unterschiedliche Granularität möglich
                - Glättung von Einzelausreißern
                - Erkennung von Mustern"""
            },
            {
                "answer": "Für jede Zeiteinheit wird der Durchschnitt der Textkomplexitätsmaße berechnet",
                "correct": True,
                "feedback": """✓ Korrekt! Durchschnittsbildung:
                - Repräsentativer Wert pro Zeiteinheit
                - Vergleichbarkeit zwischen Perioden
                - Reduziert Rauschen
                - Basis für Visualisierung"""
            },
            {
                "answer": "Nur der höchste Wert jeder Zeiteinheit wird betrachtet",
                "correct": False,
                "feedback": """× Nicht korrekt. Durchschnitt vs. Maximum:
                - Durchschnitt ist repräsentativer
                - Nur Maximum würde Verzerrung erzeugen
                - Alle Werte sollten berücksichtigt werden
                - Standard ist Mittelwertbildung"""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz)
```

## Frage 7

**Szenario:** Sie analysieren ein Korpus von Zeitungsartikeln aus den Jahren 2010-2024. Nach Berechnung des Flesch-Index und Visualisierung in einem Liniendiagramm stellen Sie fest:
- 2010-2015: Scores zwischen 70-75 (mittelschwer)
- 2015-2020: Scores zwischen 60-65 (durchschnittlich)  
- 2020-2024: Scores zwischen 50-55 (anspruchsvoll)

**Aufgaben:**
1. Wie interpretieren Sie diese Entwicklung?
2. Was könnte diese Entwicklung für die Barrierefreiheit der Texte bedeuten?
3. Welche weiteren Analysen würden Sie vorschlagen?
4. Würden Sie dieselbe Entwicklung auch mit anderen Lesbarkeitsindizes überprüfen? Warum?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('corpus-analysis-2')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. Interpretation der Entwicklung:**

Die Daten zeigen einen **klaren Abwärtstrend** der Flesch-Scores über 14 Jahre:
- **2010-2015:** 70-75 (mittelschwer, 7.-8. Klasse)
- **2015-2020:** 60-65 (durchschnittlich, 8.-9. Klasse)
- **2020-2024:** 50-55 (anspruchsvoll, 10.-12. Klasse)

**Interpretation:**
- **Steigende Textkomplexität** über die Zeit
- Durchschnittlich ca. 5 Punkte pro 5-Jahres-Periode
- Von Mittelstufen- zu Oberstufen-Niveau
- **Kontinuierlicher Trend**, keine sprunghaften Veränderungen

**Mögliche Ursachen:**
- Zunehmende Fachsprache
- Längere Sätze und komplexere Satzstrukturen
- Mehr mehrsilbige Wörter
- Thematische Verschiebungen (komplexere Themen?)

---

**2. Bedeutung für die Barrierefreiheit:**

**Negative Entwicklung für Barrierefreiheit:**

- **Abnehmende Zugänglichkeit:** Texte werden schwerer verständlich
- **Kleinere Zielgruppe:** Von breiter Öffentlichkeit (7.-8. Klasse) zu gebildeteren Lesern (10.-12. Klasse)
- **Barrieren steigen:** 
  - Für Menschen mit Lernschwierigkeiten
  - Für Menschen mit geringer formaler Bildung
  - Für Nicht-Muttersprachler
  - Für jüngere Leser

**Konsequenzen:**
- **Informationszugang** wird eingeschränkt
- **Demokratische Teilhabe** erschwert
- **Digitale Kluft** könnte vergrößert werden
- Widerspruch zu Zielen der **Leichten/Einfachen Sprache**

**Empfehlungen:**
- Bewusste Vereinfachung anstreben
- Schulungen für Redakteure
- Style Guides für verständliche Sprache
- Parallele Versionen in Leichter Sprache

---

**3. Vorgeschlagene weitere Analysen:**

**A) Detailanalyse der Parameter:**
- Welche spezifischen Parameter treiben die Komplexität?
- Sind es hauptsächlich:
  - Längere Sätze? → Durchschnittliche Satzlänge über Zeit
  - Mehr Silben? → Silbenzahl pro Wort über Zeit
  - Schwierigere Wörter? → Anteil langer/schwieriger Wörter
- Dies hilft, gezielte Verbesserungen zu identifizieren

**B) Thematische Analyse:**
- Unterscheiden sich verschiedene Themenbereiche?
- Politik vs. Kultur vs. Verwaltung
- Korrelation zwischen Thema und Komplexität?

**C) Vergleich mit anderen Quellen:**
- Wie entwickelt sich die Komplexität bei anderen Zeitungen?
- Ist dies ein allgemeiner Trend oder spezifisch?
- Benchmarking mit Qualitäts- vs. Boulevardzeitungen

**D) Saisonale/zyklische Muster:**
- Gibt es wiederkehrende Muster?
- Wahljahre komplexer?
- Ferienzeiten einfacher?

**E) Autorschaft:**
- Unterschiede zwischen Redakteuren?
- Ressorts mit konsistent höherer/niedrigerer Komplexität?

---

**4. Überprüfung mit anderen Indizes:**

**JA, definitiv!** Und zwar aus folgenden Gründen:

**Validierung der Ergebnisse:**
- **Flesch-Index allein** könnte Artefakt sein
- **Mehrere Indizes** erhöhen Vertrauenswürdigkeit
- Wenn alle Indizes denselben Trend zeigen → starke Evidenz
- Wenn Indizes divergieren → weitere Untersuchung nötig

**Unterschiedliche Perspektiven:**
- **Flesch:** Silben + Satzlänge
- **Wiener Sachtextformel:** Schwierige Wörter + Satzlänge
- **ARI:** Reine Längenmaße
- **Coleman-Liau:** Buchstaben pro 100 Wörter
- Jeder Index betont andere Aspekte

**Robustheit:**
- Nicht alle Indizes messen exakt dasselbe
- Konvergenz mehrerer Indizes = robuster Befund
- Divergenz = differenzierteres Bild

**Praktische Durchführung:**
```python
# Alle vier Indizes berechnen
df['flesch'] = df['text'].apply(calculate_flesch)
df['wiener'] = df['text'].apply(calculate_wiener)
df['ari'] = df['text'].apply(calculate_ari)
df['coleman_liau'] = df['text'].apply(calculate_coleman_liau)

# Zeitliche Entwicklung für alle
for measure in ['flesch', 'wiener', 'ari', 'coleman_liau']:
    plot_over_time(df, measure)
```

**Erwartung:**
- **Alle Indizes sollten** sinkende Lesbarkeit zeigen (steigenden Score bei den meisten)
- **Stärke des Trends** könnte variieren
- **Interpretation** wird durch Konvergenz gestützt

---

**Zusammenfassung:**

Die Analyse zeigt eine problematische Entwicklung hinsichtlich Barrierefreiheit. Eine umfassende Validierung mit multiplen Indizes und tiefergehende Analysen der Ursachen sind empfehlenswert, um fundierte Empfehlungen für barriereärmere Kommunikation zu geben.
````