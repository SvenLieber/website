---
title: CoRDI 2025
subtitle: Why research data infrastructures matter - conference report
share: true


# Link this post with a project
projects: []

toc: true

postDOI: dummy

# Date published
date: 2025-08-31T09:00:00+01:00

# Date updated
lastmod: 2025-08-31T09:00:00+01:00

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
  - Research Data Infrastructure
  - Aachen
  - NFDI
  - Wikidata
  - Wikibase
  - RDF
  - Germany
  - EOSC

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

In the old days, research was done by famous individuals.
Nowadays, research is a team effort!
Working together requires
making agreements about how to collaborate
and using common tools. 
These kinds of agreements (or standards) and tools
are especially crucial given the amount of data nowadays.
I attended the **2nd Conference on Research Data Infrastructure**,
in Aachen, Germany from August 26 to 28, 2025,
where _research data infrastructures_ were discussed.
In this blog post I will reflect 
on the various presentations and posters I saw
as well as the discussions I had.
<!--more--> 

## Context

In August 2025,
the [_German National Research Data Infrastructure (NFDI)_](https://ror.org/05qj6w324)
organized the second edition of the
Conference on Research Data Infrastructure (CoRDI).
Around **800 people** attended this international multi-track conference.
This year's edition did not follow a standard peer-review,
but was curated based on the conference organizers
and a balance of the various disciplines and topics
in the field of research data infrastructure.

Even though my contribution was not selected,
I anyway attended as this is a great chance to network.

**My main takeaways**

* a
* b
* c 

In the rest of this post I will focus on my personal _main highlights_.

{{< toc >}}

## Keynotes

This year's conference featured two keynotes:
**Rob Finn** talked about the complex data ecosystem of life science data
and
**Cathrin Stöver** provided insights into the physical networks
that make all of our work possible in the first place.

### Rob Finn - Life Science data

On the first conference day,
[Rob Finn](https://orcid.org/0000-0001-8626-2148)
from the [European Bioinformatics Institute](https://ror.org/02catss52)
talked about the kind of data that they process and publish.
As well as where he sees potential for AI.

It's not really my domain,
but what I take home from Rob's talk
is the evolution of workflows.
Because I recognized my work for the BELTRANS project,
where we create a corpus of book metadata of contemporary
translations between Dutch and French.
It's a completely different area,
but in our case we also start with a bunch of
Python scripts, glued together with bash scripts.

According to Rob,
and hinting towards work of [Carole Goble](https://orcid.org/0000-0003-1219-2137),
those ad-hoc workflows can be made FAIR
by describing them with Ro-Create
and uploading thsoe descriptions to the WorkflowHub.

![From Python scripts to the WorkflowHub](cordi-2025/2025-08-26_cordi_keynote-workflow.jpg)

### Cathrin Stöver - Research and Education Infrastructure

In her impressive keynote on the last conference day,
[Cathrin Stöver](https://www.wikidata.org/wiki/Q136008224)
the Chief Communication Officer at [GÉANT](https://ror.org/052hmv319), 
discussed how GÉANT provides global connectivity for researchers.

She wasn't referring to a few online services or cloud solutions. 
She discussed real-world 800 GBit traffic
via GÉANT's own submarine cables, 
as well as other success stories, 
such as the well-known eduroam Wi-Fi internet access service.


![Geant - 25 years of building global R&D networks](cordi-2025/2025-08-28_cordi_geant-timeline.jpg)

GÉANT provides research and education network services
by interconnecting 38 National Research and Education Networks (NRENs)
such as [_Deutsches Forschungsnetz_ (DFN)](https://ror.org/038t94116) in Germany
or [BELNET](https://ror.org/02d3h3h49) in Belgium
and serves around 50 mio users across Europe.
In the last 15 years, 
other parts of the world have been connected as well, 
such as East Africa extensively and West Africa to a lesser extent.

Global connectivity is also related to global governance, 
which is not an easy topic in today's geopolitical reality. 
This was the main subject of the Q&A, 
with questions relating to why certain parts of the world are not connected 
(GÉANT's headquarters are in Amsterdam, 
so it falls under Dutch and European law and is forced to follow sanctions) 
and why satellite networks are not used instead of terrestrial networks 
(there is no low-orbit capacity yet owned by Europe, 
and high orbit does not provide enough bandwidth).

![EU and national investments into Research & Infrastructure](cordi-2025/2025-08-28_cordi_geant-rd-funding.jpg)

In addition to these interesting facts,
the keynote also focused on the conference organizing organization NFDI.
It must undergo evaluations and needs to become operational within a few years.
Based on GÉANT’s experiences, 
Cathrin identified three important aspects for success: 
**validation, people, and funding**.
GÉANT receives top-down and bottom-up validation from both its users 
and recognition on policy level, including an alignment with the
Sustainable Development Goals.
Evenly important is the people aspect with
a strong community and regular community conferences.
But also having a value conversation to keep people with passion.
And last but not least,
the aspect of secure and sufficient funding, 
which due to the multiplier effect pays off.

If you ask me, I think NFDI is on a good way!
There is a large user base and recognition from the policy level,
both from the German government
as well as via links to European research.
I have also met many passionate people at the conference.
And at least from an outsider perspective,
I think lots of money is invested in Germany for RDFM at the moment.

---

## Persistent identifiers, Authority data & Knowledge Graphs

These are my favorite topics to dive into:
PIDs, authority data, and Knowledge Graphs. 
I was really glad to find them featured so prominently at CoRDI,
some of them even together in a single humanities session!
It's just a pity that the PID panel discussion 
was in parallel to
the humanities section about authority data.


Even though I missed the PID panel,
I could speak with experts directly,
thanks to the poster sessions!
For example at the poster of
[Barbara Fischer](https://orcid.org/0009-0009-5034-6687)
from the [German National Library (DNB)](https://ror.org/01n7gem85)
and
[Paul Vierkant](https://orcid.org/0000-0003-4448-3844)
from [DataCite](https://ror.org/04wxnsj81) about the PID network Germany.

![The poster of the PID network Germany](cordi-2025/2025-08-27_cordi_pid-network-de.jpg)

We don't have something similar in Belgium yet,
(probably also due to the special federalism in Belgium),
but I'm glad that my colleagues from the [FedOSC project](https://www.belspo.be/belspo/coordination/resDev_openScience_en.stm) 
are also looking into the PID topic, at least for the Federal Scientific Institutions!
While talking about PIDs, we were also joined by [Daniel Mietchen](https://orcid.org/0000-0001-9488-1870),
who argued that Wikibase already comes with PIDs out of the box.

----

The humanities session featured talks
about the GND, which is the authority file of German-speaking countries,
as well as the Knowledge Graph software Wikibase.


In the presentation, _Authority Files and the Text+ Data Space_
([10.5281/zenodo.16736146](https://doi.org/10.5281/zenodo.16736146)),
[Barbara Fischer](https://orcid.org/0009-0009-5034-6687)
highlighted that

> "standards are not dropping from the sky"

According to her, 
we should not lose diversity when using standards. 
Barbara used English as an example of a language 
used for understanding each other in science. 
However, it does not replace one’s mother tongue, 
with which one can express much more diverse concepts.
Barbara further argued that we have to give people the edit button,
or at least a button to suggest changes,
this will also enhance collaboration.

Open Knowledge Graphs are one way to enable (large-scale) collaboration.
While most people are familiar with Wikidata,
there are also lesser-known, more domain-specific Knowledge Bases.
One such example is the FactGrid Wikibase instance,
used by many historians.
Because the historians share a single Wikibase instance,
they are also forced to work together.

[FactGrid's](https://www.wikidata.org/wiki/Q90405608) creator,
[Olaf Simons](https://orcid.org/0000-0001-9230-4666)
gave the presentation _Wikibase - the best software to communicate with the upcoming knowledge graphs?_ 
([10.5281/zenodo.16892677](https://doi.org/10.5281/zenodo.16892677)).
In it, he states a very concrete issue:
the 100 million item limit of Wikidata's (and Wikibase's) Blazegraph triple store!
Apparently the Wikidata graph was split as a workaround.
Yet, Olaf argues that these kind of workarounds do not solve the underlying issues.
He calls for the simple but effective solution:

> "The NFDI should develop a joint interest with Wikimedia Germany to break the present 100 million item limit"

![Olaf Simons presents the 100 million item limit of Wikibase](cordi-2025/2025-08-26_cordi_100-mio-triples-challenge.jpg)

I can very much relate to Olaf's statement.
As a computer scientist I am used to developing custom software solutions
when I cannot find standard software that addresses the problem.
I often see software developers in different (engineering) fields
develop software even when standard sotware is already available.
One example is software to generate RDF from other data sources.
Standard software is important!
In the humanities, for example,
where tools with a user interface
and a high [Technology Readiness Level (TRL)](https://www.wikidata.org/wiki/Q1478071) are needed,
Wikibase plays an important role.
This fundamental software should be maintained
and further developed to overcome its current limitations.


In the same session,
[Florian Thiery](https://orcid.org/0000-0002-3246-3531)
and
[Lozana Rossenova](https://orcid.org/0000-0002-5190-1867)
presented
challenges of federated queries using the Wikiverse and OpenStreetMap 
within the NFDI Knowledge Graph Ecosystem 
([10.5281/zenodo.16736048](https://doi.org/10.5281/zenodo.16736048)).
While doing federated SPARQL qeries across Wikibase instances,
including FactGrid,
they noticed technical and conceptual hurdles,
such as namespace collisions, property mappings or
allow lists.
The latter specifying which instances can be called for federated queries.

TODO: our challenge, but not in detail

---

More talks and posters about Knowledge Graphs and ontologies sparked my interest at CoRDI.

In the presentation of
[Leyla Jael Castro](https://orcid.org/0000-0003-3986-0510)
about 
Bioschemas and Schemas.science at NFDI ([10.5281/zenodo.16735850](https://doi.org/10.5281/zenodo.16735850)),
I have learned about Bioschemas and Schemas.science.
The first is a is a community-driven initiative to build upon Schema.org for the life science domain.
The latter is a sister website in which they broaden the Bioschemas efforts to a more general research-related extension for Schema.org.
In both cases to enhance findability, as Schema.org is mainly used by search engines.

Crosswalk don't necessary have to be mappings like in ontology mapping (crosswalk thus for things where you see in a platform that there is a title, keywords etc)
Cultural heritage data is like a bag of Lego blocks, but without step by step instructions and all needed blocks
Datasheets for DH
Put access info on top (against frustration)
Sample distribution for HealthDCAT.. But how with privacy? How to define quality?
Comments from more than 100 organizations for HealthDCAT


At the poster of the NFDIcore 3.0 ontology, 
I also had a small chat with
[Jörg Waitelonis](https://orcid.org/0000-0001-7192-7143)
about the BFO basis of the ontology ([10.5281/zenodo.16736251](https://doi.org/10.5281/zenodo.16736251)).
We talked about the possibilities of the ontology to also model temporal aspects, such as names that change over time.
Which comes with a lot of extra triples (in case this is done for many entities).

![The poster of the NFDIcore 3.0 ontology based on BFO](cordi-2025/2025-08-26_cordi_poster-nfdi-core-ontology.jpg)


TODO
* talk on dcat, datacite and schema.org
* data integration bioschema


On the last day of the main CoRDI conference,
[Lozana Rossenova](https://orcid.org/0000-0002-5190-1867)
presented the results of a survey about
how NFDI consortia are using Knowledge Graphs ([10.5281/zenodo.16736078](https://doi.org/10.5281/zenodo.16736078)).
The survey was conducted between March and May 2025
and covered 27 Knowledge Graphs from 11 consortia.
![Common challenges about using Knowledge Graphs in NFDI consortia](cordi-2025/2025-08-28_cordi_kg-survey-challenges.jpg)

Their results lists challenges in different areas that are very recognizable.
TODO link to my work


[Volker Hofmann](https://orcid.org/0000-0002-5149-603X)
presented the Helmholtz Knowledge Graph ([10.5281/zenodo.16736336](https://doi.org/10.5281/zenodo.16736336)).
I liked the used images of the presentation, such as the following about 
separated islands of data. Apparently only a small percentage of all the entities.

![The Helmholtz Knowledge Graph with many separated islands of data](cordi-2025/2025-08-28_cordi_helmholtz-graph.jpg)

This made me think about the many authority records in MetaBelgica
for which we only have a name and no linked birth/death dates or birth/death places.
In our source data we have linked publications though, 
instead of leaving them out, we maybe should add some linked PIDs, ISBNs or publication places to MetaBelgica
to not create authority islands...

In
[Sarah Rebecca Ondraszek's](https://orcid.org/0009-0003-7945-6704)
presentation on the NFDI4Memory Knowledge Graph ([10.5281/zenodo.16736125](https://doi.org/10.5281/zenodo.16736125)),
I found two things interesting.
First, they do not yet have a link with PROV-O, because of the more difficult alignment with BFO (yet there could be mappings).
Second, they mentioned Sampo, a Linked Data publishing tool from Finland,
that I have recently seen at various conferences.
We are testing it for the BELTRANS project as well,
and I know that the Sampo team is collaborating 
with the CLARIAH-VL+ project in Flanders/Belgium to improve the software ([Sampo fork](https://github.com/GhentCDH/sampo-ui) that will be rebased to the original Sampo).

![Related work to the memO ontology: ArCo, Europeana and Sampo](cordi-2025/2025-08-28_cordi_memo.jpg)

During the Q&A of
[Julia Thoennissen's](https://orcid.org/0000-0002-5467-871X)
presentation
about FAIR and scalable access to large image data in the range of petabytes (among others in neuro science) ([10.5281/zenodo.16736220](https://doi.org/10.5281/zenodo.16736220))
I wondered if their workflow, which contains 3D images, could be extended with the [International Image Interoperability Framework (IIIF)](https://www.wikidata.org/wiki/Q22682088) for data publishing.
This would provide a standard software solution instead of a custom one.
The authors were not familiar with IIIF, it's probably less well-known outside of the cultural heritage domain.
Afterwards I had a look myself, there is a 3D community working group at IIIF.
However, based on the community group's current description it does not seem that this feature already exists.



---

## AI, software & workflows

It's 2025, of course there has to be AI!
[Sandra Geisler](https://orcid.org/0000-0002-8970-6282)
introduced the AI session, 
by mentioning current barriers for FAIR Research Data Management,
and for which barriers AI can help.

![Barriers for FAIR Research Data Management from which two relate to AI](cordi-2025/2025-08-27_cordi_ai-session.jpg)


Other AI-related talks and posters at the conference
focussed on different aspects to annotate machine learning models.
To this regard I have learned about things like

* FAIR4ML, a vocabulary to describe Machine/Deep Learning models, presented by [Leyla Jael Castro](https://orcid.org/0000-0003-3986-0510) 
* Skyscanner or GoogleFlights but for ML models (Nuxt3js)
* CroissantML.. Ai ready datasets
* The FAIR Digital Object registry MLentory

* medical image segmentation: define context and what should be detected for example



Workflows
* Image workflowhub
* setup of AI session tool with virtuoso and postgresql, fastapi
* gsap workbench

Research software

[Stephan Ferenz](https://orcid.org/0000-0001-9523-7227)
Towards Common Metadata For Research Software in the NFDI [10.5281/zenodo.16735848](https://doi.org/10.5281/zenodo.16735848)
* image of comparison slide 


--- 
## Training & Communities

Research infrastructure is all about communities as well!
As an outsider I must say that I am impressed about all the different initiatives
represented at CoRDI.
Through discussions at the conference I have learned that there are also other
non-NFDI initiatives in Germany, some of them older than NFDI.
For example the different federal state RDM initiatives
like bwFDM (shout out to _The Länd_) which also had posters this time.
They jointly presented themselves on the last CoRDI in 2023 ([10.52825/cordi.v1i.242](https://doi.org/10.52825/cordi.v1i.242),
see also my previous conference report [10.59350/pg3xj-4z449](https://doi.org/10.59350/pg3xj-4z449)).

Other initiatives are the _Fachinformationsdienste (FIDs)_,
that in its current form receive funding since 2014.
I personally know the thematic [FIDBenelux](https://www.wikidata.org/wiki/Q63858763) as it relates to Belgium and 
because they are also in the follow-up committee of the MetaBelgica project.
At CoRDI, 
[Reinhard Altenhöner](https://orcid.org/0000-0001-8274-780X)
and
Jana Fabrizius
presented about the Role of FIDs Between Disciplinary Research and National Infrastructure ([10.5281/zenodo.16736302](https://doi.org/10.5281/zenodo.16736302)).
I have learned that since 2018 FIDs are self organized and currently have long-term funding via FIDPlus.

![Collaboration between FIDs and the NFDI](cordi-2025/2025-08-26_cordi_FID.jpg)

Regarding RDM training, 
two posters stood out to me as memorable and insightful. 
One covered the general aspects of collaboration, and the other covered the CARE principles.

The poster _Lost in Collaboration_ really hit the nail with the identified difficulty for effective collaboration:

> "Turning Collaboration into Concrete Outcomes."

![Lost in collaboration poster about soft infrastructures and facilitators](cordi-2025/2025-08-26_cordi_poster-collaboration.jpg)

At the second poster I joined an interesting discussion about the CARE principles.
[Josef Jeschke](https://orcid.org/0000-0002-8774-0321)
explained that apparently there is no clear definition in CARE about _indigenous_,
for example, it does not have to be a minority.
In general I find the ethics aspect of CARE interesting,
so I am wondering if it could be applied even in non-indigenous use cases.
More info on their poster _The Informed CARE Data Steward. Ways to CAREification_: [https://doi.org/10.5281/zenodo.16736131](https://doi.org/10.5281/zenodo.16736131).


---

## Infrastructure and Governance

One part that is utterly important,
and leans towards the impressing keynote,
is _actual_ physical infrastructure.
With all the existing clouds, data spaces and services,
I'm often wondering where the stuff is actually hosted.
Who pays for it and for how long will the services stay online?

At the very basis we have the NRENs from GÉANT, thus for example BELNET in Belgium.
And via procurement one can get access to virtual machines for example via the OCRE programme
at data centers of partners.

![The base4nfdi poster featuring among others jupyter4nfdi](cordi-2025/2025-08-27_cordi_poster-base4nfdi.jpg)

In the context of the NFDI, base4nfdi provides higher level services such as jupyter4nfdi.
At the poster of base4nfdi, [Martin Reinhardt](https://orcid.org/0000-0002-1213-5135)
explained to me how the jupyter4nfdi works.
It is essentially a JupyterHub hosted at _Forschungszentrum Jülich_ and another data center.
Research institutions can host their own Jupyter services,
creating a decentralized network
that researchers can access via the central JupyterHub and Single-Sign-On.
This way, research institutions can configure their settings
so that only their own researchers 
can use the Jupyter resources 
from the institution's servers, for example.
However in theory, researchers from other institutions could also use the provided resources.
According to Martin, this is also welcome, 
because cloud hosts want at least a certain percentage of server load;
otherwise the infrastructure just sits there and costs money.

Eventually,
research institutions still provide the actual infrastructure,
or at least pay for virtual machines in the cloud.
This brings us back to the initial question:
Who pays for it, and for how long will the services stay online?
This obviously depends on the research institutions,
but I think it will likely be poject-based funding after all.

![Sustainable research data infrastructure is project funding after all? - imgflip](cordi-2025/research-data-infrastructure-meme.jpg)

While not ideal,
there are real-life examples of successful infrastructures
that prove such funding can work.
For example, historians can use [FactGrid](https://database.factgrid.de/wiki/Main_Page) 
to store their data even after their funding period ends.
In Flanders,
I came across the [ODIS platform](https://www.odis.be/hercules/_en_overODIS.php),
which also offers a home for research data within its scope.
For the latter I also have heard that researchers
already started to mention this platform (or repository)
in their mandatory data management plans.

todo:
* investments
* hpc talk, jullich, filetransfer & metadata
* mlz, scicat


---

The above mentioned infrastructure example also relates to governane.
When more than one institution or individual work together,
agreements are needed!

Data spaces and governance
* 

Governance
* resiliance discussion
* Mustervertrag... Alle zu streng wenn man aufbaut
[Martha Stellmacher](https://orcid.org/0000-0001-5655-0130)

[Robert Herrenbrück](https://orcid.org/0000-0002-1355-5043)
Establishing a Central Helpdesk for KonsortSWD - NFDI4Society: Goals, Challenges, and Solutions [https://doi.org/10.5281/zenodo.16735332](https://doi.org/10.5281/zenodo.16735332)


---

## Reflections & Takeaways

---

## Closing

Internet access, identity management ...


# TUESDAY


### Workflows

Final words
* fishbowl discussion, success

Dutch Thematic Digital Competence Centre

digital preservation poster

research software in the NFDI

Critics
* data portals everywhere
* Mietchen: Things bigger than a poster


# WEDNESDAY

Creating a podcast out of a research paper

Calculate embeddings from natural language context and input .. Konda
Gsap workbench
Ontologie etc is the ground truth to make Ai creative
Data preservation... How to replicate data. Data pass alliance

Pangea saving data, among others because long term funding
Régulation as Competitive advantage
Global data governance needed
Geo political boundaries.. Citizens of science not citizens of US

anel summary: think European and global, data international space station, long term funding, importance of data (it's the basis of all kinds of decision).. The construct (structure) for collaboration

Ai to ask question ABOUT image detection



