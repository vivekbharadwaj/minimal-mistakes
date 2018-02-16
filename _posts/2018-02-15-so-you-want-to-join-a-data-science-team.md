---
title: "So you want to join a data science team"
excerpt: "Choose wisely..."
layout: single
header:
    overlay_image: /assets/images/data-science-team.jpg
    overlay_filter: 0.2
categories:
  - data science
  - infrastructure
  - team composition
tags:
  - data science
  - joel test
author: "Vivek"
date: "15 February 2018"
hidden: false
---

Let's face it. The biggest benefit to the hype created around data science and artificial intelligence is that, in most markets, data scientists have considerable choice and buying power. If you're a skilled and experienced data scientist, companies need people like you, and will not hesitate to make their intentions known.

I recently read this awesome blog post by Eric Colson from StitchFix about the three things to look for in a company that could make it a great place to work for a data scientist. I'll summarise his main points here:
- **Work for a Company that Leverages Data Science for its Strategic Differentiation**. The key takeaway is to look at companies that use data science to differentiate themselves from competition as opposed to simply use AI in their sales story or merely use data science as a support function.
- **Work for a Company with Great Data**. The takeaway here is to look at companies which has access to or collects interesting data. Most company product internal data is not calibrated well enough to easily extract signal from the noise. This takes you away from the actual science into instrumentation, logging and engineering aspects. These aspects are crucial but you may not have the right expertise to actually implement them, nor might it give you the best return for your time. 
- **Work for a Company with Greenfield Opportunities**. The takeaway here is to look at companies that have unsolved optimisation problems. When you have such problems, a little creative problem solving approach and some simple models often give huge returns. In contrast, companies with established data science and machine laerning teams will have you spend 2 weeks on a project that lifts CTR by 0.5% , which is great but not hugely satisfying to the ego.

There's plenty of gold in the [entire post](https://multithreaded.stitchfix.com/blog/2015/03/31/advice-for-data-scientists/) worth recommending a read. Reading his article however reminded me of the "Joel Test" for software engineering. To give some additional context, Joel Spolsky is the CEO of StackOverflow. Back in 2000, he spun up a  ["highly irresponsible, sloppy test"](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/) to act as a quick litmus test about the seriousness and maturity of a team to practice software engineering as opposed to product hacking.  

![Joel test]({{ site.url }}{{ site.baseurl }}/assets/images/joel-test.png)

image courtesy:[joel on software](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/)

Knowing whether the company uses source control or continuous integration or does usability testing isn't mission critical to the software engineers' job by itself. The idea is that asking these questions gives you a quick barometric sense of your day-to-day activities. If I have to think of a similar litmus test for data science teams, I'd definitely look out for Eric Colson's points mentioned above. Some other aspects I'd want to know before I sign up are:
- (if it's a product organisation, then) is there an established method for extracting product attributes from transactional data, logs and user feedback i.e. an analytical database or a data mart with the right metrics and attributes
- in what manner and how often do management implement strategic insights from their data scientists into business decisions
- (as a follow up to the previous point and more applicable if it's a product organisation,) how data driven are management decisions in the company? is the goal of a project to increase some second-order product metric or to implement "because the client wants it". was this question actually surprising to them
- who is the executive sponsor for data science and machine learning within the company. how does the sponsor envision DS / ML to play a role in the company strategy
- (if you're the first data scientist in your company, then) what infrastructure frameworks already exist within the company to help management with product analytics, experimentation and algorithmic model building
- what's the expectation about progression of responsibilities in the next 6 months? how will this change after 12 months?
- what kind of supporting infrastructure in the form of data engineers, reporting / visualisation analysts, dev-ops, ML software engineers and DBAs exist inside your function. whats' the extent of your interaction with them
- how easy it is for you to reproduce past results and experiments. does the team practice package management? is all past code, data and supporting artefacts archived? how important is reproduciblity to the team?
- how easy and flexible it is for you to access stakeholders to test and retest hypotheses. are they co-located and how flexible is the organisational hierarchy

Of course, which of these company attributes are a must-have as opposed to a 'nice-to-have' is a function of the data scientists' ability, skillsets and experience as well. If you're starting out in the field, you may not benefit tremendously from the autonomy of greenfield opportunities. If you're the first data scientist in a company, then creating an on-demand and scalable compute infrastructure may not be on the top of your mind whereas you may be interested in tackling the "low hanging fruits". 

To make sense of all these factors in perspective, it's probably better to put them in a 2x2 or an X-Y coordinate graph. In fact, I'd love to see someone plot all of the joel test like features as false positive rates and an honest self-introspection of skillsets as true positive rates in an ROC AUC curve. Then, finding the right "fit" would be a simple matter of identifying the right "threshold" that you're comfortable with. The fact I find this amusing probably means that I need a vacation.

![ROC Curve]({{ site.url }}{{ site.baseurl }}/assets/images/ROC-curve.png)

Do you agree with the signs I've mentioned above? As a data scientist, what else do you look for in your dream data science team?

Notes: <br>
- Cover Image courtesy: [shutterstock](http://www.smartdatacollective.com/wp-content/uploads/2013/01/shutterstock_118303750_1.jpg) <br>
