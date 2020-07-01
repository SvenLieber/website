+++
title = "Meine Doktorarbeit erklärt"
date = 2020-06-21T16:28:14+02:00
draft = false
slug = "meine-doktorarbeit-erklaert"

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["PhD", "ontologies", "constraints"]
categories = ["explained"]

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "2020-06-phd-explained.jpg"
caption = ""
preview = true

+++

Es ist besonders schwierig die eigene Dokotorarbeit der Familie und Freunden zu erklären,
gerade in so einem abstrakten Gebiet wie der Informatik.
Im folgenden Blogpost werde Ich versuchen meine Doktorarbeit zu erklären,
befreit von akademischer Genauigkeit und mehr mit dem Großen und Ganzen im Blick.

<!--more-->

**Um es in einem Satz zusammenzufassen: Ich beschäftige mich mit Datenmodellierung.**
Ich gehe der Frage nach
wie wir graphbasierte Wissensmodelle erstellen können welche 
ebenfalls Anforderungen an Datenqualität oder Datenschutzbestimmungen erfüllen.
Im speziellen befasse ich mich einerseits mit Methoden der Wissensverarbeitung (Knowledge Engineering),
also welche Schritte durchgeführt werden müssen um solche Wissensmodelle zu erstellen,
und andererseits mit benutzerfreundlichen Visualisierungen von Bedingungen in graphbasierten Wissensmodellen (data constraints).

# Das große Ganze

Die Aufzählungspunkte sind eine zusammenhängende Story,
aber jeder Paragraph der mit einem Pfeil markiert ist kann bei Bedarf angeklickt werden um mehr zu erfahren.

<details>
<summary>Das Kombinieren von Daten aus verschiedenen Bereichen,
auch Domänen genannt, hat großes Potential.</summary>
Um den folgenden Befehl auszuführen müssen Informationen aus verschiedenen Bereichen zur Verfügung stehen.
"Alexa, schalte die Heizung an wenn ich im Homeoffice bin, es weniger als 18 Grad Celsius hat und die Kilowattstunde Strom nicht mehr als x Euro kostet".
Was wenn das Thermometer nur Daten in Fahrenheit zur Verfügung stellt?
Was wenn keine Informationen zu aktuellen Preisen vorliegen?
Und was ist überhaupt Homeoffice, wie kann Alexa das feststellen?
Ein Heizungssystem besteht aus vielen Sensoren, mein Kalender besteht aus vielen Daten
und eine Gemeinde publiziert oft Statistiken oder andere Informationen als "Open Data".
All diese Daten sind in verschiedenen Formaten und jeder der sich versucht eine nützliche App
zu Entwickeln welche alle drei Datenquellen verwendet muss die App womöglich
für jedes Heizungsszstem, jede Kalenderapplikation oder jede Gemeinde aufs neue entwickeln!
Standards helfen das Leben einfacher zu machen, ein Smartphone Ladekabel passt in jede Steckdose
in einem Land.
Dasselbe Prinzip gilt auch für Daten, folgen zum Beispiel alle Heizungshersteller einem Standard
Datenmodell kann eine App für verschiedene Heizungsanlagen verwendet werden.
Leider ist so ein Standard auf einen Bereich beschränkt,
und warum sollte ein Heizungsstandard auch Kalenderinformationen oder Strompreise definieren?!
</details>

<details>
<summary>Aber um Daten aus verschiedenen Domänen *sinnvoll* zu kombinieren ist ein
gemeinsames Verständnis in der Form eines standardisierten Vokabulars, einem Datenmodell, nötig:
Die Temparaturmessung eines Heizungssystems in Grad Celsius sollte nicht einfach
mit einer Temparaturmessung in Fahrenheit oder gar mit meinem Lebensalter verrechnet werden!
</summary>
Hierfür verwende Ich das Resource Description Framework ([RDF](https://www.w3.org/TR/2014/REC-rdf11-concepts-20140225/)),
eine vom World Wide Web Consortium (W3C) empfohlene graphbasierte Sprache.
Jedes *Ding* und jede mögliche *Beziehung* zwischen *Dingen* bekommt eine eigene Webadresse!
Dadurch ist *alles* eindeutig identifizierbar, und da alles derselben Graphstruktur folgt
kann ein *Heizungssystem* welches in der *Seriennummer*-beziehung zu einer *Nummer steht*,
auch in einer *gehört-zu*-beziehung zu *mir* stehen.
Es kann ebenfalls spezifiziert werden das eine konkrete *Messung* vom typ *Grad Celsius* ist.
*Ich* wiederum kann in mehreren *Beziehugen* zu persönlichen Informationen wie meiner *Blutgruppe*
oder meinem *Geburtsdatum* stehen.
Das große Plus: Computerprogramme können die "Webseiten" nachschlagen und die Definitionen
von *Dingen* und *Beziehungen* lesen und interpretieren.
Außerdem lässt sich so ein Graph einheitlich nach Informationen durchsuchen
egal ob es sich jetzt um Informationen zu meiner Heizung oder mir handelt.
</details>


<details>
<summary>Ein solches Vokabular welches Konzepte, deren Beziehungen zueinander
und *Bedeutung* in der Form von Bedingungen definiert
sollte detailliert genug sein um Fragen zu beantworten
die wir im vornherein evtl. haben, in anderen Worten: es muss seinen Zweck erfüllen.
</summary>
Ein erster Schritt in der Wissensmodellierung ist das Aufschreiben der Anforderungen,
zum Beispiel in Form von Fragen.
Dadurch kann in einem späterern Schritt in der Wissensmodelleriung überprüft werden
ob das Datenmodell seine Anforderungen erfüllt, also die Fragen beantworten kann.
</details>


<details>
<summary>
Obwohl sehr präzise und mit *Bedeutung* versehende Datenmodelle unverzichtbar für manche Zwecke sind,
birgt deren Komplexität Nachteile für viele andere Zwecke.
</summary>
In den Domänen *Biotechnik* und *Maschinenbau* werden oft sehr präzise
Datenmodelle mit RDF erstellt.
Diese sind so präzise das spezielle Programme mit den gegebenen logischen Regeln
neues Wissen ableiten und logische *Inkonsistenzen* entdecken können;
etwas das sehr viel Geld und Probleme ersparen kann!
Der Nachteil ist dass das Erstellen solcher präzisen Datenmodelle sehr aufwendig
ist, man Experten benötigt und das Datenmodell evtl. schlecht wiederverwendbar ist,
also zuviele problemspezifische Annahmen im Modell getroffen wurden.
Im Kontrast dazu haben wir das Web,
googlen wir ein lokales Restaurant zeigt Google uns in einer Infobox
die Öffnungszeiten, das Jahr der Gründung, die Addresse und vieles mehr.
Das sind ebenfalls Daten aus verschiedenen Domänen, für gewöhnlich
auf der Webseite des Restaurants zur Verfügung gestellt die dann
von Google gelesen werden.
Spezifische Informationen in der Webseite sind, ebenfalls mit einem
standardisierten Vokabular, gekennzeichnet!
Das ist dasselbe Prinzip, allerdings ist dieses Vokabular,
genannt Schema.org, sehr breit gefächert und unterliegt
weniger logischen Beschränkungen.
Dass macht das Modell einfach wiederverwendbar!
</details>

<details>
<summary>
Selbst mit einem standarisierten Datenmodell müssen korrekte und inkorrekte Daten gehandhabt werden,
normalerweise setzen wir sogar voraus das uns ein Computer Fehlermeldungen mitteilt falls etwas schief gelaufen ist.
</summary>
Sobald mehrere Systeme Daten austauschen müssen oder ein Benutzer im Spiel ist
welcher Daten in eine Applikation eingibt muss mit fehlerhaften Daten gerechnet werden!
</details>


Daher ist es offensichtlich dass Fehlerbehandlung beim Erstellen eines Datenmodells mitbehandelt werden sollte.
Schließlich erwarten wir dass *eine App* oder Webseite korrekt funktioniert!

Die momentan standardisierte Modellierungssprache *OWL* mit der graphbasierte Datenmodelle erstellt werden können
basiert auf Logik, komplexe Eigenschaften können modelliert werden sodass Computerprogramme,
basierend auf der Logik, sogar neues Wissen ableiten können!
Allerdings können Bedingungen nicht so modelliert werden wie wir das gerne hätten,
also damit inkorrekte Daten gemeldet werden.


Erst im Jahr 2017 wurde die Entwicklung einer anderen Modellierungssprache abgeschlossen und deren Verwendung vom W3C Komitee empfohlen.
Diese Modellierungssprache ergänzt die logikbasierte Modellilerungssprache *OWL* mit Fehlerbehandlung, eine Sprache namens SHACL:
konkrete Bedingungen was in einem gewissen Kontext korrekt und was inkorrekt ist können nun modelliert werden!
*Was einfach klingt ist der Startschuss für meine Forschung ...*

# Meine Forschung - Teil 1: Methoden der Wissensverarbeitung

Im folgenden beschreibe ich kurz meine Forschung zu Methoden der Datenmodellierung
und benutzerfreundlichen Visualisierungen von *Bedingungen* für graphbasierten Wissensmodellen.

Professionelle Softwareentwicklung ist nicht nur Programmierung,
es geht um ingenieursmäßig definierte Schritte um qualitativ hochwertige Software zu erstellen,
das schließt auch Prozesse wie das Sammeln von Anforderungen,
das Erstellen von Dokumentation und das Schulen von Benutzern mit ein.

Ähnliche Methoden wurden von Wissenschaftlern für die Erstellung von graphbasierten Datenmodellen vorgeschlagen
und in etlichen Projekten für nützlich befunden.

Leider sind diese Methoden im Detail nicht sehr genau und decken
vor allem Anforderungen an Datenqualität nur unzureichend ab!
Um genau zu sein: das eigentliche Modellieren von Bedingungen wird der Erfahrung des Modellierers überlassen
und folgt daher keiner messbaren Methodik.

Grundannahme meiner Forschung ist das jedoch einige Anforderungen an Datenqualität bereits bei
der Definition vom Zweck des Datenmodells und beim Sammeln der Anforderungen bekannt sind.
Außerdem ist es für einen Einsteiger nicht ersichtlich welche Anforderungen
besser als Logik ins Datenmodell gepackt werden sollen und welche als externe Bedingungen
um fehlerhafte Daten zu entdecken.

Um diese Probleme zu Lösen entwickle Ich Methoden um solche 
Anforderungen aus existierenden Datenmodellen zu extrahieren
oder von Domänenexperten in Erfahrung zu bringen.

Dabei erfinde ich das Rad nicht neu,
ich habe mich intensiv in die Literatur zur Wissensmodellierung eingearbeitet und tue es immer noch!
Das Ziel ist es bestehende Methoden soweit wie möglich wiederzuverwenden
sie jedoch für die Modellierung von Bedingungen anzupassen.
Dazu gehört auch zu analysieren welche messbaren Vor- und Nachteile es bringt
gewisse Bedingungen entweder als Logik des Datenmodells oder anderweitig zu modellieren.
Ein Beispiel meiner Doktorarbeit sind Datenschutzbestimmungen.
Um die Einhaltung von Datenschutzbestimmungen zu überprüfen muss einerseits
das Datenmodell relevante Informationen hergeben aber womöglich auch
Regeln in der Form von Bedinungen.

# Meine Forschung - Teil 2: Benutzerfreundliche Visualisierungen

In meinem Labor arbeiten wir hauptsächlich an verschiedenen Projekten mit Industrie, Behörden und Institutionen.
Die Erfahrung aus diesen Projekten hat andere Probleme offenbart:
Die 2017 neu vorgestellte Sprache um Bedingungen zu modellieren ist textbasiert,
Nutzer müssen diese Sprache erst erlernen was nicht ohne Tücken ist!

Menschen besitzen ein erstaunliches Informationsverarbeitungssystem, ..
nein, ich rede nicht vom Smartphone in der Hosentasche sondern vom Gehirn!
Aus der Kognitionswissenschaft wissen wir das Text langsam verarbeitet wird da wir mehr Konzentration aufbringen müssen.

Im Gegensatz dazu werden Formen und Farben fast schon automatisch und daher ohne sichtliche Mühe erkannt.
Wir arbeiten mit graphbasierten Wissensmodellen welche sehr greifbar sind, das machen wir uns zu Nutze!

Wir entwickeln grafische Sprachen um die Bedinungen auf unser graphbasiertes Wissensmodell zu beschreiben.
Unter der Annahme dass solche grafischen Sprachen *intuitiver* sind als eine fremde Textsyntax,
untersuchen wir in Studien welche grafischen Sprachen sich am besten eignen und
wie wir sie anpassen müssen.

![Me presenting my poster at the ISWC doctoral consortium in 2019](/img/2019-11-05-iswc-poster-sven.jpg)
