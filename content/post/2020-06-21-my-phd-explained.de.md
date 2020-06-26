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
image = ""
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
ebenfalls Anforderungen an Datenqualität erfüllen.
Im speziellen befasse ich mich einerseits mit Methoden der Wissensverarbeitung (Knowledge Engineering),
und andererseits mit benutzerfreundlichen Visualisierungen von Bedingungen in graphbasierten Wissensmodellen (data constraints).

# Das große Ganze

Das Kombinieren von Daten aus verschiedenen Bereichen,
auch Domänen genannt, hat großes Potential.
<details>
  <summary>Kombinieren von Daten (klick mich um mehr zu erfahren)</summary>
"Alexa, schalte die Heizung an wenn ich im Homeoffice bin, es weniger als 18 Grad Celsius hat und die Kilowattstunde Strom nicht mehr als x Euro kostet".
Was wenn das Thermometer nur Daten in Fahrenheit zur Verfügung stellt?
Was wenn keine Informationen zu aktuellen Preisen vorliegen?
Und was ist überhaupt Homeoffice, wie kann Alexa das feststellen?
Ein Heizungssystem besteht aus vielen Sensoren, mein Kalender besteht aus vielen Daten
und eine Gemeinde publiziert oft Statistiken oder andere Informationen als "Open Data".
All diese Daten sind in verschiedenen Formaten und jeder der sich versucht eine nützliche App
zu Entwickeln welche alle drei Datenquellen verwendet muss das evtl.
für jedes Heizungsszstem, jede Kalenderapplikation oder jede Gemeinde aufs neue tun!
Standards helfen das Leben einfacher zu machen, ein Smartphone Ladekabel passt in jede Steckdose
in einem Land.
Dasselbe Prinzip gilt auch für Daten, folgen zum Beispiel alle Heizungshersteller einem Standard
Datenmodell kann eine App für verschiedene Heizungsanlagen verwendet werden.
Leider ist so ein Standard auf einen Bereich beschränkt,
und warum sollte ein Heizungsstandard auch Kalenderinformationen oder Strompreise definieren?!
</details>

Aber um Daten aus verschiedenen Domänen sinnvoll zu kombinieren ist ein
gemeinsames Verständnis in der Form eines standardisierten Vokabulars, einem Datenmodell, nötig:
Die Temparaturmessung eines Heizungssystems in Grad Celsius sollte nicht einfach
mit einer Temparaturmessung in Fahrenheit oder gar mit meinem Lebensalter verrechnet werden!
<details>
  <summary>Sinnvolles kombinieren von Daten? (klick mich um mehr zu erfahren)</summary>
Hierfür verwende Ich eine vom World Wide Web Consortium (W3C) empfohlene graphbasierte Sprache.
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


Ein standardisiertes Vokabular sollte detailliert genug sein
um Fragen zu beantworten die wir evtl. haben: es muss seinen Zweck erfüllen.
<details>
  <summary>Der Zweck eines Datenmodells? (klick mich um mehr zu erfahren)</summary>
</details>


Obwohl sehr präzise und sinvolle Datenmodelle unverzichtbar für manche Zwecke sind,
birgt deren Komplexität Nachteile für viele andere Zwecke.
<details>
  <summary>Komplexität eines Datenmodells? (klick mich um mehr zu erfahren)</summary>
</details>

Selbst mit einem gemeinsamen Datenmodell müssen korrekte und inkorrekte Daten gehandhabt werden,
normalerweise setzen wir sogar voraus das uns eine Maschine Fehlermeldungen mitteilt falls etwas schiefgelaufen ist.

Daher ist es offensichtlich dass Fehlerbehandlung teil des Datenmodells sein sollte
damit es seinen Zweck erfüllt, schließlich erwarten wir dass *die Maschine* korrekt funktioniert!

Die momentan häufig verwendete Modellierungssprache um graphbasierte Datenmodelle zu erstellen
basiert auf Logik, komplexe Eigenschaften können modelliert werden sodass Computerprogramme,
basierend auf der Logik, sogar neues Wissen ableiten können!


Erst im Jahr 2017 wurde eine Sprache vorgestellt welche diese Modellierungssprache ergänzt,
konkrete Bedingungen was in einem gewissen Kontext korrekt und was inkorrekt ist können nun modelliert werden.

# Meine Forschung

Professionelle Softwareentwicklung ist nicht nur Programmierung,
es geht um ingenieursmäßig definierte Schritte um qualitativ hochwertige Software zu erstellen,
das involviert auch Prozesse wie das sammeln von Anforderungen und Schulen von Benutzern.

Ähnliche Methoden wurden von Wissenschaftlern für die Erstellung von graphbasierten Datenmodellen vorgeschlagen.

Leider sind diese Methoden im Detail nicht sehr genau und decken vorallem Anforderungen an Datenqualität nicht ab!

Grundannahme meiner Forschung ist das jedoch Anforderungen an Datenqualität bereits bei
der Definition vom Zweck des Datenmodells und beim sammeln der Anforderungen bekannt sind.

Ich entwickle Methoden um solche Anforderungen aus existierenden Datenmodellen zu extrahieren
oder von Domänenexperten in Erfahrung zu bringen.
