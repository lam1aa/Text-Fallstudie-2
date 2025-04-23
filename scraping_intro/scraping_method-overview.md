(scraping-intro_method)=
# Web-Scraping als Methode der Korpuserstellung
```{admonition} Groblernziel dieses Kapitels
:class: lernziele
Sie können verschiedene Methoden der Website-Abfrage aufzählen und Unterschiede identifizieren. 
Sie können Vor- und Nachteile der Methoden erklären und ermitteln, in welchen Szenarien welche Methode geeignet ist.
```

Im [vorherigen Kapitel](scraping-intro_http-intro) haben wir bereits ein Beispiel zur automatisierten Abfrage einer Website kennengelernt. Um mehr als eine Website abzufragen, gibt es verschiedene Methoden. Welche Methode sich am besten zur Extraktion eignet, hängt davon ab, wie die abzufragenden Websites aufgebaut sind und sie rein statische oder auch dynamische Inhalte beinhalten. 

### Statische vs. dynamische Websites

Websites können grundsätzlich in zwei Kategorien eingeteilt werden: statische und dynamische Websites. Abhängig davon, welche Inhalte extrahiert werden sollen und wie die Website beschaffen ist, muss die Scraping-Methode angepasst werden.

- **Statische Websites**: Diese Websites sind wie fertige Dokumente, die auf dem Server bereitliegen. Wenn Sie eine solche Seite anfordern, wird Ihnen exakt dieser vorbereitete Inhalt geschickt. Das ist vergleichbar mit dem Anfordern eines bestimmten Buchkapitels aus einer Bibliothek – der Inhalt liegt fertig vor und ändert sich nicht. Diese Art von Websites kann leicht mit einfachen Scraping-Methoden extrahiert werden, da alle Informationen direkt im HTML-Code enthalten sind.

- **Dynamische Websites**: Diese modernen Websites werden erst im Moment der Anfrage oder sogar in Ihrem Browser zusammengestellt. Sie enthalten oft JavaScript-Code, der nach dem Laden der Seite ausgeführt wird und weitere Inhalte nachladen oder verändern kann. Das ist vergleichbar mit einem Koch, der das Gericht erst auf Bestellung zubereitet oder sogar mit einer Anleitung, die Sie selbst ausführen müssen. Für diese Art von Websites benötigt man fortgeschrittenere Scraping-Methoden wie Selenium, die einen echten Browser simulieren können.


## Drei Ebenen des Web Scrapings

### 1. Einfache Anfragen mit requests

Die grundlegendste Form des Web Scrapings ist das Abrufen einzelner Webseiten, z.B. mit Hilfe des Python-Pakets `requests`. Diese Methode eignet sich für statische Webseiten, deren Inhalt direkt im HTML-Code enthalten ist.

```python
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
    print(f"Fehler beim Abrufen der Seite: {response.status_code}")
```

**Vorteile:**
- Einfach zu implementieren
- Geringer Ressourcenverbrauch
- Ausreichend für einfache Scraping-Aufgaben

**Nachteile:**
- Nur einzelne Seiten werden abgerufen
- Keine automatische Navigation zu anderen Seiten
- Nicht geeignet für dynamisch generierte Inhalte (JavaScript)

### 2. Navigation mit Scrapy

Für komplexere Scraping-Aufgaben, bei denen mehrere Seiten durchlaufen werden müssen, eignet sich die Bibliothek `scrapy`. Sie ermöglicht das systematische Folgen von Links und das Extrahieren von Daten aus mehreren Seiten.

```python
import scrapy

class BooksSpider(scrapy.Spider):
    name = 'books'
    start_urls = ['https://books.example.com/']

    def parse(self, response):
        # Extrahiere Daten von der aktuellen Seite
        for book in response.css('div.book-item'):
            yield {
                'title': book.css('h2.title::text').get(),
                'author': book.css('p.author::text').get(),
                'price': book.css('span.price::text').get()
            }

        # Folge den Links zu den nächsten Seiten
        next_page = response.css('a.next-page::attr(href)').get()
        if next_page is not None:
            yield response.follow(next_page, self.parse)
```

**Vorteile:**
- Effizientes Crawlen mehrerer Seiten
- Integrierte Funktionen für Datenverwaltung und -export
- Robuste Error-Handling-Mechanismen

**Nachteile:**
- Steilere Lernkurve als bei `requests`
- Nicht geeignet für dynamische Webseiten mit JavaScript
- Komplexere Konfiguration

### 3. Simulation von Benutzerinteraktionen mit Selenium

Für Websites, die dynamische Inhalte mittels JavaScript laden oder Benutzerinteraktionen erfordern, ist `Selenium` die geeignete Wahl. Diese Bibliothek steuert einen echten Webbrowser und kann somit mit allen Elementen interagieren.

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.service import Service
from webdriver_manager.chrome import ChromeDriverManager
import time

# Browser-Instanz erstellen
driver = webdriver.Chrome(service=Service(ChromeDriverManager().install()))

# Website aufrufen
driver.get('https://example.com/dynamic-page')

# Warten, bis JavaScript-Inhalte geladen sind
time.sleep(2)

# Mit Elementen interagieren
search_button = driver.find_element(By.ID, 'search-button')
search_button.click()

# Auf dynamisch geladene Inhalte zugreifen
results = driver.find_elements(By.CLASS_NAME, 'result-item')
for result in results:
    print(result.text)

# Browser schließen
driver.quit()
```

**Vorteile:**
- Zugriff auf dynamisch geladene Inhalte (JavaScript)
- Simulation von Benutzerinteraktionen (Klicks, Formulare ausfüllen)
- "Sieht" die Website wie ein menschlicher Benutzer

**Nachteile:**
- Deutlich ressourcenintensiver
- Langsamer als `requests` oder `Scrapy`
- Anfälliger für Änderungen im Website-Layout

## Geeignete Szenarien für die verschiedenen Methoden

| Szenario | Geeignete Methode | Begründung |
|----------|-------------------|------------|
| Extraktion von Texten aus einer bekannten Webseite | `requests` | Einfach, effizient für einzelne statische Seiten |
| Durchsuchen und Extraktion von Daten aus einem Blog oder Wiki | `Scrapy` | Effizientes Folgen von Links, Extrahieren ähnlicher Daten von mehreren Seiten |
| Daten aus einem Social-Media-Portal | `Selenium` | Notwendig für Login, Scrollen, Klicken und dynamisch nachgeladene Inhalte |
| Korpuserstellung aus statischen Webseiten | `Scrapy` | Gute Balance aus Geschwindigkeit und Funktionalität für größere Sammlungen |
| Korpuserstellung aus dynamischen Webseiten | `Selenium` | Notwendig für Scrollen, Klicken und dynamisch nachgeladene Inhalte |
| Interaktion mit Suchformularen | `Selenium` | Ermöglicht das Ausfüllen und Absenden von Formularen |

## Ethische und rechtliche Aspekte

Beim Web Scraping sind stets ethische und rechtliche Aspekte zu beachten:

- Beachtung der `robots.txt`-Datei einer Website, die Informationen darüber gibt, welche Websites gescraped werden dürfen.
- Angemessene Wartezeiten zwischen Anfragen einhalten
- Keine persönlichen Daten ohne Einwilligung sammeln
- Urheberrecht und Nutzungsbedingungen der Websites beachten
- Datenschutzbestimmungen einhalten
