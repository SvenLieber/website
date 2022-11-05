---
title: "Meine Doktorarbeit erklärt"
subtitle: An early attempt in 2020
share: false

slug: "meine-doktorarbeit-erklaert"

# Link this post with a project
projects: []

# Date published
date: 2020-06-21T16:28:14+02:00

# Date updated
lastmod: 2020-06-21T16:28:14+02:00

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - PhD
  - ontologies
  - constraints

categories:
  - explained
---

Es ist besonders schwierig die eigene Dokotorarbeit der Familie und Freunden zu erklären,
gerade in so einem abstrakten Gebiet wie der Informatik.
Im folgenden Blogpost werde Ich versuchen meine Doktorarbeit zu erklären,
befreit von akademischer Genauigkeit und mehr mit dem Großen und Ganzen im Blick.

<!--more-->

Die Abschnitte sind eine zusammenhängende Story,
aber jeder Paragraph der mit einem Pfeil markiert ist kann bei Bedarf angeklickt werden um mehr zu erfahren.

# Der Kontext
Habt Ihr euch je gefragt wie ein Assistenzsystem wie Alexa oder Siri
Antworten auf beliebige Fragen finden kann?
Dazu muss so ein System Daten von unterschiedlichen Fachbereichen,
auch Domänen genannt, durchsuchen können.

Dafür bietet es sich an Daten auf natürliche Weise zu verbinden,
man muss sich das ganze wie einen Graphen vorstellen:
**Knoten** sind Dinge wie konkrete Personen und **Verbindungen**
zwischen den Knoten sind die Beziehungen zwischen diesen Dingen.
Als Text kann so ein Graph zum Beispiel so aussehen: 

```
Sven hatGeburtstag 25.04.1988 .
Sven arbeitetFür IDLab .
IDLab hatFirmensitzIn Belgien .
Belgien gehörtZu Europa .
```

<details>
<summary>
**Was** jedoch **wie** miteinander unter **welchen Bedingungen** verlinkt werden kann und soll
muss man aber erst einmal festlegen, das wird **Datenmodell** genannt.
In diesem Beispiel kann mein Arbeitgeber IDLab, welches eine Organisation ist, keinen Geburtags haben,
ebenso kann Sven keinen Firmensitz haben da er eine Person ist.
Und im großen und ganzen forsche Ich daran wie solche Datenmodelle erstellt werden können.
</summary>
Datenmodellierung ist nichts neues, anstatt jedoch wie bisher Daten nur für
eine einzelne Datenbank oder ein einzelnes Computerprogramm zu Erstellen
machen wir uns Das World Wide Web zu nutze.
Jedes Konzept und jede Beziehung, so wie `Person` und `hatFirmensitzIn`
aber auch konkrete Daten selbst, so wie `Sven` oder `Belgien`
bekommen eine eigene Webadresse.
Damit sind sie global eindeutig identifizierbar und sowohl Computerprogramme
wie auch Benutzer können das Konzept oder die Information nachschlagen!
Das kann dann so wie auf der folgenden Seite aussehen: https://sven-lieber.org/profile
</details>

# Meine Forschung - Teil 1: Der Datenmodellierungsprozess

Nun kann jeder so ein Datenmodell in einem Nachmittag erstellen,
das ist nicht die Kunst.
Die Herausforderung ist das ganze professionell zu machen
damit am Ende ein qualitativ hochwertiges Datenmodell herauskommt.
Ideallerweise solle das Datenmodell so konstruiert sein
das es die Probleme löst weswegen es erstellt worden ist!
Für die Frage "Wie ist das Wetter heute in Gent?"
muss das Datenmodell beispielsweise zumindest
die Konzepte *Wetter* und *Stadt* aber auch *zeitliche Informationen* enthalten.

<details>
<summary>
Nun kann ein Datenmodell einfach und wiederverwendbar entwickelt werden,
oder sehr komplex und auf ein konkretes Problem zugeschnitten.
</summary>
Ein Beispiel für ein einfaches und wiederverwendbares Datenmodell ist das folgende.
Wenn Ihr irgend ein Geschäft googelt zeigt euch Google rechts in einer
Infobox zum Beispiel Öffnungszeiten oder das Gründungsjahr des Geschäfts.
Das kann unter anderem gemacht werden weil die Webseitenbetreiber
ein standardisiertes Datenmodell verwendet haben um Informationen
in Ihrer Webseite zu kennzeichnen.
Dafür wird nicht viel Genauigkeit verlangt da die Information hauptsächlich
menschlichen Nutzern angezeigt wird.
Im Gegensatz dazu werden in der *Biomedizin* sehr komplexe Datenmodelle
verwendet welche logischen Regeln folgen.
Diese sind so präzise das selbst Computerprogramme sie "verstehen können"
</details>

<details>
<summary>
Für gewöhnlich muss man beim Erstellen eines Datenmodells mit
vielen Verantwortlichen und Experten sprechen,
existierende Daten analysieren und eine Ahnung von existierenden
Datenmodellen haben.
Schließlich soll das Datenmodell einheitlichen Standards folgen
und nahtlosen Datenaustausch mit anderen Datenmodellen, auch interoperabilität genannt, fördern.
**Das ganze ist also ein komplexer Prozess den man in Schritte
aufteilen kann.**
</summary>
Das ist übrigens auch in der professionellen Softwareentwicklung,
dem Software Engineering so.
Eine ingenieursmäßige Herangehensweise in Form von meßbaren und
optimierbaren Prozessen unterscheidet Software Engineering
vom simplen Akt der *Programmierung*.
</details>

Der erste Teil meiner Forschung dreht sich um diesen Prozess.
Ich gehe der Frage nach **wie man Bedingungen im Datenmodell am besten
repräsentiert**, wie man also ein Datenmodell erstellen kann das
nicht zu simpel aber auch nicht zu komplex ist für ein gegebenes Problem ist.
Bedingungen können einerseits logische Schlußfolgerungen wie `Alle Lebewesen haben ein Geburtstadum` sein,
aber auch testbare Eigenschaften wichtig für Datenaustauch und Datenqualität so wie `Das Geburtsdatum muss kleiner als das Sterbedatum sein`.

Dabei erfinde ich das Rad nicht neu,
ich habe mich intensiv in die **Literatur zur Wissensmodellierung** eingearbeitet und tue es immer noch!
Das Ziel ist es bestehende Methoden soweit wie möglich wiederzuverwenden
sie jedoch für die Modellierung von Bedingungen anzupassen.
Dazu gehört auch zu analysieren welche messbaren Vor- und Nachteile es bringt
gewisse Bedingungen entweder als Logik des Datenmodells oder als testbare Bedinungen zu modellieren.
Ein Beispiel meiner Doktorarbeit sind Datenschutzbestimmungen.
Um die Einhaltung von **Datenschutzbestimmungen** zu überprüfen muss einerseits
das Datenmodell relevante Informationen hergeben aber womöglich auch
Regeln in der Form von testaren Bedinungen.

# Meine Forschung - Teil 2: Benutzerfreundliche Visualisierungen

In meinem Labor arbeiten wir hauptsächlich an verschiedenen Projekten mit Industrie, Behörden und Institutionen.
Die Erfahrung aus diesen Projekten hat konkrete **Probleme der Benutzerfreundlichkeit** von Modellierungssprachen offenbart:
Eine erst 2017 neu vorgestellte Sprache um testbare Bedingungen in Graphmodellen auszudrücken ist textbasiert,
Nutzer müssen diese Sprache erst erlernen was nicht ohne Tücken ist!

**Bilder sagen mehr als tausend Worte.**
Jedoch besitzen Menschen ein erstaunliches Informationsverarbeitungssystem, ...
nein, ich rede nicht vom Smartphone in der Hosentasche sondern vom Gehirn!
Aus der Kognitionswissenschaft wissen wir das Text langsam verarbeitet wird da wir mehr Konzentration aufbringen müssen.
Im Gegensatz dazu werden Formen und Farben fast schon automatisch und daher ohne sichtliche Mühe erkannt.
Wir arbeiten mit graphbasierten Wissensmodellen welche sehr greifbar sind, das machen wir uns zu Nutze!

**Wir entwickeln grafische Sprachen** um die Bedinungen auf unser graphbasiertes Wissensmodell zu beschreiben.
Unter der Annahme dass solche grafischen Sprachen *intuitiver* sind als eine fremde Textsyntax,
untersuchen wir in Studien welche grafischen Sprachen sich am besten eignen und
wie wir sie anpassen müssen.

# Und warum das Ganze?

**Daten ohne Beschreibung sind nutzlos.**
Stellt euch vor Ihr findet einen Zettel mit vielen Nummern.
Ganz ohne Kontext habt ihr keine Ahnung was die Nummern bedeuten.
Evtl. existiert irgendwo ein Computerprogramm das genau
weiß wie die Nummern auf diesem Zettel zu interpretieren sind,
für euch oder auch fuer andere Programme ist dieser Zettel jedoch nutzlos!

**Das Hinzufügen von Beschreibungen gibt Kontext und macht die Daten selbstbeschreibend
und dadurch interpretierbar.**
Notiert ihr dass die erste Spalte auf dem Zettel Gewicht gemessen in Kilogramm ist
und dass die zweite Spalte jeweils ein Geburtsdatum ist
und dass beides Eigenschaften einer Person sind deren Name
in der dritten Spalte steht habt ihr Datenmodellierung betrieben!
Außerdem sind die Daten nun selbtbeschreibend und unabhänging von
speziellen Computerprogrammen.
Übrigens: Dieser Zettel kann stellvertretend für eine Datei oder eine Webseite stehen.

Wenn Daten gut beschrieben sind lassen sie sich *sinnvoll kombinieren*
und solch kombinierte Daten lassen sich dann schneller, einfacher
und vorallem einheitlich Durchsuchen was sich dann **Systeme wie Alexa oder Siri zu Nutzen machen!**
Eine nicht sinvolle Kombination ist zum Beispiel das Verrechnen
einer Temparatur in Grad Celsius mit meinem Lebensalter in Jahren.

# Zusammengefasst

Anhand des gelesenen können wir also jetzt zusammenfassen:
**Ich beschäftige mich mit Datenmodellierung.**
Ich gehe der Frage nach
wie wir graphbasierte Wissensmodelle erstellen können welche 
ebenfalls Anforderungen an Datenqualität oder Datenschutzbestimmungen erfüllen.
Im speziellen befasse ich mich einerseits mit Methoden im Modellierungsprozess (Knowledge Engineering),
also welche Schritte durchgeführt werden müssen um Wissensmodelle zu erstellen,
und andererseits mit benutzerfreundlichen Visualisierungen von Bedingungen in graphbasierten Wissensmodellen (data constraints),
damit auch *Nicht-Experten* solche Bedingungen erstellen können.

**So, das wars!
Ich hoffe ich konnte ein wenig Licht ins Dunkle bringen :-)**

Nachfolgend noch ein Bild von der ISWC 2019 Konferenz
bei der ich den Plan meiner Doktorarbeit als Präsentation und als Poster
vorgestellt habe (mein Reisebericht zu dieser Konferenz welche in Neuseeland stattgefunden hat ist [hier](https://sven-lieber.org/en/2019/11/05/iswc-2019/), momentan leider nur in Englisch).

![Me presenting my poster at the ISWC doctoral consortium in 2019](/img/2019-11-05-iswc-poster-sven.jpg)
