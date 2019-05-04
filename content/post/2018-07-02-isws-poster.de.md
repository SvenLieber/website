+++
title = "ISWS 2018 Poster"
date = 2018-07-02T10:20:27+02:00
draft = false
slug = "isws-2018-poster"

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["ISWS summer school", "shapes", "constraints", "Italy"]
categories = ["other"]

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "2018-07-02-isws-poster-cover.jpg"
caption = ""
preview = true

+++

Für die ISWS summer school habe ich ein interaktives Poster vorbereitet. In diesem Blogpost erkläre ich worüber das Poster handelt und wie ich es erstellt habe.

<!--more-->

Mein diesjähriger Sommer startet mit der Teilnahme an der International Semantic Web Research Summer School ([ISWS](http://stlab.istc.cnr.it/isws/wordpress/)) in Bertinoro, Italien.
Teilnehmende wurden gebeten ein Poster mitzubringen welches unsere PhD Forschung beschreibt.
Meine aktuelle Forschung umfasst sogenannte Shapes (Formen), welche Daten in einem Informationsgraphen beschreiben.
**Weil Graphen und Formen sehr greifbare Konzepte sind** und die Hauptaufgabe eines Posters ist Feedback zu bekommen, gestalteten wir das Poster interaktiv.
Meine Betreuerin hat vorgeschlagen post-its zu verwenden, aber da ich eine Menge überschüssige kreative Energie übrig habe 
(und vermutlich versuche das Schreiben von Papern aufzuschieben), habe ich beschlossen ein Wissenspuzzle zu erstellen.

# Was ist der Kontext?
Im Semantic Web werden Informationen mittels Vokabularien aus Begriffen, deren Beziehungen zueinander und möglichen Einschränkungen ausgedrückt.
Die Kombination aus den genannten Vokabularien, Begriffsbeziehungen und Einschränkungen wird für gewöhnlich als Ontologie bezeichnet und kann mittels formaler Sprachen ausgedrückt werden.
Solch eine Formalisierung ermöglicht es Computerprogrammen die Daten "zu verstehen", aber auch neues Wissen abzuleiten.
Zum Beispiel, wenn ein Konzept namens Person modelliert wird und wir formal ausdrücken dass es eine "kennt" Beziehung zwischen Personen gibt die besagt das beide Personen
sich kennen, kann ein Programm von der Information "Sven kennt dich" ableiten, das auch du Sven kennst. 

# Was hat das mit Shapes zu tun?
Nunja, Einschränkungen in Ontologien werden verwendet um neues Wissen gemäß der Einschränkungen abzuleiten, und nicht um Daten zu validieren also beispielsweise das eine
konkrete Person mindestens einen Vor und Nachnamen haben muss.
Das hat viele verschiedene Gründe, welche den Rahmen dieses Blogposts sprengen würden.
Für den Rest des Blogposts ist das folgende wichtig, 
erst kürzlich wurde vom W3C Komitee eine Empfehlung ausgesprochen Einschränkungen als Shapes auf Daten auszudrücken um beispielsweise Daten zu validieren.

![Vorbereitung des Puzzles](/img/2018-07-02-puzzle-preparation.jpg)

# Okay okay, genug Hintergrund, worüber handelt den nun das Poster?
Ich arbeite momentan an einem Projekt, welches eine verbesserte Customer Journey beim Verwenden von öffentlichen Dienstleistungen zum Ziel hat.
Ein Beispiel: Beim einem Umzug müssen verschiedene Amtsgänge erledigt werden, zum Beispiel die Abmeldung des Wohnsitzes in der Gemeinde in der man lebt.
Amtsgänge müssen aber auch in der Gemeinde in die man zieht erledigt werden, um sich anzumelden oder aber auch einen Parkplatz vor der neuen Wohnung zu benatragen.
All diese Amtsgänge können als ein Workflow verstanden werden, welcher aus kleineren Schritten besteht.
Das Ziel dieses Projekts ist das Erstellen von städteübergreifenden maßgeschneiderten Benutzeroberflächen.
Dadurch interagiert ein Bürger augenscheinlich nur mit einem einzigen System, während im Hintergrund verschiedene Formulare auf verschiedenen Städtenwebseiten ausgefüllt werden.


![Puzzlestücke](/img/2018-07-02-poster-pieces.jpg)

**Die Anpassung ist der Kernpunkt!**
Neben einfachen Anpassungen wie beispielsweise das lediglich einmalige Abfragen der aktuellen Wohnsitzadresse
(oder sogar die Wiederverwendung dieser Information, denn eine Behörde hat diese Information bereits),
sind auch weitere Personalisierung denkbar.

Und da kommen Shapes ins Spiel!
Gegeben verschiedene Workflows bestehend aus verschiedenen Schritten, können Vorlieben als Shapes ausgedrückt werden und verwendet werden um optimale Schritte für eine Person auszuwählen.
In ähnlicher Weise können Kontextinformation wie beispielsweise welches Endgerät für die Anfrage verwendet wird, oder Informationen über spezielle Lebensumstände als
Einschränkungen abgebildet werden um optimale Schritte auszuwählen.

Für mein [Poster](https://www.slideshare.net/SvenLieber/knowledge-jigsaw-puzzle) habe ich nun Workflowschritte (Blau), Bedingungen für einen Schritt (Grau), und Transaktionen (Grün) mit bestehenden Systemen (Orange) modelliert.
Im einfachen Beispielpuzzle gibt es Shapes für sichere Transaktionen (https) und einige Bedingungen.

![Puzzlestücke auf dem Poster](/img/2018-07-02-puzzle-on-poster.jpg)


Das ist natürlich nur ein kleines Beispiel wie Workflowschritte modelliert werden könnten.

Von einem Forschungsstandpunkt ist es interessant zu Untersuchen wie Shapes verwendet werden können, 
herauszufinden wann ein Einsatz sinnvoll ist und wann es besser ist Einschränkungen anderweitig auszudrücken.
Wenn Shapes verwendet werden sollen, ist es außserdem interessant zu untersuchen ob Shapes 
lediglich nacheinander angewendet werden sollen oder ob sie auch in irgendeiner Weise kombiniert werden können.
Können wir neue Shapes ableiten?
Auch ein automatisches Reasoning wird interessant, gegeben einiger kontextbasierter und anderer Einschränkungen, können wir neue Shapes schlussfolgern?

Eine Menge möglicher Forschung!
**Ich bin auf viel Feedback während der Postersession gespannt.**
