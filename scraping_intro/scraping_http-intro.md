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

(scraping-intro_http-intro)=
# Webkommunikation mittels HTTP
```{admonition} Groblernziel dieses Kapitels
:class: lernziele
Sie können die Komponenten aufzählen, die an einem HTTP-Request beteiligt sind, den Unterschied zwischen dem Aufbau eines HTTP-Requests und einer HTTP-Response erläutern sowie die Response codes 200, 404, 403 und 500 interpretieren.
```

Zur Erstellung eines Korpus bestehend aus großen Mengen von Website-Inhalten, ist es ratsam eine automatisierte Methode zum Herunterladen der Website-Inhalte zu verwenden. Um zu verstehen, wie das Herunterladen bzw. das Abfragen von Websites automatisert werden kann, verschaffen wir uns zuerst einen Überblick darüber, was (auf Netzwerkeebene) passiert, wenn wir eine Website anwählen.  

## Aufbau der Webkommunikation mittels HTTP
Wenn Sie eine Website besuchen, passiert im Hintergrund Folgendes:

1. **Anfrage senden**: Ihr Computer, der **Client**, schickt eine Anfrage an den Computer, auf dem die Website gespeichert ist, den **Server**. Diese Anfrage heißt **HTTP-Request** und ist vergleichbar mit einem Formbrief: "Bitte sende mir die Webseite unter dieser Adresse."

2. **Antwort erhalten**: Der Server bearbeitet Ihre Anfrage und schickt eine Antwort zurück, die **HTTP-Response**. Diese enthält sowohl Metainformationen über den Erfolg der Anfrage als auch die eigentlichen Inhalte der Webseite.

### HTTP Request
Ein HTTP-Request besteht vor allem aus zwei wichtigen Elementen:
1. Der  **URL (Uniform Resource Locator)**: Dies ist die Webadresse, die Sie aufrufen möchten. Sie besteht typischerweise aus mehreren Teilen:
- `https://` - Das Protokoll (verschlüsselte Verbindung)
- `www.berlin.de/` - Der Domainname (Server-Adresse)
- `rbmskzl/` - Der Pfad zur spezifischen Ressource
- `?suche=Begriff&seite=2` - Optionale Parameter (nach dem Fragezeichen)
Die vollständige URL hier als Beispiel der Berliner Senatskanzlei lautet zusammengesetzt: [https://www.berlin.de/rbmskzl/](https://www.berlin.de/rbmskzl/)

2. Einer **Request-Methode**, mit der spezifiziert wird, welche Aktion vom Server erwartet wird. Die gängigsten Request-Methoden sind:
- **GET**-Request: Fragt Daten an, ohne sie zu verändern (wie wenn Sie einen Katalog bestellen würden). GET-Requests sind in der URL sichtbar (z.B. in der Adressleiste Ihres Browsers).
- **POST**-Request: Sendet Daten an den Server, z.B. bei Formularen oder Login-Daten (wie wenn Sie ein ausgefülltes Formular zurücksenden würden). POST-Daten sind nicht in der URL sichtbar.

### HTTP-Response
Die Antwort vom Server enthält ebenfalls mehrere Komponenten:

- **Statuscode**: Informiert über den Erfolg der Anfrage:
  - **200 ("OK")**: Alles hat funktioniert, hier sind die gewünschten Daten.
  - **404 ("Not Found")**: Die angeforderte Seite existiert nicht. Das ist vergleichbar mit einem Postboten, der eine Adresse nicht finden kann.
  - **403 ("Forbidden")**: Zugriff verweigert - wie vor einer verschlossenen Tür zu stehen.
  - **500 ("Internal Server Error")**: Der Server hat ein Problem, wie wenn die Poststelle selbst nicht funktioniert.
- **Response-Header**: Informationen über die Antwort, z.B. welchen Inhaltstyp sie enthält (Text, Bild, etc.)
- **Response-Body**: Der eigentliche Inhalt, meist HTML-Code für Webseiten (siehe Kapitel [Einführung in HTML](html-intro_html-intro)), aber auch Bilder, PDFs oder andere Dateitypen.


## Automatisierte Abfrage der Startseite der Berliner Senatskanzlei
Beispielhaft wollen wir die Startseite der Berlinar Senatskanzlei abfragen. Dafür verwenden wir die Python-Bibliothek `requests` und erstellen einen GET-Request, da wir ausschließlich die Inhalte der Website zugesendet bekommen wollen (wie wenn Sie auf diese URL klicken: [https://www.berlin.de/rbmskzl/](https://www.berlin.de/rbmskzl/)).

```{code-cell} python3
# import library to perform HTTP requests
import requests

# Set URL 
url = "https://www.berlin.de/rbmskzl/"

# perform get request
response = requests.get(url)

# check if request was successful (code: 200)
if response.status_code == 200:
    print(response.status_code)

    # display the first lines of the response body (the content of the website)
    print(response.text[:100])
else:
    print(response.status_code)
```



