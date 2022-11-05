---
title: 'Assessing, Creating and Using Knowledge Graph Restrictions'
share: false

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin

date: 2022-03-10T13:37:00+02:00
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: 2022-03-10T13:37:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['5']

# Publication name and optional abbreviated publication name.
publication: " PhD dissertation, Ghent University, Belgium"
publication_short: "PhD dissertation"

tags: ['knowledge graph', 'axioms', 'constraints', 'RDF', 'SHACL']

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

#url_pdf: "/en/publication/phd.pdf"
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: "https://doi.org/10.5281/zenodo.7258477"
url_video: "https://www.youtube.com/watch?v=NofQSwc3Svk"
url_source: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Chapter structure of my PhD thesis'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ''
---

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
