---
title: What is Provenance?
share: false


# Link this post with a project
projects: []

postDOI: https://doi.org/10.59350/7tkkb-n0636

# Date published
date: 2017-04-07

# Date updated
lastmod: 2017-04-07

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 1
  preview_only: false

authors:
  - admin

tags:
  - provenance

categories:
  - explained

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

Having Provenance or not having it, that could be worth than several hundred million dollar. Where does something come from, how was it changed since it exists, that is provenance. These informations help human beings to asses things. Which questions need to be answered and what is my role as computer scientists in this research field?!
<!--more-->

{{% callout note %}}
If you want to get notified about more content or want to receive bi-weekly updates on FAIR and Linked Data,
please consider subscribing to my bi-weekly Newsletter.
{{% /callout %}}
<iframe src="https://fairdata.substack.com/embed" width="100%" style="border:1px solid #EEE; background:white;" frameborder="0" scrolling="no"></iframe>

In 2015 the painting Les Femmes d’Alger from Picasso was sold for
unbelievable [179 Mio Dollars](http://www.independent.co.uk/arts-entertainment/art/news/pablo-picasso-les-femmes-dalger-version-o-sells-for-179m-and-sets-new-world-record-10243056.html).
The painting La Bella Principessa from Leonardo da Vinci was sold for surprisingly cheap 20,000 Dollars (see [Ludäscher](https://link.springer.com/chapter/10.1007%2F978-3-319-40226-0_7)).
But what is the main difference, why did the first painting obtained such a high price compared to the second?
The answer is, that there is a peace of paper which documented every owner and former places of custody of the first painting.
The same information for the second painting was [incomplete](https://en.wikipedia.org/wiki/La_Bella_Principessa#Provenance). This documented history of ownership is called Provenance.

## Why is this Provenance so important to us?

Well, let’s say I sell a car and you want to buy it. If I can provide you a service record which documents how often the car was checked in a garage the last years you have more trust in its functionality. In the same manner is it also from interest how the car was changed, which parts are newer because they were replaced for example.
Of course there is no direct trust involved, but the provenance helps to form an opinion and allows one to draw conclusions about the object. Other properties than quality can be important as well, the value of the car might also be higher if the former owner was a celebrity.

The car example shows the importance of provenance and the millions of dollars price difference of the paintings that it is definitely worth to capture! 
There are plenty of use cases where provenance is helpful, just think about the food you are eating, where does it come from? How was it produced? Was the cooling chain never interrupted? 
All these information influence your buying decision. Providing these information is therefore also in the interest of the producer. 
There is actually a start-up company called [Provenance](https://www.provenance.org), which tries to make the supply chain of products transparent.
Information if the food comes from regional producers or information if the employees were treated fair justify a higher price. 
Whereas this kind of provenance help to address a more selective client base other provenance like the consistent cooling chain is enforced by law and you have to proof it in case of an audit.

## Provenance and Computer Science

I am a computer scientist and not a quality assurance officer, where is the link to Provenance?
We are living in the 21 century, no one is using pen and paper to record the Provenance. Machines of the supply chain, Smart Sensors of the Internet of Things (IoT) are measuring and transmitting the provenance information. The provenance needs then to be stored in a queryable way . Why? Continue reading …
Imagine you are a pharmaceutical company, you keep track of the bottling of the medicine and to which drugstore each bottle was sold. Let’s say you have all the provenance just split into hundred of thousands of files somewhere on an external hard drive in an custom data format, nobody knows about.
After encountering a possible contamination of some of the produced drugs, you need to know where they end up so you can take selective only the affected bottles from the market. You don’t want to waste time and money to instruct one employee to carefully search for the information within the files, which can take multiple days. Having the Provenance stored in an machine understandable format which is queryable, will give you the answer within seconds!
Using an appropriate data storage instead of an external hard drive ensures availability and prevents data loss. Having the provenance in an standardized data format allows the usage of standard software instead of investing time and money to reinvent the wheel.
o
![woman code](what-is-provenance/2017-04-07-what-is-provenance_woman-code_no-attribution.jpg)

Overall, standards are important! Imagine your smartphone runs out of battery, you are at a friends place, but your charger doesn’t fit into the electrical socket because every house has another socket type. 
Thankfully there is a standard and every electrical socket within a country or larger region is built upon a standard. The same applies for digital standards, you can probably open PDF documents on every of your devices. 
For Provenance the World Wide Web Consortium (W3C) released a standard called PROV.

## Provenance and Social Media

Speaking of the world wide web, everybody of us produces and/or consumes so much information. Just think about all the blogs and news sites producing content every minute. 
Journalists normally investigate carefully and check the reliability of all their sources. But classical media are nowadays only one possible source from which we get information from. 
Social media like Twitter or Facebook allows everybody to create content and offer it to a broad variety of people. How do you trust if it is real what is written there? 
Political oriented groups can spread so called fake news to influence the opinion of a lot of people. Who actually takes the time to really read an article and check its sources?! 
A dramatic headline together with some emotional pictures will get much more response than an article based on facts from boring statistics. 
Additionally, such articles also generate a lot of ‘clicks’, meaning that people click on them, visit the site and are seeing some special ads  and the site operator gets a lot of money. 
Reason enough for some people to just make up stories, only interested in the money they will get.

![fake-news](what-is-provenance/2017-04-07-what-is-provenance_fake-news_no-attribution.png)

This whole process of information spreading only partially produces provenance, but the provenance is somehow there. It is implicitly hidden in the timing, the textual similarity or the social connections between the participants of the spreading. 
The provenance can partially be reconstructed. That brings us directly to the last part, the research about provenance. As a computer scientists I do actual science. 
Research about what kind of provenance can be reconstructed from social media and to which extend is this useful? This is only one example, focusing on social media. 
Also general aspects about provenance are not fully explored right now. How to handle provenance, how to secure the provenance records itself against forgery. 
Provenance sometimes means total transparency, to which extend is this desirable, at which point the privacy of individuals gets affected? 
How can new technologies help to answer some of those questions?

You hopefully have now an idea what provenance is. What do you think, where else could provenance be useful? Leave a comment!

