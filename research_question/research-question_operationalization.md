(research-question_operationalization)= 
# Operationalisierung und Methodik
```{admonition} Feinlernziel(e) dieses Kapitels
:class: lernziele
Sie kennen Ansätze zur Operationalisierung von Forschungsfragen für quantitaive Methoden-Settings.
```
Die im [vorhergehenden Abschnitt](research-question_research-question) entwickelte Forschungsfrage zielt darauf, eine Verminderung der sprachlichen Komplexität in der Kommunikation der Berliner Senatsverwaltung mit der Öffenlichkeit zu beobachten, mithin potenzielle Veränderungen der kommunikativen Barrierearmut in einem bestimmten Zeitraum zu messen. 

Um eine solche Messung möglich zu machen, muss zunächst eine Operationalisierung der Forschungsfrage erfolgen. "Operationalisierung bezeichnet den Prozess, ein Erkennungs- oder Messverfahren für ein theoretisches Konzept zu entwickeln." {cite:p}`krautter_operationalisierung_2023`.

Für die Operationalisierung unserer Forschungsfrage müssen insbesondere drei Fragen adressiert werden:
- Was verstehen wir unter kommunikativer Barrierearmut? 
- Wie kann diese gemessen werden?
- Anhand welches Korpus lässt sich die kommunikative Barrierearmut messen?

## Kommunikative Barierefreiheit und das Konzept der Leichten Sprache
Das Konzept der kommunikativen Barrierearmut koppeln wir, wie im vorhergehenden Abschnitt bereits vorbereitet, an das **Konzept der Leichten Sprache**. Unter Barrierefarmut wollen wir in diesem Sinne im Folgenden eine Kommunikation in leicht verständlicher Sprache verstehen. Kommunikative Barrierarmut ist damit ein gradueller Begriff: die Sprache kann leichter oder schwerer verständlich sein. Unsere Messung soll genau das ermitteln: wird sie Sprache – unter bestimmten Gesichtspunkten – leichter oder schwerer verständlich?

In der Forschung wird das Konzept der Leichten Sprache an einer ganzen Reihe von Indikatoren festgemacht. Die [DIN SPEC „Empfehlungen für Deutsche Leichte Sprache“](https://www.dinmedia.de/de/technische-regel/din-spec-33429/387728031) beziehen sich z.B. in Hinblick auf die sprachliche Dimension …  
- … auf die **Wortebene** (z.B. Verwenden geläufiger Wörter, Vermeiden von Metaphern und Fremd- bzw. Fachwörtern oder Abkürzungen u.v.m.), 
- … auf die **Satzebene** (eher Verbalstil, Vermeiden von Negationen, Vermeiden von komplexen Nominalphrasen und eingebetteten Nebensätzen u.v.m.) 
- … und auf **Textebene** (klare Absatzgliederung, vorangestellte Zusammenfassung, Verwenden von Zwischenüberschriften u.v.m.)

## Lesbarkeitsindizes
Für unsere Operationalisierung wollen wir auf ein kleines Set aus diesen Indikatoren zurückgreifen, das traditionell in sogenannten **Lesbarkeitsindizes** ({cite:p}`dubay_principles_2004`) zusammengeführt wird, die zur Messung von Textkomplexität entwickelt wurden. Viele dieser Lesbarkeitsindizes nutzen dabei zur Berechnung der Textkomplexität die durchschnittliche Wortlänge und die durchschnittliche Satzlänge, und damit zwei Parameter, die auch im Diskurs um Leichte Sprache regelmäßig herangezogen werden. 

Vor diesem Hintergrund können wir unsere Fragestellung fokussieren, präzisieren und konkretisieren: Wir werden die kommunikative Barrierearmut messbar machen, indem wir mittels des Konzepts der Lesbarkeitsindizes die Textkomplexität messen und diese Messwerte so auswerten, dass wir zeitliche Entwicklungen ermitteln können. Daraus folgt für unsere Fragestellung: 
- Steigt die mittels Lesbarkeitsindizes ermittelte Textkomplexität in den Texten unseres Korpus über die Zeit, dann wir die Behördenkommunikation schwerer verständlich.
- Sinkt die mittels Lesbarkeitsindizes ermittelte Textkomplexität in den Texten unseres Korpus über die Zeit, dann wir die Behördenkommunikation leichter verständlich.

## Wahl eines Korpus
Die damit skizzierten Analysen werden wir auf einem **Korpus** durchführen, das mindestens vier Kriterien erfüllen muss: 
- Es muss öffentlich zugänglich und maschinell aggregierbar ("Scraping") sein.
- Es muss im Kern der Kommunikation der Behörden mit der Öffentlichkeit dienen
- Es muss in Hinblick auf die enthaltenen Textsorten möglichst homogen sein, da es bei Textsorten jeweils unterschiedliche Konventionen der Textkomplexität geben kann.
- Die Einzeltexte des Korpus müssen sich möglichst präzise zeitlich situieren lassen, da nur so die Frage nach der zeitlichen Verteilung und damit nach der Entwicklung beantwortbar ist. 

Nach systematischen Recherchen auf den Websites der Landesbehörden des Landes Brandenburg und des Landes Berlin haben wir uns dafür entschieden, die Pressemitteilungen der Berliner Senatsverwaltung als exemplarischen Datensatz auszuwählen, den wir für die Analyse im Sinne unserer Fragestellung nutzen wollen. Die Pressemitteilung erfüllen alle der vier oben genannten Kriterien. Mit dem Korpusaufbau beschäftigen wir uns weiter im Kapitel [Korpora als epistemische Objekte](corpus-collection_intro)


## Unsere Operationalisierung
Im Ergebnis kommen wir schließlich zu der folgenden Operationalisierung.

`````{admonition} Operationalisierung
:class: tip
Als repräsentative Kommunikation des Berliner Senats mit der Öffentlichkeit sollen die vom Senat veröffentlichten Pressemitteilungen gelten. Unter Barrierearmut wird eine Kommunikation in leicht verständlicher Sprache verstanden. Um die Komplexität der Sprache zu messen, werden verschiedene Lesbarkeitsindice herangezogen, die etwa auf der durchschnittlichen Wort- bzw. Satzlänge beruhen. 
Wenn die so verstandene Textkomplexität über die Zeit niedriger wird, spricht dies für eine barriereärmere Kommunikation. Wenn die Textkomplexität über die Zeit ansteigt, nehmen die sprachlichen Barrieren in der Kommunikation zu. 

`````

## Reflexion der Praxis des Operationalisierens
Diese Operationalisierung ist, wie jede Operationalisierung in den Digital Humanities, diskutabel. Sie folgt dabei einem quantitativen Methodenparadigma. Und sie wählt mit den Lesbarkeitsindice einfache Indikatoren für das zu messende Phänomen. Die Operationalisierung wird zudem weitere Einschränkungen erfahren müssen, etwa was das Korpus der Analysen betrifft, das mit der Formulierung "vom Senat veröffentlichten Pressemitteilungen" noch zu groß gewählt ist und sich auf die digital verfügbaren Pressemitteilungen beschränken wird.   

Die Reflektion der Grenzen und Beschränkungen, die mit der eigenen Operationalisierung einhergehen, ist essentieller Bestandteil von Digital Humanities-Projekten. Wir werden in der abschließenden [Reflexion](reflection_reflection) darauf zurückkommen.

## Bibliographie
```{bibliography}
:filter: docname in docnames
```
