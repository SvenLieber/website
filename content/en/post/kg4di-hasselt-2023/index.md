---
title: Knowledge Graphs for Data Integration - UHasselt 2023
subtitle: Network event summary
share: true


# Link this post with a project
projects: []

postDOI: 10.59350/rwmp4-kmt63
toc: true

# Date published
date: 2023-06-12T09:00:00+01:00

# Date updated
lastmod: 2023-06-12T09:00:00+01:00

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
  - workshop
  - Knowledge Graphs
  - Reasoning
  - SHACL
  - SPARQL
  - cardinality estimation
  - Machine Learning
  - Comunica
  - Hasselt
  - RDF
  - Belgium

categories:
  - events

metadata:
  authors:
    - name: Sven Lieber
      website: ''
      sameas:
        - name: 'Orcid'
          url: 'https://orcid.org/0000-0002-7304-3787'
        - name: 'Wikidata'
          url: 'https://www.wikidata.org/entity/Q59469449'


---

In June 2023 I attended a workshop in Hasselt, Belgium, organized by a research network on Knowledge Graphs and Data Integration.
Linked Data-based systems and declarative SPARQL queries somehow magically do all the work efficiently, but how?
For many people, presentations about _using_ Linked Data and SPARQL already seem very technical.
But this event went further, it covered the fundamental algorithms that power the Linked Data systems!
In this post I try my best to briefly summarize some of the talks and highlight the added value of those fundamental and often behind-the-scenes work.
<!--more-->

## Context
The [FWO](https://www.fwo.be/en/)-founded research network [_Knowledge Graphs and Data Integration_](https://u0152642.pages.gitlab.kuleuven.be/kg4di-fwo-network/)
organized a [workshop](https://www.uhasselt.be/knowledge_graphs_kg4di)
at the [Data Science Institute](https://www.uhasselt.be/en/instituten-en/dsi) of Hasselt University in Belgium.
As part of this workshop, a keynote about _a logical approach to model interpretability_ was given
by [Marcelo Arenas](https://marceloarenas.cl/) from the _Pontificia Universidad Catolica de Chile_.
Afterwards, several papers were presented in three different sessions: foundations, experience and exemplars, and processing and mining.
I will group my summaries in these categories as well.

**My overall takeaway** is that there is still plenty of research for Knowledge Graphs!
Not only for how to use them or how to encode knowledge in them,
but also for how to _actually implement_ Knowledge Graph software
based on formally sound techniques.

{{% callout note %}}
If you want to get notified about more content or want to receive weekly updates on FAIR and Linked Data,
please consider subscribing to my weekly Newsletter.
{{% /callout %}}
<iframe src="https://fairdata.substack.com/embed" width="100%" style="border:1px solid #EEE; background:white;" frameborder="0" scrolling="no"></iframe>

{{< toc >}}


## Keynote

Before I focus on the keynote itself I would like to start with an example.
Recently in a show of the Flemish comedian [Lieven Scheire](https://www.lievenscheire.be/),
I heard about a Machine Learning (ML) algorithm that was trained to distinguish images
from wolves and from huskies. The algorithm seemed to perform very well, but not always.
Later, by trying out a few things, it turned out the algorithm apparently "learned" that the distinguishing factor is a white background (snow).
So if there was white background, the animal on the image was classified as a husky image by the ML model.

This is just an example to illustrate that we don't actually know what a ML algorithm/model has learned and thus _why_ a certain output is generated.
That's why such models are usually called a _black box_. But in a world in which more and more ML enters our daily lives, 
**it is absolutely fundamental that we are able to explain why the model behaves in a certain way.**

### Explaining predictions of ML models
In simple terms, the keynote of [Marcelo Arenas](https://marceloarenas.cl/)
presented some fundamental research in early stages that tries to specify a declarative query language (think of SQL or SPARQL) for ML models. 
The keynote lecture had some very nice examples to illustrate the graph algorithms.
But why graphs actually?

Machine Learning models are usually based on so-called "neural networks"
that are inspired by neurons in the human brain.
These neural networks  that may consist of several layers of neurons
"learn" patterns by adjusting how information flows through the connections between the nodes.
This is not a Knowledge Graph in a Linked Data-based sense
in which you explicitly encode information that you can query later.
**But it is a graph and hence one can perform graph algorithms that include some sort of queries.**

### A logic-based query language for ML models
In his talk, Marcelo explained how they define theoretical logics for operations on such graphs. Their overarching goal is to develop a declarative query language, such as SPARQL, but for neural networks.
This is not purely theoretical as they also implemented their "FOIL" logic using a special logic programming language that is different to languages such as Python or Java that you may know. Like this the theories can be tested with real life data and it can be observed how effective they are with specific data (besides the theoretical complexity).
If you are interested in more, here you can find a preprint of an earlier paper: https://arxiv.org/abs/2110.02376


## Foundations

From this session, I will focus on three of the talks. Two that focus on effective computations
and one about reliable query languages.

### Graph compression
The work of [Jeroen Bollen](https://twitter.com/jbinero)
is motivated by the fact that memory is often a bottleneck for so-called Graph Neural Networks. 
There are ways to compress the graphs.
But so far there haven't been any formal proofs showing that the accuracy of the algorithm
remains stable with differently compressed graphs.

In his talk, Jeroen presented his work where he showed that
they could minimize computational and memory requirements
while keeping a similar accuracy. 
Very interesting work that demonstrates that **fundamental research can make a difference!**

### Effective reasoning
Other more formal work inspired by a real world use case was presented by
[Robin De Vogelaere](https://be.linkedin.com/in/robin-de-vogelaere-50b898100).
You probably have used _glue_ (a cohesive) at least once in you life.
Selecting the right adhesive in the right situation is not trivial.
It depends on the material and in which conditions the product will be used (heat, shock, etc).

Robin presented the _FO(.)_ first-order logic
that they use in their [IDP/Z3](https://www.idp-z3.be/) Knowledge Base system
to perform reasoning (on cohesives).
In his presentation he highlighted why the Knowledge Graph Community should care (see image below),
**A perfect example of the knowledge transfer the workshop aimed for!**

![Robin De Vogelaere presents reasons why the Knowledge Graph community should care about the FO dot logic](kg4di-2023/2023-06-09_kg4di-why-kg-should-care.jpg)


### Reliable query languages
Staying in the Linked Data RDF world:
You might have used SPARQL already to query something from Wikidata via the [Wikidata Query Service](https://query.wikidata.org/).
But using some baked-in SPARQL functionality, you can actually write a _federated SPARQL Query_
that fetches different parts of the data from different servers.

But what if one crucial FILTER part of the query relies on the data of a server
that is currently offline?
Should the whole query fail or would you accept data from the other servers
that could not have been filtered (and which are wrong for your use case)?

[Tim Baccaert](https://baccaert.com/) presented some early work on exactly those problems.
He is looking into different ways to make query languages more reliable.
For example by providing better machine-understandable error messages
such that clients can interpret partial results better.

This is _one way_ of dealing better with the reality where servers are down sometimes.
Another way is [Linked Data Fragments (LDF)](https://linkeddatafragments.org/):
Instead of processing the whole possibly complex SPARQL query on the server,
the LDF server only accepts simple patterns
and the computation of the result is done on the server _and_ the client.

## Experience and exemplars

This session is about experiences in setting up Knowledge Graphs
and in using the data.


### Data dependencies
Understanding relationships between attributes of relational data
is important to integrate data in a meaningful way.
[Marcel Parciak](https://be.linkedin.com/in/marcel-parciak-b412171ab)
presented work on detecting (approximate) _functional dependencies_ in data.

By performing a literature review before their experiments,
they could identify 12 measures to detect possible dependencies.
They performed an evaluation of the different measures
on benchmark datasets.
Before doing that they also had to annotate the benchmark data
because there were no labels for
when there is a functional dependency and when not. 


[Larissa C. Shimomura](https://scholar.google.com/citations?user=FFZa8_QAAAAJ&hl=en)
is researching another kind of dependency: Graph Generating Dependencies.
Such dependencies are helpful to understand the data and possible correlations between different attributes.
In particular, Larissa investigates reasoning on property graphs.


### Rapid Prototyping 

Declarative solutions following common standards are the goal
when working with Knowledge Graphs in RDF.
However, especially in the beginning of a project
the requirements are often vague
and different stakeholders need to build a common understanding.

In his talk, [Christophe Debruyne](https://chrdebru.github.io/)
presented work about the TOXIN Knowledge Graph.
The aim of this Knowledge Graph is to describe
existing safety data about cosmetic ingredients.
It therefore contributes to non-animal systemic toxicity assessments.

In the beginning phase of the project many things were set up
with Python.
This helped in getting a shared understanding between the stakeholders
before setting up a complete infrastructure.
In later stages, R2RML and other declarative tools
such as SHACL for quality assessments were used.


### Technology stacks Knowledge Graph
While talking about infrastructure,
the technology stacks of cloud platforms are quite complex.
This means that switching between providers can become really cumbersome.

In his presentation, [Johannes Härtel](https://researchportal.vub.be/en/persons/johannes-h%C3%A4rtel)
talked about how they used RDF to describe technology stacks.
Furthermore, they have implemented a tool that harvests data
about the software stacks from GitHub repositories.

For example, if you have a docker file,
the script detects this and will add to the Knowledge Graph
that you at least use YAML files and
that you have at least one docker setup provided.

The goal of their work is to allow for a smoother switch
between technology stacks. 
For example, to identify Open Source technologies that fit
the current (proprietary) technology stack you are using.
At the core, they used Apache Jena to store RDF.
Johannes listed four reasons for why to use Knowledge Graphs (see image below).

![Johannes Härtel presents 4 reasons why to use Knowledge Graphs](kg4di-2023/2023-06-09_kg4di-kg-reasons.jpg)

### Law as code
The transparency of legislation and the accountability of governments are very important
for a democracy.
In his presentation,
[Tom De Nies](https://tomdenies.be/)
presented the tools [Themis](https://themis.vlaanderen.be/) 
and [Kaleidos](https://kaleidos.vlaanderen.be/aanmelden)
which are used to support the legislation process in
Flanders, Belgium with Linked Data.

The clue?
There is no data conversion needed, their system works with RDF at its core!
Data is stored, accessed and published from a RDF triple store.
Input forms and other website components are created
by using an [EmberJS](https://emberjs.com/) frontend
that relies on a rich microservice infrastructure in the backend.


## Processing and mining

Last but not least,
the last session focused on mining information
and effective query execution.

### Mining software engineering patterns
[Yunior Pacheco Correa](https://cu.linkedin.com/in/yunior-pacheco-correa)
presented work on mining software engineering patterns from code repositories.
This can help to support a developer with auto-completion
when writing code, such as [GitHub Copilot](https://github.com/features/copilot).
Another possibility would be to query the mined patterns
to for example look for security vulnerabilities.

### More efficient SPARQL queries
Three presentations from the IDLab [KNoWS group](https://knows.idlab.ugent.be/)
focused on the behind-the-scenes of querying with SPARQL.
SPARQL is a declarative query language: the user specifies _what_ to retrieve and not _how_.
Internally, the used SPARQL query engine
processes the query and builds a query plan.
For example, it determines how to join result patterns.

[Bryan-Elliott Tam](https://ca.linkedin.com/in/bryanelliotttam/en)
presented work related to _guided link traversal query processing_.
So basically, how a RDF query interface can already provide hints
about its data via the [TREE hypermedia specification](https://treecg.github.io/specification/),
such that the query engine can make better choices in query planning.
Similar research was presented by Jonni Hansi.

Bryan's research has shown that with SPARQL FILTER expressions and the TREE specification,
they were able to prune links to Linked Data fragments that will certainly not contribute to the SPARQL query.
This means the query will be faster!


Ruben H. Eschauzier presented early work on
a ML model to learn effective joins in query planning.
As a modular part of the [Comunica](https://comunica.dev/) query engine,
the presented model can be used to predict the execution time of a join
and tries to select the most efficient one.
Currently this model only outperforms the Comunica templates
in 7 out of 18 templates.
There is thus still more research needed!

### More on query optimization
The research of [Wilco van Leeuwen](https://research.tue.nl/en/persons/wilco-van-leeuwen)
centers around _cardinality estimation_:
a technique used to estimate the number of items returned by a query or subquery.
He is interested in obtaining the most accurate answers using
the least amount of resources (time and space).

Compared to relational data, graph data introduce additional challenges
for cardinality estimation.
His research helps understanding different cardinality estimation techniques and their trade-offs.
This could for example be applied to improve query planning on graph data,
such as for SPARQL query planning.



## Final remarks

Thanks to the organizers for planning this event
and to the researchers to present their work!
I think this has been a fruitful exchange of knowledge. 
I am looking forward to the following events.

Don't forget to share this post on social media and in your networks!

Please also consider subscribing to my weekly newsletter _FAIR Data Digest_
to receive more interesting content every Tuesday!

<iframe src="https://fairdata.substack.com/embed" width="100%" style="border:1px solid #EEE; background:white;" frameborder="0" scrolling="no"></iframe>

