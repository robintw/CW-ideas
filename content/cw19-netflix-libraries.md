---
title: "Netflix of libraries"
author:
- Ben Krinkler
year: 2019
type: hack-ideas
tags:
---
### Collaborations Workshop 2019 (CW19) #CollabW19          2019-04-01 to 2019-04-03

Netflix of libraries - HP12-CW2CC


### **Hackday Idea Proposer**

ben krikler - mr.krikler@gmail.com



---


_This document should be used to capture the information for a Hack Day Idea._


### **Context / Research Domain**

Developers in any research domain that want to find appropriate libraries (this could be extended to other resources).


### **Problem**

Developers can find it hard to** identify suitable software libraries for their work**. Given a problem, deciding on which libraries to use is difficult; even if you know one, it’s hard to f**ind other libraries that do the same thing**, or equivalent libraries in other languages. What is the **approach with the most traction**, particularly within a given community? Which l**ibraries are popular, but low-quality**? **Serendipitous discovery** of libraries is also particularly hard.

Original document: [https://docs.google.com/document/d/1HAIAaHoJCBPi_kG9aNIod2ww2dR3uYbtQ9UGUbH_ZkY/edit?usp=sharing](https://docs.google.com/document/d/1HAIAaHoJCBPi_kG9aNIod2ww2dR3uYbtQ9UGUbH_ZkY/edit?usp=sharing) 


### **Solution**

Building a recommendation system that incorporates feedback, using information from similar individuals, and what packages are present (what signal) in your GitHub repo. Based on these, a NetFlix-style recommendation system could suggest possible libraries, and you could give feedback on how suitable a suggested library is for your application. With sufficient iteration, it would be possible to build up a profile of your tastes or needs and how they relate to other users. This would also make it possible to aid discovery by recommending libraries that other similar developers use.  

A decentralised, user-maintained business model might be easier to sustain. As a result, an initial implementation could work by providing a script or tool that queries existing package and library aggregators and rankers. A user would configure this tool by cloning a template repository from the official github, and setting it to run regularly within a continuous integration pipeline.  Specific customisations like types of packages, licensing, etc, is left in the configuration of the user’s cloned repository.  Additionally, automated summaries of the user’s code (styles, typical package uses, languages, etc) can be produced using the developed tools and stored in the user’s repository.  Recommender functionality that looks at collaborator’s styles and dependencies can work by querying colleague’s public clone of the same repository.


### **Diagrams / Illustrations**




![Proliferation of standards (xkcd 927).](../images/cw19-xkcd927.jpg)


