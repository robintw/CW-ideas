---
title: "CarpenTREE"
author:
- Arshad Emmambux 
- Patricia Herterich
- Victor Koppejan
- Louise Bowler
- Niall Beard
year: 2019
type: collaborative-ideas
tags:
---
### Collaborations Workshop 2019 (CW19) #CollabW19          2019-04-01 to 2019-04-03

CarpenTREE - DSR12-CW2CC


### **Reporter**

Arshad Emmambux - a.emmambux@soton.ac.uk


### **Participants**

Patricia Herterich - [p.s.herterich@bham.ac.uk](mailto:p.s.herterich@bham.ac.uk) 

Victor Koppejan - [victorkoppejan@gmail.com](mailto:victorkoppejan@gmail.com)

Louise Bowler - [lbowler@turing.ac.uk](mailto:lbowler@turing.ac.uk)

Niall Beard


### Link to initial proposal

[https://docs.google.com/document/d/1CQv-LJejF3pcXIFz0ve1JGMLtUperfxClbTEJbO5VYA/edit](https://docs.google.com/document/d/1CQv-LJejF3pcXIFz0ve1JGMLtUperfxClbTEJbO5VYA/edit)


### Link to final presentation

[https://docs.google.com/presentation/d/1df3kYNx7UquQLJl1x8WnCfnEzQfyYrtsUhdUGAFsaY0/edit?usp=sharing](https://docs.google.com/presentation/d/1df3kYNx7UquQLJl1x8WnCfnEzQfyYrtsUhdUGAFsaY0/edit?usp=sharing) 


### Problem statement

Navigating software /data carpentry lessons isn’t straightforward, it’s not always clear where to go next and how much knowledge you need to start a lesson. Not many people have a complete overview of the carpentry lessons. 

As a carpentry instructor, 

I want to create a customised lesson for a specific outcome 

In order to deliver efficient and tailored training.

As a carpentries student

I want to know which lessons would be a good follow up to what I just learned

In order to get the most out of the software carpentries class and material.


### Envisioned solution / Scope

We envision a tree/visualisation that helps instructors design better sessions and help newcomers design their pathway to gain the skills they want step by step. It will provide and easy overview of the content covered in carpentry lessons.


### Available resources

Prerequisites in Carpentry lessons seem to be tagged with {: .prereq} in the index file e.g. [https://github.com/swcarpentry/hg-novice/blob/gh-pages/index.md](https://github.com/swcarpentry/hg-novice/blob/gh-pages/index.md)

Not all lessons have a wrap - up - could the reference overview help? - Niall, Louise

If we find a reference to those in any of the more advanced, we can link those lessons.



*   We could tag those lessons for ourselves and map them (PH to do that manually for one advanced lesson - and maybe use Niall’s tool to visualise)
*   Look at the different pathway within the software / data carpentry lessons, e.g Ecology, Geospatial, Social Sciences, etc… and check for common lessons and differences. (AE to check for these)
*   
*   Scrape all datasets and see where they are used
*   Scrape for R or python libraries used
*   Scrape all bold words in the glossary sections
*   Scrape instructor guides


### Team skills

Python (except Patricia)

C++ (Vic, Louise)

Javascript (Niall, Louise (mostly in the context of Angular/TypeScript))

Git (All)

Data visualisation - d3 and vega-lite (Louise - but only a couple of months experience on each)

R (Arshad)


### Roadmap

Evening: create a list of all the URLs of reference files comma separated 

One for data carpentry, one for software carpentry?

9-10

Loiuse - Niall -> start scraping

PH + VWK to attempt a manual mapping starting from an advanced lesson

Arshad -> Work on pathways (mainly data carpentry?) similarities and differences in dc curriculum

10-10.30 Document what we have done in step one and discuss next steps

10.30 - lunch 

Setup a small visualization sample in Tess

Continue scraping

Wrangle some data if needed

Work on documentation / presentation framework


### Gates / Milestones

Any GitHub repos:

[https://github.com/vwkoppejan/carpenTREE](https://github.com/vwkoppejan/carpenTREE) 

Do a final issue to the carpentries summarizing what we’ve done and suggestions for them to take this further.

Think about how this could be used for other lesson material that’s not carpentries


### Future works

Branching out the branches of the TREE further

Translation of the carpentry lessons into multiple languages.

Create a dashboard filter that you could filter for lesson time etc. (shiny for R Studio)

---

Advanced: add filters tags to the tree to highlight discipline specific sessions

Advanced: language filters

Go meta: turn this into a data carpentry lesson

