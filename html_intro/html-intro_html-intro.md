(html-intro_html-intro)=
# Einführung in HTML

HTML (HyperText Markup Language) ist die Grundsprache des Internets. Sie wird verwendet, um Webseiten zu strukturieren und Inhalte wie Text, Bilder und Links darzustellen. Die Bausteine der HTML-Sprache sind HTML-Elemente.

```{figure} ../book_images/html_tag_anatomy.png
---
height:
name: HTML-Element
---
Der Aufbau eines einfachen HTML-Elements
```

## 1. Die Grundstruktur einer HTML-Seite
Jede HTML-Datei beginnt mit der Deklaration `<!DOCTYPE html>`, die dem Browser mitteilt, dass es sich um eine HTML5-Datei handelt. Die grundlegende Struktur sieht so aus:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meine erste Webseite</title>
</head>
<body>
    <h1>Willkommen!</h1>
    <p>Dies ist ein einfacher Absatz.</p>
</body>
</html>
```

- `<html>`: Der Hauptcontainer für die gesamte Seite.
- `<head>`: Enthält Metainformationen und den Titel der Seite.
- `<title>`: Legt den Titel der Webseite fest.
- `<body>`: Enthält den sichtbaren Inhalt der Seite.

## 2. Wichtige HTML-Elemente
HTML besteht aus verschiedenen Elementen, die durch Tags (`<tag>` und `</tag>`) gekennzeichnet sind.

### a) Überschriften und Absätze
- `<h1>`, `<h2>`, ..., `<h6>`: Überschriften unterschiedlicher Größe.
- `<p>`: Ein Absatz.

```html
<h1>Überschrift 1</h1>
<h2>Überschrift 2</h2>
<p>Dies ist ein Absatz.</p>
```

### b) Links und Bilder
- `<a href="URL">Text</a>`: Erstellt einen Link.
- `<img src="bild.jpg" alt="Beschreibung">`: Fügt ein Bild ein.

```html
<a href="https://www.example.com">Besuche Example</a>
<img src="bild.jpg" alt="Beispielbild">
```

## 3. Listen und Tabellen

### a) Ungeordnete und geordnete Listen
- `<ul>`: Eine Liste mit Punkten.
- `<ol>`: Eine nummerierte Liste.
- `<li>`: Ein Listenelement.

```html
<ul>
    <li>Erstes Element</li>
    <li>Zweites Element</li>
</ul>
```

### b) Tabellen
- `<table>`: Erstellt eine Tabelle.
- `<tr>`: Erstellt eine Zeile.
- `<td>`: Erstellt eine Zelle.
- `<th>`: Erstellt eine Kopfzelle.

```html
<table>
    <tr>
        <th>Name</th>
        <th>Alter</th>
    </tr>
    <tr>
        <td>Max</td>
        <td>25</td>
    </tr>
</table>
```

## 4. HTML und CSS
HTML strukturiert die Inhalte, aber für das Design wird CSS (Cascading Style Sheets) verwendet. CSS kann direkt in HTML eingefügt werden:

```html
<style>
    body { background-color: lightblue; }
    h1 { color: darkblue; }
</style>
```

## Fazit
HTML ist einfach zu lernen und bildet die Grundlage jeder Webseite. Mit HTML kann man Texte, Bilder, Links, Tabellen und mehr darstellen. CSS ist ein wichtiger Bestandteil des Webdesigns. Um Websites zu scrapen und automatisch Daten aus dem Web zu extrahieren, sind HTML-Kenntnisse besonders wichtig.

### Video: eine 3-minütige HTML-Einführung von W3C

<iframe width="560" height="315" src="https://www.youtube.com/embed/it1rTvBcfRg?si=WRkTaxnrprLZM9RP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
