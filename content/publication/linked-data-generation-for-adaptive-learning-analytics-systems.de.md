+++
title = "Linked Data Generation for Adaptive Learning Analytics Systems"
date = 2018-06-23T12:34:08+02:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Sven Lieber", "Ben De Meester", "Anastasia Dimou", "Ruben Verborgh"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "In LILE workshop, part of the WebScience conference"
publication_short = "In LILE workshop, part of the WebScience conference"

# Abstract and optional shortened version.
abstract = ""
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = ["leaps"]

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Learning Analytics", "Linked Data", "Provenance"]

# Links (optional).
url_pdf = "https://websci18.webscience.org/wp-content/uploads/2018/01/WebSci18_Events_PreProceedings-4-Linked_Learning_2018-lres.pdf"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = "https://www.imec-int.com/en/what-we-offer/research-portfolio/leaps"
url_slides = "https://doi.org/10.5281/zenodo.7257398"
url_poster = "https://doi.org/10.5281/zenodo.7257459"
url_video = ""
url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Does this page contain LaTeX math? (true/false)
math = false

# Does this page require source code highlighting? (true/false)
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "2018-06-23-lile-paper-header.jpg"
caption = ""

+++

Auch schon mal geärgert das Übungen einer Sprachlern-App entweder zu schwer oder zu einfach sind?
Tatsächlich sind das Gründe, weshalb viele Leute aufgeben.
Vermutlich würde es den Nutzern einer solchen Sprachlern-App nützen, wenn ein adaptives Lernanalysesystem verwendet wird, welches sich auf die Fähigkeiten der Nutzer einstellt.
Das Bereitstellen eines adaptiven Lernanalysesystems samt Daten, ist Teil eines [Projekts](https://www.imec-int.com/en/what-we-offer/research-portfolio/leaps) an dem ich momentan arbeite.
<!--more-->

Dieses Paper wurde beim Linked Learning ([LILE](https://lile2018.wordpress.com/)) workshop bei der [WebScience2018](https://websci18.websience.org/) Konferenz angenommen,
und beschreibt wie aus Lernaktivitätsdaten (Logfiles welche generiert werden während eine pädagogische App verwendet wird) Linked Data generiert werden kann.
Im folgenden wird beschrieben was Linked Data ist, wie es beim adaptiven Lernen helfen kann und wie wir etwas namens [Provenance](https://sven-lieber.org/de/2017/04/07/was-ist-provenance/) 
benutzen um Benutzern unseres Systems
bei Datenschutzaufgaben behilflich zu sein.

# Problem
Das Anpassen vom Schwierigkeitsgrad einer Aufgabe, basierend auf Fähgikeiten des Nutzers, kann durch maschinelles Lernen ermöglicht werden.
Maschinenlernalgorithmen müssen trainiert werden und benötigen eine Menge Daten!
Die Art der Aufgabe muss beschrieben werden (ist es eine grammatikalische Aufgabe? audiovisuell?), 
aber auch Daten bezüglich der Nutzer (sind Lernschwächen wie Dyslexie bekannt? Was weis ein Nutzer bereits?).
All diese Daten müssen dann natürlich noch integriert werden um verwendbar zu sein.
Anders ausgedrückt: Ein Programm muss verstehen das ein bestimmtes Konzept wie eine Lernschwäche 
in Beziehung zu anderen Konzepten wie Grammatik steht (welches dann ein wesentlicher Teil einer Aufgabe ist).

# Lösung
Das Beschreiben von Aufgaben und Nutzern mit der Hilfe von semantischen Technologien, als zusätzlichen Verarbeitungsschritt von existierenden Lernaktivitätsdaten.

Wie können wir Dinge semantisch beschreiben damit auch Programme es verstehen können? Dafür verwenden wir Linked Data!
Im Grunde ist Linked Data eine Menge von Design-Prinzipien, jedes beschriebene Konzept

* sollte eine eindeutige Kennzeichnung besitzen (Man beschreibt bspw. ein Konzept und gibt ihm den Namen "Person")
* sollte dereferenzierbar sein (Ein Programm welches unser "Person" Konzept verwendet, muss in der Lage sein nachzusehen was eine Person ist) => http://xmlns.com/foaf/spec/#term_Person ist eine eindeutige Kennzeichnung da eine URL verwendet wird, und daher ebenfalls dereferenzierbar für ein Programm
* sollte mit Standards beschrieben werden (Die Definition eines Konzepts "Person" mittels eines Standards wie RDF stellt sicher das ein Programm es verarbeiten kann)
* sollte wiederverwendbar sein und zu anderen existierenden Konzepten verlinken.

![Linked Data Beispiel](/img/2018-06-23-ld-example.jpg)


Das Bild zeigt ein Linked Data Beispiel als Graph.
Verschiedene Farben repräsentieren verschiedene Domänen.
Daten welche Lernaktivitäten beschreiben sind blau dargestellt, Daten welche Nutzer beschreiben grün, und Daten welche Fähigkeiten beschreiben (gelb).
Die Präfixe sind Abkürzungen für eine URI.


Und siehe da, wir haben die Daten von verschiedenen Domänen bereits in einem einheitlichen Graphmodell integriert!
Das sieht nach einer schönen Lösung aus, richtig? Aber wie bekommen wir Linked Data?


Wir zwingen niemanden die Art und Weise wie Lernaktivitätsdaten generiert werden zu ändern.
Die Einzige Voraussetzung die wir haben ist, dass Lernaktivitätsdaten mittels der [xAPI Spezifikation](https://github.com/adlnet/xAPI-Spec) beschrieben werden.
XAPI ist ein strukturiertes Textformat, welches bereits breite Anwendung findet.
Lernaktivitätsdaten sind für gewöhnlich in speziellen Datenbanken, genannt Learning Record Stores, gespeichert.
Unsere Lösung baut auf diesen Learning Record Stores auf, in anderen Worten: Wir extrahieren Daten aus diesen Datenbanken.

Wir konstruierten eine Pipeline, welche Standardtechnologien wie [JSON-LD](https://www.w3.org/TR/json-ld/) verwendet, 
um die strukturierten Textdaten zu Linked Data zu transformieren.

Für jeden Verarbeitungsschritt in der Pipeline sammeln wir auch Provenance Informationen, welche wir ebenfalls mithilfe von Linked Data beschreiben.
Warum das?
Nunja, geltendes Datenschutzrecht wie die Datenschutzgrundverordung (DSGVO, engl. GDPR) gewährt Personen deren persönliche Daten verarbeitet werden verschiedene Rechte.
Personen können beantragen das ihre Daten gelöscht, oder korrigiert werden.
Falls solch ein Antrag eingeht, können Benutzer unserer Applikation basierend auf bestehenden Linked Data Provenance Informationen abfragen woher 
Lernaktivitätsdaten kommen und wann sie extrahiert worden sind.
Das ermöglicht die Löschung oder Korrektur personenbezogener Daten in der Quelle und ggf. allen Kopien die durch Verarbeitungsschritte erzeugt wurden.

