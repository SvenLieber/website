+++
title = "Assessing, Creating and Using Knowledge Graph Restrictions"
date = 2022-03-10T13:37:00+02:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Sven Lieber"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = ["5"]

# Publication name and optional abbreviated version.
publication = " PhD dissertation, Ghent University, Belgium"
publication_short = "PhD dissertation"

# Abstract and optional shortened version.
abstract = ""
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
#projects = ["besocial"]

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Knowledge Graph", "Axioms", "Constraints", "RDF", "SHACL"]

# Links (optional).
url_pdf = "/en/publication/phd.pdf"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = ""
url_slides = "https://www.slideshare.net/SvenLieber/assessing-creating-and-using-knowledge-graph-restrictions"
url_video = "https://www.youtube.com/watch?v=NofQSwc3Svk"
url_poster = ""
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
image = "2022-03-10-phd-thesis-structure.jpg"
caption = ""

+++


Mehr und mehr Daten werden erzeugt, aber die sinnvolle Beantwortung von Fragen mit diesen Daten ist nicht einfach, da wir ein gemeinsames Verständnis darüber benötigen, was die verschiedenen Daten bedeuten und wie sie zusammenhängen.
Wissensgraphen mit Konzepten und Verbindungen zwischen Konzepten bieten eine flexible Möglichkeit, Informationen darzustellen: "Sven (Ding) schreibt (Verbindung) Dissertation (Ding)“ und "Sven (Ding) ist eine (Verbindung) Person (Ding)."
Die technologische Basis dieser Graphen kann das Web sein, wobei Komponenten des Graphen Webadressen sind, sodass Menschen und Maschinen Komponenten des Graphen nachschlagen können.

Allerdings muss man mögliche Verbindungen im Graphen so benschränken, dass auch ein Computer daraus einen Sinn machen kann.
Sonst kann eine "Dissertation (Ding)  Luft (Ding) atmen (Verbindung)", was keinen Sinn macht und zu falschen Dateneinsichten führt.
Benschränkungen können entweder unter Verwendung von Axiomen ausgedrückt werden, um eine formale Bedeutung bereitzustellen, oder als lokale Einschränkungen, um Daten zu validieren.

Diese Doktorarbeit befasst sich mit der Unterstützung von Benutzern bei der Bewertung, Erstellung und Verwendung von Einschränkungen des Knowledge Graph.
Konkret wird in dieser Dissertation die FAIR Montolo-Statistiken beigesteuert, die Benutzer bei der Bewertung bestehender Knowledge Graphs auf der Grundlage verwendeter Benschränkungen unterstützt.
Die beiden visuellen Notationen ShapeUML und ShapeVOWL werden vorgestellt und evaluiert: Sie repräsentieren alle Constraint-Typen der Shapes Constraint Language (SHACL) und bringen damit den Stand der Technik voran.
Schließlich wird die Verwendung von Benschränkungen zur Darstellung formaler Bedeutung und zur Bewertung der Datenqualität für einen Anwendungsfall der Archivierung von sozialen Medien im BESOCIAL-Projekt der Königlichen Bibliothek von Belgien (KBR) demonstriert.

