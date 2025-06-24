# Resümee

```{admonition} Key points des Kapitels
:class: keypoint

**Automatisierte HTTP-Anfragen**

Mithilfe einer HTTP-Bibliothek wie *Requests* können HTTP-Anfragen automatisiert werden. Dadurch lassen sich große Mengen an Webseiten gezielt und wiederholbar abrufen.

**HTML-Parsing mit BeautifulSoup**

Mit einer HTML-Parsing-Bibliothek wie *BeautifulSoup* lässt sich die Struktur der Suchergebnisse auf *berlin.de* systematisch analysieren. So können Links zu Pressemitteilungen sowie die Inhalte einzelner Pressemitteilungsseiten effizient extrahiert werden.

**Herausforderungen beim Massenscraping**

Beim Massenscraping müssen typische Fehlerfälle berücksichtigt werden, etwa nicht erreichbare Links (HTTP-Status 404), temporäre Sperrungen durch den Server bei zu vielen Anfragen (HTTP-Status 429) sowie weitere technische Einschränkungen. Pausen zwischen den Anfragen (Sleep-Intervalle) sind dabei essenziell, um ein stabiles und serverfreundliches Crawling sicherzustellen.

**Metadaten erfassen**

Da das Scraping von externen Servern abhängt und zeitaufwendig sein kann, sollten Metadaten parallel zum Scraping-Prozess systematisch erfasst und gespeichert werden. Zu jeder Meldung speicherten wir: ID, URL, Datum, Titel, Quelle (Ressort), Dateinamen von HTML/TXT sowie Tokenzahl.  Diese strukturierte CSV ist Grundlage für spätere Analysen (Zeitreihen, Quellvergleiche, Längenverteilung …).
```
<!-- **Filter → Korpusabgrenzung**  
Mit gezielten Checkbox-Filtern im Berliner Presseportal haben wir ausschließlich Veröffentlichungen der Exekutive (Senatsverwaltungen + Bezirksämter + Landesbeauftragte) erfasst und Polizei / Justiz sowie weitere Sonderbehörden ausgeschlossen. So entsteht ein thematisch kohärentes, politisch vergleichbares Korpus. -->