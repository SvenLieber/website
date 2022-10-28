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
url_slides = "https://doi.org/10.5281/zenodo.7258477"
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

More and more data is created, but meaningfully answer questions with this data is not straightforward because we need a shared understanding of what the different data means and how it relates.
Knowledge Graphs with concepts and relationships offer a flexible way to represent information: "Sven (thing) writes (relationship) dissertation(thing)" and "Sven (thing) is a (relationship) Person (thing)".
The technological basis of these graphs can be the web, where components of the graph are web addresses, thus humans and machines can look up components of the graph.

However, one has to restrict possible connections in the graph such that also a computer can make sense out of it. 
Otherwise a "dissertation (thing) can breathe (relationship) air (thing)", which does not make any sense and leads to wrong insights of data.
Restrictions can either be expressed using axioms to provide formal meaning or as local constraints to validate data.

This doctoral thesis tackles the support of users when assessing, creating and using Knowledge Graph restrictions.
More concretely, in this dissertation the FAIR Montolo statistics are contributed, supporting users in assessing existing Knowledge Graphs based on used restrictions.
The two visual notations ShapeUML and ShapeVOWL are presented and evaluated: they represent all constraint types of the Shapes Constraint Language (SHACL) and thus advance the state of the art.
Finally, the use of restrictions to represent formal meaning and to assess data quality is demonstrated for a social media archiving use case in the BESOCIAL project of the Royal Library of Belgium (KBR).
