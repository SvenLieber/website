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
url_slides = "https://www.slideshare.net/SvenLieber/linked-data-generation-for-adaptive-learning-analytics-systems"
url_video = ""
url_poster = "https://www.slideshare.net/SvenLieber/poster-linked-data-generation-for-adaptive-learning-analytics-systems"
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

Did you ever use a language learning app and were annoyed that the exercises are either too easy or too hard?
That are actually reasons people give up.
Well, probably you would profit from adaptive learning systems, which adapt the difficulty of the exercises to your abilities!
Providing Adaptive Learning Analytics Systems with data to do that, is one part of a [project](https://www.imec-int.com/en/what-we-offer/research-portfolio/leaps) I am currently working on.
<!--more-->

This paper which was accepted at the Linked Learning ([LILE](https://lile2018.wordpress.com/)) workshop at the [WebScience2018](https://websci18.webscience.org/) conference describes
how we generate Linked Data out of learning activity data (logfiles generated when you are using an educational app).
Learn here what Linked Data is,
how it can help and how we also use something called [Provenance](https://sven-lieber.org/en/2017/04/07/what-is-provenance/) to assist the users of our system with data protection tasks.

# Problem
Adapting exercise difficulties to your abilities is possible using e.g. Machine Learning algorithms. These algorithms need to be trained and therefore need looooots of data!
But not just any data, the bare nature of an exercise needs to be described (is this an grammatical task? audio task?),
also YOU and users in general need to be described (do you have learning disabilities like dyslexia? what do you already know?) and of course these data then needs to be integrated.
Strictly speaking, the machine needs to understand that a certain concept like a disability relates somehow to certain other concepts like grammar (which is then an essential part of an exercise).

# Solution
Describe exercises and users with the help of semantic technologies and doing that as additional step on already existing learning data.

How do we describe things semantically so machines can understand it? Therefore we are using Linked Data!
Basically Linked Data is a set of design principles. Every concept you describe, 

* should have an unique identifier (you say what a Person is and give it the unique name Person)
* needs to be dereferenceable (a machine using your concept of a Person should be able to look up what it means) => http://xmlns.com/foaf/spec/#term_Person would be unique and as it is a web resource also dereferenceable
* should be described using standards  (define your concept of a person using a standard like RDF ensures that a machine can read it)
* should re-use and link to other concepts already existing.

![Linked Data Example](/img/2018-06-23-ld-example.jpg)

In that picture you see an example of Linked Data, expressed as a graph. Different colors indicate the different domains the data comes from.
The data describing your performed learning activities (blue), data about you (and users in general) (green) and data regarding your abilities (yellow), the prefixes are shortcuts for an URI.

And there you see that we already successful integrated data from these different domains!

That looks like a nice solution, right? But how do we get the Linked Data?

We are not forcing anyone to change now the way they collect learning activity data. The only thing we require are learning activity data according to the [xAPI specification](https://github.com/adlnet/xAPI-Spec).
That is a structured text format, which is already used a lot.
The learning activity data are usually stored in special databases called Learning Record Stores.
Our solution works on top of that, meaning, we extract the data out of these databases.

Actually we built a small pipeline, which uses standard technologies like [JSON-LD](https://www.w3.org/TR/json-ld/) to lift the structured text data to actual Linked Data resources!

For each step in the pipeline, we also collect Provenance information which we make available as Linked Data as well.
Why that you may ask?! 
Well, current privacy law like the European General Data Protection Regulation (GDPR) grant persons whose private data are processed certain rights. They (or in that case you as well) can request to delete or correct data which is about you.
If such a request was made, the users of our application can query the generated Linked Data and based on the provenance information they see where the data comes from and when it was extracted, which enables then to delete or correct the personal data everywhere.

