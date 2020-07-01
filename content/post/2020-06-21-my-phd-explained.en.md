+++
title = "My PhD explained"
date = 2020-06-21T16:28:14+02:00
draft = false
slug = "my-phd-explained"

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

It is particularly challenging to explain PhD research to family and friends,
especially in an abstract field such as Computer Science.
In the following blog post I will try to explain my PhD,
freed from academic precision and more from the big picture and with plenty of examples.

<!--more-->

**To summarize it in one sentence: I deal with data modeling.**
I pursue the question how we can build data models of knowledge graphs
which also comply with requirements towards data quality and privacy.
In particular I investigate on the one hand methods of knowledge engineering,
so which steps need to be performed to create such knowledge graphs,
and on the other hand the user-friendly visualization of data constraints.

# The big picture

The bullet points form one coherent story,
but each paragraph marked with an arrow can be clicked to read more details.

<details>
<summary>There is great potential in combining data from diverse fields, called domains.</summary>
Information from different domains is necessary to execute the following example order.
"Alexa, turn the heating on if I am in home office, if it has less than 18 degrees celsius
and if the kilowatt hour energy costs less than x Euro".
What if the thermometer only provides data in Fahrenheit?
What when no information regarding pricing is available?
And what is even "home office", how can Alexa determine this?
A heating system consists of plenty of sensors, my calendar consists of a lot of data
and a municipality often publishes statistics or other information as "Open Data".
All these data are in different formats
and everyone who tries to develop a useful app which uses all three data sources
might have to develop it for every heating system, every calendar application
or each municipality again.
Standards help to make lives easier,
a smartphone charger fits in each power plug of a certain country.
The same principle also applies on data, if for example all heating system manufacturer
follow one standard data model an app can be reused across multiple heating system models.
Unfortunately such a standard is limited to one domain,
and why would a heating system standard define calendar information or energy prices?!
</details>

<details>
<summary>But to combine data from different fields in a *meaningful* way
a common understanding in the form of a standardized vocabulary (data model) is needed:
A temperature measurement in Celsius should not be added to a
measurement performed in Fahrenheit or even to my age!
</summary>
Therefore I am using the Resource Description Framework ([RDF](https://www.w3.org/TR/2014/REC-rdf11-concepts-20140225/)) a graph-based language recommended by the world wide web consortium (W3C).
Every *thing* and every possible *relationship* between *things* will get an own web address!
Hence *everything* is uniquely identifiable and because everything follows the same graph structure,
a *heating system* can relate via a *serial-number*-relationship to a *number*
but also via a *belongs-to*-relationship to *me*.
It can also be specified that a concrete *measurement* is of type *Celsius*.
I in turn can be in multiple relationships to personal information such as my *bloodtype*
or my *date of birth*.
The big plus: computer programs can look up these "websites"
and read and interpret the definition of *things* and *relationships*.
Additionally such a graph can be searched for information in a uniform way
no matter if it is information regarding my heating or regarding me.
</details>

<details>
<summary>
Such a shared vocabulary which consists of concepts, relationships among the concepts
and *meaning* in the form of restrictions
should be detailed enough to answer questions we initially have,
in other words: it should fulfill its purpose.
</summary>
A first step in knowledge engineering is the collection of requirements,
e.g. in the form of questions.
Therefore, in a later step of knowledge engineering, it can be checked
if the data model fulfills its purpose,
if initially asked questions can be answered.
</details>


<details>
<summary>
Although very precise and meaningful data models are indispensable for some use cases,
their complexity comprises drawbacks in a lot of other cases.
</summary>
Very precise data models in RDF are often created
for the domains of *bio engineering* and *engineering*.
These data models are so prceise that special programs
can infer new knowledge based on the given logical rules
and detect inconsistencies;
something which saves lots of money and problems.
The downside is that the creation of such precise models is cumbersome,
experts are needed and the reusability is hampered,
meaning that too much problem specific assumptions were made in the model.
In contrast to this we have the web,
if we google a local restaurant Google shows us in an infobox
the opening hours, the founding year, the address and much more.
These are also data from different domains,
usually provided on the website of the restaurant which is
taken into account by Google.
Specific information in the website are
marked with standardized vocabularies.
This is the same principle but this vocabulary
named schema.org is very broad and is subject to less logical restrictions.
This makes the model easier reusable!
</details>

<details>
<summary>
Even with a common data model correct and incorrect data need to be handled,
usually we even expect error messages from computers if something is incorrect.
</summary>
As soon as multiple systems have to exchange data or as soon as a human user is involved
who inserts data via an application one has to consider incorrect data.
</details>


So it is apparent that error handling should be considered when developing data models.
Eventually we expect that *an app* or website works property!

The currently standardized modeling language *OWL* with which knowledge graphs can be build
is based on logic.
Complex characteristics can be modeled such that computer programs,
based on this logic, can infer new knowledge!
However, constraints are not modeled in a way how we might expect it to be,
in the sense of detecting incorrect data.

Just in the year 2017 the development of another modeling language was finished
and its use recommended by W3C.
This modeling language complements the logic-based language *OWL* with error handling capabilities, a language called SHACL:
concrete constraints describing what is valid in a certain context and what is invalid can now be modeled!
*What sounds easy is the begin of my research ...*

# My research - part 1: knowledge engineering

In the following I will briefly explain my research regarding knowledge modeling
and user-friendly visualizations of knowledge graph constraints.

Professional software engineering is not just programming,
it is about engineering, defined steps to develop qualitatively high software.
This includes processes such as the collection of requirements,
the creation of documentation or the training of users.

Similar methods were proposed by researchers for knowledge modeling
and found useful in plenty of projects.

Unfortunately these methods are not very detailed and
do especially cover requirements towards data quality only insufficiently.
To be precise: the *actual* modeling of restrictions is left to the experience of the modeler
and, thus, does not follow a measurable methodology.

The basic assumption of my research is that several requirements towards data quality
are already known at design time, e.g. when the requirements are collected.
Additionally for beginners it is not obvious which requirements
should better be placed within the logic of the data model and which
in form of external constraints to detect erroneous data.

To solve these problems I develop methods to extract requirements
from existing data models or from domain experts.

Thereby I do not reinvent the wheel,
I carefully read the literature of knowledge modeling and I still do!
The goal is to reuse existing methods as much as possible
but to adapt them to the modeling of constraints.
Part of this is also to analyze which measurable pros and cons arise
certain restrictions are either expressed as logical axioms in the data model or elsewhere.
One use case in my PhD are privacy regulations.
To check compliance with privacy regulations on the one hand
the data model needs to provide relevant information
and on the other hand constraints are possibly needed.


# My research - part 2: user-friendly visualizations

In my lab we mostly work in different projects together with industry, the government or institutions.
The experience of this projects revealed other problems:
The 2017 newly introduced language is text-based,
user have to first learn it which might be tricky!

Humans possess an astonishing information processing system, ..
no, I do not talk about the smartphone in the pocket but about the brain!
From cognitive science we know that text is processed slowly as we have to concentrate more.

In contrast to that shapes and colors are almost automatically processes
with no visible effort.
We work with knowledge graphs which are tangible, we take advantage of that!

We develop graphical languages to describe constraints on our knowledge graphs.
Based on the assumption that such languages are *more intuitive* compared to an alien text syntax
we examine in user studies which graphical languages are suited best.

![Me presenting my poster at the ISWC doctoral consortium in 2019](/img/2019-11-05-iswc-poster-sven.jpg)
