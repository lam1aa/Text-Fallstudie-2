(corpus-analysis_text_complexity)=
# Textkomplexität und Visualisierung
```{admonition} Feinlernziel(e) dieses Kapitels
* Sie können die Textmaße (Wortlänge, Satzlänge etc.), die zur Berechnung der Textkomplexität dienen, aufzählen.
* Sie kennen verschiedene Methoden zur Berechnung der Textkomplexität und können die Vor- und Nachteile der Methoden aufzeigen.
* Sie können das Konzept eines Liniendiagramms erklären.
```

## 1. Forschungsfrage und Operationalisierung 

Wir gehen von folgender Forschungsfrage aus: 
`````{admonition} Forschungsfrage
:class: tip
Lässt sich eine Verminderung der sprachlichen Komplexität in der Kommunikation des Berliner Senats mit der Öffenlichkeit feststellen?
`````
Um diese mit quantitativen Methoden zu bearbeiten, wurde die Forschungsfrage zunächst wie folgt **operationalisiert**:
1. die **Kommunikation des Berliner Senats mit der Öffenlichkeit** wird durch das Korpus, bestehend aus Pressemitteilungen, erfasst
2. die **die sprachliche Komplexität** wird über Textkomplexitätsmaße errechnet
3. die **Verminderung** der Textkomplexität wird durch die sich über Zeit verändernde Textkomplexität untersucht.

## 2. Textkomplexitätsmaße

### 2.1 Was ist Textkomplexität
Aus psychologischer Sicht beschreibt Textkomplexität die Schwierigkeit, mit der ein Text für Lesende zu verstehen ist. {cite:p}`schnotz2010textverstehen` unterscheidet drei Repräsentationsebenen des Textverstehens:
1. die Ebene der Textoberfläche bezeichnet die sprachliche Komplexität (Satzlänge, Satzstruktur, Wortwahl)
2. die Ebene der Textbasis bezeichnet die semantische Komplexität (die Propositionen eines Texts und deren Zusammenhang)
3. die Ebene des mentalen Modell bezeichnet die mentale Repräsentation des im Text beschriebenen Sachverhalts, der auf Ebene 1 und 2 sowie auf Weltwissen der Lesenden aufbaut. 

Da wir eine computationelle Untersuchung anstreben und diese transparent und somit nachvollziehbar, also besser reproduzierbar sein sollte, beschränken wir die Analyse auf Ebene 1. Unser Untersuchungsgegenstand ist demnach die Textoberfläche und schließt semantische Komponenten aus. Etablierte Algorithmen (z.B. FLESCH) zur Berechnung der Textkomplexität oder Lesbarkeit, die auf der Textoberfläche arbeiten, benutzen eine Reihe von linguistischen Markern und errechnen daraus einen Score, der häufig auf Bildungsniveaus bzw. Jahrgangsstufen abgebildet wird. 
Mit Hilfe der Algorithmen kann die Komplexität von Texten verglichen und so z.B. festgestellt werden, welcher Text sich eignet, um in einer bestimmten Klassenstufe gelesen zu werden.

### 2.2 Linguistische Marker 
Zur Untersuchung der Textoberfläche lassen sich unterschiedliche linguistische Marker heranziehen. Die meisten Lesarbeitsindice basieren auf einer Kombination der folgenden Marker:

#### Wortebene
* **Länge** der Wörter:
  * wird errechnet durch Anzahl der Buchstaben
  * Annahme: Je weniger lange Wörter ein Text enthält, desto leichter ist der Text zu verstehen. 
* Anzahl der Buchstaben auf 100 Wörter:
  * Ähnlich zur Wortlänge, allerdings wird der Text bei dieser Methode in Abschnitte unterteilt, das heißt es wird einbezogen, ob der Text gleichmäßig kompliziert ist oder nicht.
  * Berechnung: Zählen von 100 Wörtern → Zählen der Buchstaben
  * Annahme: Je weniger Buchstaben, desto kürzer sind die Wörter, desto leichter ist der Text zu verstehen.
* **Anzahl der Silben** eines Wortes:
  * wird errechnet, indem das Wort zuerst in Silben aufgeteilt wird und dann die Silben gezählt werden. Die Silbentrennung ist sprachspezifisch.
  * Annahme: Je weniger Wörter mit vielen Siblen ein Text enthält, desto leichter ist der Text zu verstehen. Wörter mit ein oder zwei Silben gelten als leicht, Wörter mit mehr als drei Silben gelten als schwer.
* Anzahl **schwierige Wörter**:
  * wird ermittelt anhand eines vordefnierten Wörterbuchs, das leichte Wörter enthält. Wenn ein Wort nicht im Wörterbuch vorkommt, gilt es als schwer. 
  * Annahme: Je weniger schwere Wörter ein Text enthält, desto leicht ist der Text zu verstehen. 

#### Satzebene
Zur Berechnung der Komplexität wird die **Satzlänge** auf unterschiedliche Weise einbezogen:
* Satzlänge des Texts
  * wird errechnet durch die Anzahl an Wörtern in einem Satz. 
  * Annahme: Je kürzer die Sätze, desto leichter ist der Text zu verstehen
* Anzahl an Sätzen auf 100 Wörter:
  * Berechnung: Zählen von 100 Wörtern → Aufteilen der 100 Wörter in Sätze → Zählen der Sätze
  * Annahme: Je mehr Sätze, desto kürzer sind die Sätze, desto besser verständlich ist der Text 

Es wird meistens mit dem Durchschnitt der Wort- oder Satzlänge gerechnet. Der Durchschnitt wird berechnet indem zuerst die Längen aller Wörter/Sätze berechnet wird. Die Längen werden summiert und durch die Anzahl der Sätze/Wörter im Text geteilt.

### 2.3 Algorithmen zur Errechnung
Seit den 1940er Jahren wurden verschiedene Lesbarkeitsindice entwickelt, die teils sprachunbhängig sind, teils sprachabhängig (wenn die Anzahl der Silben in einem Wort oder ein vordefiniertes Wörterbuch einbezogen wird). Die meisten Indice wurde für die englische Sprache entwickelt. Die Berechnung kann zwar für die deutsche Sprache adaptiert werden (z.B. indem die Silbentrennung auf Deutsch angepasst wird), allerdings nehmen viele der Indice eine Gewichtung in ihrer Berechnung vor, die auch auf die englische Sprache angepasst ist. 
Für die deutsche Sprache wurde die Wiener Sachtextformel entwickelt. Auf das Deutsche angepasst wurde einer der bekanntesten Lesbarkeitsindice Flesch. Wir verwenden deshalb diese zwei Indice sowie den Automated Readability Index (ARI) und den Coleman-Liau-Score, da diese noch andere Paramter einbeziehen als Flesch und die Wiener Sachtextformel. 
Im Folgenden werden die vier Maße kurz vorgestellt und an folgendem Beispielsatz berechnet:
`
Mein Nachbar, den ich letztes Jahr kennengelernt habe, hat gestern ein Glitzereinhorn gekauft.
`

#### Flesch-Lesbarkeitsindex 
Der Flesch-Lesbarkeitsindex (entwickelt von Rudolf Flesch) ist eines der bekanntesten und am häufigsten verwendeten Maße für Textkomplexität. Für die deutsche Sprache wurde er von Toni Amstad adaptiert.

**Formel für den deutschen Flesch-Lesbarkeitsindex (Amstad):**

```
Flesch-Lesbarkeitsindex = 180 - ASL - (58,5 × ASW)
```

Wobei:
- ASL = Durchschnittliche Satzlänge (Anzahl der Wörter geteilt durch Anzahl der Sätze)
- ASW = Durchschnittliche Silbenzahl pro Wort (Anzahl der Silben geteilt durch Anzahl der Wörter)

**Interpretationsskala:**
- 90-100: Sehr einfach (5. Klasse)
- 80-90: Einfach (6. Klasse)
- 70-80: Mittelschwer (7.-8. Klasse)
- 60-70: Durchschnittlich (8.-9. Klasse)
- 50-60: Anspruchsvoll (10.-12. Klasse)
- 30-50: Schwierig (Studium)
- 0-30: Sehr schwierig (Akademiker:innen)

**Beispiel:**
* Durchschnittliche Satzlänge (ASL) = 13 (da Kommata und Punkte nicht als Worte gezählt werden)
* Durchschnittliche Silbenzahl (ASW) = 1 + 2 + 1 + 1 + 2 + 1 + 4 + 2 + 1 + 2 + 1 + 4 + 2 = 24 Silben / 13 Wörter = 1.8
* Flesch-Index = 180 - 13 - (58.5 * 1.84) = 61.7

Der Satz wird als *durchschnittlich* eingestuft.

#### Wiener Sachtextformel
Die Wiener Sachtextformel wurde von Richard Bamberger und Erich Vanecek speziell für deutsche Sachtexte entwickelt. Sie existiert in mehreren Varianten, wobei die Wiener Sachtextformel 2 am häufigsten verwendet wird.

**Formel (Wiener Sachtextformel 2):**

```
Wiener Sachtextformel = (0,2007 × MS) + (0,1682 × ASL) + (0,1373 × IW) - 2,779
```

Wobei:
- MS = Prozentsatz der Wörter mit drei oder mehr Silben
- SL = Durchschnittliche Satzlänge (Anzahl der Wörter geteilt durch Anzahl der Sätze)
- IW = Anzahl an langen Wörtern (länger als sechs Buchstaben) 

**Interpretationsskala:**
- 4-5: Sehr einfach (Primarstufe)
- 6-8: Einfach (Unterstufe)
- 9-10: Durchschnittlich (Mittelstufe)
- 11-12: Schwierig (Oberstufe)
- 13-15: Sehr schwierig (Universitätsniveau) 

**Beispiel:**
* Prozentsatz von Wörtern mit drei oder mehr Silben: 2 von 13 = 0.1538 * 100 = 15.38 
* Durchschnittliche Satzlänge (ASL) = 13 (da Kommata und Punkte nicht als Worte gezählt werden)
* Anzahl an langen Wörten: 6 
* Wiener Sachtextformel = (0,2007 * 15,38) + (0.1682 * 13) + (0.1373 * 6) - 2,779 = 3.32

Der Satz wird als *sehr einfach* eingestuft.


#### Automated Readability Index (ARI)
Der Automated Readability Index wurde entwickelt, um die Lesbarkeit von Texten anhand von Zeichen, Wörtern und Sätzen zu messen. Er wurde ursprünglich für die englische Sprache konzipiert, findet aber auch in anderen Sprachräumen Anwendung.

**Formel:**

```
ARI = 4,71 × (Zeichen/Wörter) + 0,5 × (Wörter/Sätze) - 21,43
```

**Interpretationsskala:**
- 1: 5-6 Jahre (Vorschule)
- 2: 6-7 Jahre (1. Klasse)
- ...
- 12: 16-17 Jahre (12. Klasse)
- 13+: 18+ Jahre (Hochschule)

**Beispiel:**
* Durchschnittliche Anzahl an Zeichen pro Wort: 6,31
* Durchschnittliche Satzlänge (ASL) = 13 (da Kommata und Punkte nicht als Worte gezählt werden)
* ARI = 4,71 * 6,31 + 0,5 * 13 - 21,43 = 14.8 

Der Satz wird als *sehr schwierig* eingestuft.

#### Coleman-Liau Score 
Der Coleman-Liau-Index wurde von Meri Coleman und T.L. Liau entwickelt und basiert auf der Anzahl von Buchstaben und Sätzen pro 100 Wörter.

**Formel:**

```
Coleman-Liau-Index = 0,0588 × L - 0,296 × S - 15,8
```

Wobei:
- L = Durchschnittliche Anzahl von Buchstaben pro 100 Wörter
- S = Durchschnittliche Anzahl von Sätzen pro 100 Wörter

**Interpretationsskala:**
Analog zum ARI, entspricht der Index dem US-amerikanischen Schuljahr, das zum Verständnis des Texts erforderlich ist.

**Beispiel:**
* Durchschnittliche Anzahl an Zeichen pro Wort (L): 6,31
* Durchschnittliche Satzanzahl (S) = 1 / 13 = 0.077
* Coleman-Liau = 0.0588 * 6,31 * 100 - 0,296 * 0.077 * 100 - 15,8 = 18,52

Der Satz wird als *sehr schwierig* eingestuft.

### 2.4 Komplexere Methoden zur Berechnung der Textkomplexität

## 3. Zeitlicher Verlauf und visuelle Darstellung 



