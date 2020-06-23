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
image = ""
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
which also comply with requirements towards data quality.
In particular I investigate on the one hand methods of knowledge engineering
and on the other hand the user-friendly visualization of data constraints.

# The big picture

There is great potential in combining data from diverse fields or just in general.

**But to combine data from different fields in a meaningful way
a common understanding in the form of a shared vocabulary (data model) is needed:
A temperature measurement in celsius should not be added to a
measurement performed in kelvin or even with my age!**
<details>
<summary>Combine data in a meaningful way? (click me)</summary>
Therefore I am using a graph-based language recommended by the world wide web consortium (W3C).
Every *thing* and every possible *relationship* between *things* will get an own web address!
Hence *everything* is uniquely identifiable and because everything follows the same graph structure,
a *heating system* can relate via a *serial-number*-relationship to a *number*
but also via a *belongs-to*-relationship to *me*.
It can also be specified that a concrete *measurement* is of type *celsius*.
I in turn can be in multiple relationships to personal information such as my *bloodtype*
or my *date of birth*.
The big plus: computer programs can look up these "websites"
and read and interpret the definition of *things* and *relationships*.
Additionally such a graph can be searched for information in a uniform way
no matter if it is information regarding my heating or regarding me.
</details>


A shared vocabulary should still be detailed enough to answer
questions we potentially have; it has to fulfill a purpose.

Although very precise and meaningful data models are indispensable for some use cases,
their complexity comprises drawbacks in most common cases.

Even with a common data model correct and incorrect data need to be handled,
usually we even expect error messages from machines if something is incorrect.

So it is apparent that 

# My research
