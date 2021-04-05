---
title: "How to map out software and data skills lessons like Duolingo"
author:
- Dan Katz
- Jeremy Cohen
- Neil Chue Hong
- Olivia Mitchell
- Victor Koppejan
year: 2019
type: collaborative-ideas
tags:
---
### Collaborations Workshop 2019 (CW19) #CollabW19          2019-04-01 to 2019-04-03

How to map out software and data skills lessons like Duolingo - CI8-CW2CC


### **Reporter**

Neil Chue Hong - n.chuehong@googlemail.com


### **Participants**

Dan Katz, Jeremy Cohen, Neil Chue Hong, Olivia Mitchell, Victor Koppejan



---


_This document should be used to capture the information for a Collaborative Session / Hack Day Idea. (The total amount of text should ideally be between 100-300 words and you can include a diagram or two). The document should be no larger than two pages of A4. Don’t delete the details at the top of the document but you should delete all the hint text once you no longer need it._


### **Context / Research Domain**

_Please describe the context or research domain to which the problem applies_

At present, there is no “roadmap” which makes it easy for learners to understand what topics they should move on to next to improve their skills in the areas of software development and data analysis. Additionally, trainers have no standard framework that lets them tweak their lessons to different fields, by showing what skill topics and proficiency levels might be applicable to that field.


### **Problem**

_Description of the problem you are trying to solve_

Although many existing initiatives have tried to map out learning progression, many are overly complex with a level of detail that is too confusing for people who do not have a primary background in the space. They often combine general concepts with specific tools and are hard to maintain and keep up to date.

What we would like is a representation of learning pathways/routes, with well-defined “prerequisites”, “learning outcomes” and “postrequisites”, that enables learners to understand what they could or should learn next, and would allow trainers to categorise/tagging their material. It then allows people to understand what are the most used / most useful things to learn in any particular discipline

The biggest challenge is understanding what level of detail / granularity the nodes should be at, and how to agree what the links between nodes should be.


### **Solution**

_Explanation of the solution to the problem you have identified_

Define a metadata schema for training material (or identify a suitable existing one)

Define specific metadata for existing lesson material (including relationship to other existing material, such as “prerequisites”, “learning outcomes” and “postrequisites”)

Define representation(s) for the metadata that can show relationships of interest to different types of viewers

Build tool(s) that visualize the relationships and the metadata. 

Determine how to maintain metadata over time.

Setup a reviewing procedure for the points above using existing github or equivalent frameworks.

(Very far fetched) build tools that automate the combination of lessons and build new syllabi based on the graph.


### **Diagrams / Illustrations**

_You can include one or two diagrams in this section. Please ensure you have the right to use the image(s), and include an attribution if applicable._


![Skills mapped like duo lingo interface mock-up.](../images/cw19-duo-lino.jpg)



### Discussion below this point

Initial ideas proposed:



*   Victor: Automatically scraping Carpentries material to create “Lighterweight” material, put it into Jupyter notebooks
*   Jeremy: how do you bring together communities and link that to an understanding of how doing this might help things going forward
*   Neil: How do we help support people who are running events to make their events better, specifically making the events more inclusive - where the support can be done via documents, not via personal support
*   Dan: How could there be more funding for software? Making it easier for people who use open source research software to contribute money
*   Olivia: Using Python to code (add metadata) to data, text, and images in the humanities. Making this more more useful to other subjects.

Discussion



*   Dan: How does a new school/department/disciplinary community use existing material produced by others and adapt it / make it relevant with the minimum of effort
    *   Similar to Olivia - by trying to make it easier to apply the techniques developed in one area to another
*   Jeremy: Roadmap for training
    *   Software and Data Carpentry - where do I go next for each domain
*   Victor: did follow-up drop-in sessions and surgeries
*   Jeremy: bottom up understanding of software development vs top down (problem focused)
*   Olivia: learnt the techniques that were directly related to the problem to be solved, then where to go next
*   Jeremy: how to signpost where to go next
*   Victor: hard to explain why some programming concepts are useful, without an example
    *   Similar underlying roadmap, with different discipline specific examples
*   Neil: Skill trees - e.g. learning how to cook - basic skills you need, i.e. learn how to use an oven. Then you could progress towards, say, simple cake making, etc. How would a roadmap work in practice - ensure that they are easy to translate, easy to signpost (can you easily recognise where you are on a roadmap?). Can we ensure these roadmaps are not too expensive to maintain/update? How would you create and design such a roadmap?
*   Does this already exist? 
    *   Example: [https://en.wikipedia.org/wiki/Common_European_Framework_of_Reference_for_Languages](https://en.wikipedia.org/wiki/Common_European_Framework_of_Reference_for_Languages)
    *   Does this become a directory of training courses?



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")


(A bad example of how to do pathways)



*   How would we keep this maintained?
    *   How would we understand how to source the links for what next?
        *   Is this the responsibility of the 
        *   Prerequisites and (post-requisites / learning outcomes)
    *   Developers of new courses and maintainers of existing courses could be responsible for updating the graph data for their courses, once the idea of a graph is accepted and the initial graph has been created
        *   Use the wikipedia "rules" & processes to approve/edit the graph data 
    *   People would add metadata / tags to their lessons containing learning prerequisites and learning outcomes. These could be treated similarly to current issue / pull request system in place for carpentries lesson development.
    *   How do source the common identifiers for these prerequisite and postrequisite “topics”
    *   What levels should these topic 
*   Is a tree the best representation for this?
    *   Is it a linked graph?
        *   The level of detail is important - you don’t need the deep level of details
        *   C.f. data science skills roadmap, want at the level of text mining, statistics, visualisation
*   What’s the metadata schema that you need for each “location” on the roadmap?
    *   Relevant Domains
    *   Proficiency Level
    *   Programming Language
    *   Generality of lesson: E.g., general concept, specific tool
    *   “High level Topic / pathway”? E.g. Data analysis (or is it data cleaning - what level)?
    *   Could use expert judgement or could mine existing materials to identify what people are already using
