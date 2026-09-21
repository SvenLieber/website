---
title: SEMANTiCS 2026
subtitle: a conference report
share: true


# Link this post with a project
projects: [metabelgica]

toc: true

postDOI: 10.59350/nj6za-wjb05

# Date published
date: 2026-09-18T09:00:00+01:00

# Date updated
lastmod: 2026-09-18T09:00:00+01:00

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

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
  - conference
  - ontology
  - Ghent
  - Wikidata
  - Wikibase
  - RDF
  - LLM
  - AI
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

{{% callout note %}} Momentan leider nur auf Englisch verfuegbar da ich noch keine Zeit hatte den Blogpost zu uebersetzen. {{% /callout %}}

In a world with generative AI,
semantically annotated data of high quality
is also of high value!
The SEMANTiCS conference usually brings together
not only Semantic Web scholars,
but also players from the industry.
More than 400 people attended the 
**22nd edition of SEMANTiCS**
in Ghent, Belgium from September 15 to 17, 2026.
Apparently a record number of participants!
In this blog post I will reflect
on some of the keynotes and talks that I have attended.
As always with references, links,
and archived at the [Rogue Scholar](https://rogue-scholar.org/).

<!--more--> 

## Context

In September 2026,
the 22nd edition of SEMANTiCS was hosted at the beautiful [Bijloke Site](https://id.erfgoed.net/erfgoedobjecten/20338) in Ghent, Belgium.
I have attended the two main conference days and enjoyed talking to many peers.
Below you will see some slides showing some statistics about the conference.
Almost half of the participants came not from academia, after all SEMANTiCS is known to be the "more applied" Semantic Web conference.

**My main takeaway after attending different presentations is 
that generative AI also has changed the Semantic Web research field. 
But instead of replacing the semantics or us researchers, 
our role became much more important and mainstream.
Additionally AI opens new ways to support Knowledge Engineering and to make our work easier.**
Check also my Reflections and takeaways at the end of the post.

By the way, in a piece about AI, the Flemish TV broadcaster VRT also reported about the conference 
and interviewed a few companies that were present with a booth: 
[video](https://www.vrt.be/vrtmax/a-z/vrt-nws-journaal/2026/vrt-nws-journaal-vrt-nws-journaal-19u-20260916/?starttime=1825) (in Dutch).

![The registration statistics of SEMANTiCS 2026](semantics-2026/PXL_20260916_073458618.jpg)
As Angelo Salatino, one of the general chairs explained,
the host country was responsible for most of the participants,
followed by the usual suspects,
but there is also a growing number of a more international audience.

![The number of submissions (242) and how many got accepted](semantics-2026/PXL_20260916_074101857.jpg)
The acceptance rates for the different tracks are 
26% for the research track, 
25% for BlueSky, 
48% for industry, 
77% for posters and demos, 
and 96% for practitioners.
In my impression this is comparable to other Semantic Web conferences.
Apparently there was an incredible number of 700 reviews,
a big thank you to all the reviewers and track chairs!


The conference offered three parallel tracks,
and I also used the conference time to network
and catch up with former colleagues,
hence I could not visit all talks.
So the following post subjectively focuses on a few selected talks
which for this post I group into a few broader topics.

{{< toc >}}

## Wikibase and library-related talks

One **Wikibase**-related talk directly caught my attention in the programme,
because we currently are also setting up a Wikibase-based solution in the [MetaBelgica project](https://metabelgica.be).

[Eléna Liu](https://orcid.org/0009-0007-5175-4901)
from the [University of Liège](https://ror.org/00afp2z80)
presented the Wikibase Mapping Language (WBML) ([DOI 10.3233/SSW260007 ](https://doi.org/10.3233/SSW260007 )).
Among others, objectives include providing a more standard way
to integrate heterogeneous data sources directly into Wikibase instances.

Currently their mapping language is directly extending [RML](https://rml.io/),
I hope someone will make work of also extending the YARRRML notation ([DOI 10.1007/978-3-319-98192-5_40](https://doi.org/10.1007/978-3-319-98192-5_40))
with WBML; I mainly use mapping rules in YARRRML syntax.
Someone in the audience asked how WBML compares to the state of the art,
luckily Elèna had an interesting backup slide (see below) :-)
I'm curious to get my hands on it when I have time and a matching use case.

![State of the art comparison of the Wikibase Mapping Language (WBML)](semantics-2026/PXL_20260916_095156793.jpg)

---

Another interesting presentation focused on born-digital archives.
The work of [Lucia Giagnolini](https://orcid.org/0000-0002-4876-2691)
from the [University of Bologna](https://ror.org/01111rn36)
focused on **turning information from file systems into Knowledge Graphs** ([DOI 10.3233/SSW260020](https://doi.org/10.3233/SSW260020)).

I must admit,
when hearing to turn private archives into Knowledge Graphs,
I think of 19th Century scholars with beautiful home libraries,
not about a folder called _Downloads_ with hundreds of pdf files or power point presentations.

Lucia and colleagues have focused on digital sources
from the Italian writer _Valerio Evangelisti_,
concretely they have tested their pipeline on three directories (main computer hard disk, external hard disk, and floppy disk contents)
which already produced **61 million RDF triples** for the representation of 
78,211 files, 11,135 folders and 5.5 million metadata fields.

The paper was nominated for a best paper award and won it, congratulations 🎉.


![Statistics about the born-digital archive of the writer and historian Valerio Evangelisti](semantics-2026/PXL_20260917_091515879.jpg)

---

Once I wrote a [blog post](https://doi.org/10.59350/4hd4r-1tk44) about clustering of book editions into more general _works_.
Such an approach is also part of the work presented by
[Jeroen Wouters](https://www.linkedin.com/in/jeroen-wouters-6b02161a/) from the company [Inuits](https://inuits.eu/).
They have built a catalogue software for Cultuurconnect, 
an organization that runs the central catalogue used by 300 Flemish public libraries.
The _Work, Expression, Manifestation, Item (WEMI)_ model is central to their data management,
even though they still offer data in the common MARC21 format for downstream tasks,
their system does not work in MARC.

![Some basic information about the GraphQL interface of the elody platform for the Flemish public libraries](semantics-2026/PXL_20260917_094251557.jpg)



## Our contributions: BELTRANS and MetaBelgica

At this year's SEMANTiCS conference I presented both a demo and a poster.

The demo was about the user interface to explore
50 years of book translation flows between Dutch and French in Belgium,
aka the BELTRANS corpus that we will publish soon.
We already had a semantically annotated corpus,
thus we could use the off-the-shelf software SAMPO-UI ([DOI 10.3233/SW-210428](https://doi.org/10.3233/SW-210428))
to configure a user interface
with JSON configuration files and SPARQL queries.

Recently the Ghent-Centre for Digital Humanities upgraded SAMPO-UI,
which became the new v4 of SAMPO.
They and one of the SAMPO-UI developers from Finland were also at SEMANTiCS,
they had a demo right next to me.

---

The poster was about a current challenge in the MetaBelgica project
for which I wanted some feedback from the community.
Our Wikibase is internal, but we will have a public interface.
In order to comply with legislation such as the GDPR,
we eventually have to implement rules that govern which person records
or which properties of which person records are shown publicly and which not.
The main idea is that **we use some additional Wikibase properties and qualifiers
to annotate what is supposed to be public or private.**
For example, in case we receive a GDPR opt-out request we can
update the annotations.
The filter API that we put on top of the internal Wikibase
can then use those annotations to render the data GDPR-compliant.

Concretely, the poster ([DOI 10.5281/zenodo.21915884](https://doi.org/10.5281/zenodo.21915884)) shows three different ways to use properties and qualifiers.
Thanks to some feedback I know already
that I have to adapt the mapping to the Data Privacy Vocabulary (DPV) ([DOI 10.1007/978-3-031-77847-6_19](https://doi.org/10.1007/978-3-031-77847-6_19)), because I made a mistake.

![Our BELTRANS demo and MetaBelgica poster](semantics-2026/PXL_20260916_131549098.MP.jpg)

---

## Interesting use cases

[Hans Schevers](https://orcid.org/0009-0000-1017-8097)
from the company [Wistor](https://wistor.nl/)
presented their project for an interesting asset management tender
from the municipality of Utrecht in the Netherlands.

_What made the tender so interesting?_
Instead of asking for a single asset management system,
the tender **was split into an object registry
and a separate management app.**

I find this also particularly interesting,
because I find myself thinking about the same issue in the Cultural Heritage sector:
Software vendors provide Content Management Systems (CMSs)
in which all data management _and_ storage is handled.
Especially in an inter-institutional scenario like for Federal Scientific Institutes in Belgium
it is difficult to think
of solutions that span across institutions,
without thinking of merging everything into a single centralized system.
Whereas when splitting things up,
much more becomes possible!
Like tendering a centralized storage solution with basic metadata fields for interoperability
and separate domain specific management systems for detailed metadata.


![A 2022 tender from the city Utrecht split an asset management application in two: object registry and management app](semantics-2026/PXL_20260916_102459892.MP.jpg)

---


Apparently there is a lack of community for the Data Quality Vocabulary (DQV).
[Harshvardhan J. Pandit](https://orcid.org/0000-0002-5068-3714)
from the [Trinity College Dublin](https://ror.org/02tyrky19)
presented some recent extensions of DQV that make the vocabulary more future-proof ([DOI 10.3233/SSW260022](https://doi.org/10.3233/SSW260022)).
For example, the target for quality specifications are now generalized from `dcat:Dataset` to `dcat:Resource` such that also the quality of AI models can be described, not just datasets.

![Published extensions of the DQV vocabulary so it is AI-ready](semantics-2026/PXL_20260917_113037886.jpg)

Last but not least,
there was a presentation about a very interesting and practical use case:
A Knowledge Graph about the product composition of vaccines.

[Filip Pattyn](https://orcid.org/0000-0003-0858-6651)
from the company [FAQIR](https://faqir.eu/)
started off his presentation with the challenge of finding "well known" medication
while you're abroad.
Apparently most medications like painkillers are sold under different brand names
in different countries.
Also the composition of the medication can be slightly different.
A Knowledge Graph encoding underlying concepts like composition can help!
This paper was also nominated for a best paper award and won it, congratulations 🎉.

![A Knowledge Graph excerpt about the product composition of vaccines](semantics-2026/PXL_20260917_122933281.jpg)


---


## Key insights for Knowledge Engineering

The very first keynote speaker and the last invited speaker both talked about Knowledge Engineering!
There was a lot to learn and both talks have shown me that AI really has set in.


[Juan Sequeda](https://orcid.org/0000-0003-3112-9299)
from the company [data.world (from ServiceNow)](https://data.world/)
kicked off the conference after the welcome presentations.
His _20 Lessons from 20 Years of Building Ontologies and Knowledge Graphs_
included some real food for thought.
Throughout the conference I heard people referring to some of the things said in this talk
such as the need to _figure out incentive mechanisms_ when implementing change.

Juan also emphasized the importance of socio-technical challenges,
with this regard he suggests to rename _soft-skills_ to _strong-skills_.
The slide below shows his thoughts on research agenda.


![Juan Sequeda's thoughts on research agenda](semantics-2026/PXL_20260916_083815552.MP.jpg)

---

In the last presentation of the conference,
[Daniel Garijo](https://orcid.org/0000-0003-0454-7145)
from the [Universidad Politécnica de Madrid](https://ror.org/03n6nwv02),
focused on Ontology Engineering.

During my PhD (2016-2022) I also looked into Ontology Engineering,
unfortunately I never managed to get a paper accepted about it,
nor got to include it into my PhD in the way I would have liked to. 
For example the [Ontoboldt](https://w3id.org/ontoboldt) Knowledge Graph 
for which I spend a lot of time compiling and aligning all information about existing Ontology Engineering methodologies.
Before the raise of generative AI this took a lot of manual efforts :-)

Apparently a lot has happened since the rise of Generative AI ...
Daniel has cited many recent research papers exploring the intersection
of Ontology Engineering and AI, in particular Large Language Models (LLMs).

A question he raised, _is an ontology really an otology if it has been automatically generated?_
In that case, Juan Sequeda from the audience suggested to adapt the following 1992 definition of Gruber 

> "An ontology is a formal specification of a shared conceptualization" - Gruber 1992

to something like

> "An ontology is a formal specification of a **generated assumed** conceptualization" - Sequeda 2026

![Conclusions of Daniel Garijo regarding Ontology Engineering in an generative AI-era](semantics-2026/PXL_20260917_134202644.jpg)




## Reflections and Takeaways

SEMANTiCS 2026 was my first Semantic Web conference in many years
and I must say that I have enjoyed it!

We are living in a time where semantically annotated Knowledge Graphs
not only support generative AI or describe its input training data,
but where the underlying ontologies and human consensus itself 
is partially generated or at least influenced by AI.
Where will this lead to? I don't know,
but let's stay open and keep annotating everything with provenance
such that it at least becomes transparent which input was used,
human-generated or not.

Let's focus on the socio-technical problems like Juan suggested,
let's focus on methodologies.

And while doing this,
please keep the following great statement from [Ingrid Thurlings](https://www.linkedin.com/in/ingridthurlings/?locale=en) in mind,
when being asked how to ideally "extract" knowledge from domain experts:

> Keep asking "the stupid" questions and "what do you mean?"
> to get the domain experts to talk (even to each other)


(No AI was used to write this blog post)



## References

- Dimou, A., Vander Sande, M., Colpaert, P., Verborgh, R., Mannens, E., & Van de Walle, R. (2014). RML: A generic language for integrated RDF mappings of heterogeneous data. Ldow, 1184, 2014. http://ceur-ws.org/Vol-1184/ldow2014_paper_01.pdf
- Golpayegani, D., Yaman, B., Linde, F., Albertoni, R., & Pandit, H. J. (2026). DQV4AI: Representing AI Quality Dimensions for ISO and EU AI Act Using the Data Quality Vocabulary. In Bridging the Gap Between Curated and Induced Semantics: Proceedings of the 22nd International Conference on Semantic Systems, 15-17 September 2026, Ghent, Belgium (pp. 263-279). https://doi.org/10.3233/SSW260022
- Heyvaert, P., De Meester, B., Dimou, A., & Verborgh, R. (2018, June). Declarative rules for linked data generation at your fingertips!. In European Semantic Web Conference (pp. 213-217). Cham: Springer International Publishing. https://doi.org/10.1007/978-3-319-98192-5_40
- Ikkala, E., Hyvönen, E., Rantala, H., & Koho, M. (2021). Sampo-UI: A full stack JavaScript framework for developing semantic portal user interfaces. Semantic Web, 13(1), 69-84. https://doi.org/10.3233/SW-210428
J. Pandit, H., Esteves, B., P. Krog, G., Ryan, P., Golpayegani, D., & Flake, J. (2024, November). Data privacy vocabulary (DPV)–version 2.0. In International Semantic Web Conference (pp. 171-193). Cham: Springer Nature Switzerland. https://doi.org/10.1007/978-3-031-77847-6_19
- Giagnolini, L., & Bonora, P. (2026). From File Systems to Knowledge Graphs: A Multi-Phase Workflow for the Description of Born-Digital Literary Archives. In Bridging the Gap Between Curated and Induced Semantics: Proceedings of the 22nd International Conference on Semantic Systems, 15-17 September 2026, Ghent, Belgium (pp. 229-245). https://doi.org/10.3233/SSW260020
- Golpayegani, D., Yaman, B., Linde, F., Albertoni, R., & Pandit, H. J. (2026). DQV4AI: Representing AI Quality Dimensions for ISO and EU AI Act Using the Data Quality Vocabulary. In Bridging the Gap Between Curated and Induced Semantics: Proceedings of the 22nd International Conference on Semantic Systems, 15-17 September 2026, Ghent, Belgium (pp. 263-279). https://doi.org/10.3233/SSW260022
- Lieber, S. (2026). Enforcing fine-grained data governance for Wikibase via generic and declarative filter rules [Graphic]. Zenodo. Posters, Demos, Blue Sky, and Tutorials at SEMANTiCS 2026, Ghent, Belgium. https://doi.org/10.5281/zenodo.21915884
- Lieber, S., Van Camp, A., Six, J., & Birkholz, J. (2026). Explore Intra-Belgian book translations between French and Dutch in the period 1970 - 2020 with a SAMPO-UI interface [Graphic]. Zenodo. https://doi.org/10.5281/zenodo.22275750
- Liu, E., Duchateau, J., & Debruyne, C. (2026). Declaratively Populating Wikibases with WBML. In Bridging the Gap Between Curated and Induced Semantics: Proceedings of the 22nd International Conference on Semantic Systems, 15-17 September 2026, Ghent, Belgium (pp. 53-69). https://doi.org/10.3233/SSW260007 
