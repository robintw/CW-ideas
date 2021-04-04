---
title: "Infrastructure to support following up after a workshop / training session"
author:
- Aleksandra Nenadic
- Robin Long
- Louise Bowler
- Jess Ward 
- Ilektra Christidi
- James Graham
year: 2019
type: collaborative-ideas
tags:
---
o### Collaborations Workshop 2019 (CW19) #CollabW19          2019-04-01 to 2019-04-03

Collaborative Idea Group 3 - CI9-CW2CC


### **Reporter**

Aleksandra Nenadic - anenadic@gmail.com


### **Participants**

Aleksandra Nenadic

Robin Long

Louise Bowler

Jess Ward 

Ilektra Christidi

James Graham



---



### Context / Research Domain

Early-career researchers often attend training and workshops orientated around learning good programming techniques and other best practices for producing reproducible, robust research. Training of this type (Carpentries, short courses etc.) is applicable for researchers in a wide variety of domains.


### Problem

People attending training do not always apply the learning to their research after it. There is a problem with motivation of training (e.g. people are in early stages of their PhDs and do not have a concrete problem yet) and sometimes they only realise the importance of the training once something has gone wrong - perhaps applying the lessons would have prevented / mitigated this (e.g. Version Control). There is a fine balance between teaching people these techniques too early or too late. Also, people sometimes feel overwhelmed with the stuff they have been taught (e.g. it may be too abstract) and find it difficult to take it back to their individual research problems and apply it in practice. 


### Solution

Infrastructure to support following up after a workshop / training session. The aim would be to keep people reminded of the lessons, but also to offer additional guidance if required to apply the training into practice.

This may include:



*   A checklist / handbook of how to apply the lessons to your own work
*   A way to manage volunteer time to help - e.g. office hours type thing - needs to fit the requirements of the audience
*   Infrastructure for managing in-person meetings / surgeries (including CoC for setting a positive vibe and a welcoming environment (in particular for beginners) to ensure people feel invited to ask all sorts of questions and can bring their code in any state)


### Diagrams / Illustrations

_You can include one or two diagrams in this section. Please ensure you have the right to use the image(s), and include an attribution if applicable._




### Alternative Ideas


##### GitHub Annotator idea


### Context / Research Domain

Documentation in general, but especially for software project handover. All research domains.


### Problem

Quite often, a lot of the detail of how and why a piece of software has been developed the way it did, is hidden inside GitHub Issue and PR discussion threads. 

The kind of information that tends to get lost this way are the approaches that didn’t work, since the ones that did have some hope to make their way to the final documentation of the package, and they are the code implementation itself. But this information is crucial to future developers of the code, saving them time, effort and mistakes by warning them about the things that have been tried and failed.

Another category of information lost this way are the “loose ends”: things that can be improved or features that can be implemented, but did not due lack of time or other reasons. These can spawn new projects/proposals, or improve the codebase in the future.


### Solution

A GitHub app that would help developers keep track of the pertinent information hidden inside Issue and PR comments - not the code or commit message itself - and create a “map of failures”. 

The easiest way seems to be to automatically populate the repo wiki with such pertinent comments, every time a predefined trigger occurs. Possible triggers could be:



*   When closing an issue, you’d have to specify the reason (drop-down, prompt…?): if resolved, provide the PR that resolved it and move on with life (not added to the failures map). If not, provide a reason, which will be added to the map. Same for when closing a PR without merging.
*   When an issue or PR stays open longer than a predefined amount of time, prompt the developer for a reason. Have a “final” kind of text that would prevent bugging them again, possibly with the option to re-start.
*   Manually flag specific comments for persistification (with a magic string…). Hints for when to do this could be when the suggested way to solve an issue changes, or the development in an existing PR changes course due to code review comments...

In addition to adding the comment (with a timestamp?) and the link to the Issue/PR that generated it, ideally one would like to prevent the issue, PR and related branch from being deleted in the future.

Another way to present the same info, but not sure how doable it would be, is to annotate a GH timeline of branches/commits with the pertinent comments.


### Diagrams / Illustrations

_Notes:_

_Illekra: documentation needed for handover, issues and pull requests hide many information and wealth of knowledge  and documentation. What happens if something fails or is abandoned. Or pull requests stays for a year unattended. What do you do when someone else inherits this projects. Pull requests to stay open too long - to poke the person responsible, why something is abandoned, flag things to trigger certain actions and transfer them into wiki into github._

_Louise: Thing that are useful, important - a way to flag them is needed._

_Jess: Map of the failures, so you do not take the same turn that people have already been before that did not work. _

_Annotate a timeline? Talking about comments not a commit. Shove comments into permanent #documentation. _


##### Idea 2 - Docuflow


### Context / Research Domain

_Please describe the context or research domain to which the problem applies_

Documentation in software or projects


### Problem

_Description of the problem you are trying to solve_

Many pieces of software lack documentation. There can be many reasons for this such as not knowing: How to document, Why to document, What types or documentation, or what methods exist to document.


### Solution

_Explanation of the solution to the problem you have identified_

Create a flow chart / board displaying concepts under categories. This links to descriptions of Why that concept is need, how to enact it, and tools/links that can be useful.


### Diagrams / Illustrations

		


<table>
<tr>
<td>			 
<p>
Comments in Code
<p>
	
</td>
<td>			
<p>
	 Readme
<p>
	
</td>
<td>	
<p>
  GitHub Readme
<p>
	
</td>
</tr>
<tr>
<td>	
<p>
     Style Guide
<p>
	
</td>
<td>		
<p>
	Tutorials
<p>
	
</td>
<td>	
<p>
   Developer Docs
<p>
	
</td>
</tr>
<tr>
<td>          
<p>
	   User Docs
<p>
	
</td>
<td>			 
<p>
   Requirements 			
</td>
<td>	
<p>
	DocStrings
<p>
	
</td>
</tr>
</table>


**ReadMe:**

**_Why?_**

_README files should help people get started with installing the software and running it.  Without it user may not know how to install or use the software._

**_How?_**

README files are usually a text file (.txt).  These would README files typically contain instructions and additional help as well as details about patches or updates.

_You can include one or two diagrams in this section. Please ensure you have the right to use the image(s), and include an attribution if applicable._

_Robin: how to document things - documentation templates - simple web page resource information you select the type for documentation that you want or are creating with info on how to comment e.g. for a programming language and there are links to read more about each of the resources (with a small description for each). Almost like a hidden flowchart of things that need to be done._

_James: You should provide licence, that gives you one start, then more metadata gives you 2 stars, building like levels of progression of what needs to be done with an idea of building onto what can I do to make my dataset better. _

_Aleks: Guidelines are useful.  It’s often not obvious to people what decisions they should be making.  E.g. Should I have a readme (yes), should it be Markdown?  Are other formats okay?_

_Louise: Guidance and having step by step ways of doing things is important. _

_Illekra: are there standards or guidelines for this._

_James: level one: README and licence files, but then more higher up people would argue what goes in the process. Some helps and prompt and links about what licence to chose, what should go into README file, etc._

_Jess: even very fundamental guidance what goes into README._

_Robin - in the templates - we need guidance with info on why this particular things is important to do this and how to do it. _

_Louise: Community ready checklist built into GitHub - under a repo within a github organisation  then Insights/Community but only for public repos - maybe pro only accounts on GitHub have this. But only one person from a group knows about this and the rest were not aware._


##### Idea 3 (more of a problem at this stage!) - some sort of infrastructure to follow up after training


### Context / Research Domain

_Please describe the context or research domain to which the problem applies_

Early-career researchers often attend training and workshops orientated around learning good programming techniques and other best practices for producing reproducible, robust research. Training of this type (Carpentries, short courses etc.) is applicable for researchers in a wide variety of domains.


### Problem

_Description of the problem you are trying to solve_

People attending training do not always apply the learning to their research after it. There is a problem with motivation of training (e.g. people are in early stages of their PhDs and do not have a concrete problem yet) and sometimes they only realise the importance of the training once something has gone wrong - perhaps applying the lessons would have prevented / mitigated this (e.g. Version Control). There is a fine balance between teaching people these techniques too early or too late. Also, people sometimes feel overwhelmed with the stuff they have been taught (e.g. it may be too abstract) and find it difficult to take it back to their individual research problems and apply it in practice. 


### Solution

_Explanation of the solution to the problem you have identified_

Infrastructure to support following up after a workshop / training session. The aim would be to keep people reminded of the lessons, but also to offer additional guidance if required to apply the training into practice.

This may include:



*   A checklist / handbook of how to apply the lessons to your own work
*   A way to manage volunteer time to help - e.g. office hours type thing - needs to fit the requirements of the audience
*   Infrastructure for managing in-person meetings / surgeries (including CoC for setting a positive vibe and a welcoming environment (in particular for beginners) to ensure people feel invited to ask all sorts of questions and can bring their code in any state)


### Diagrams / Illustrations

_You can include one or two diagrams in this section. Please ensure you have the right to use the image(s), and include an attribution if applicable._

_Louise: Reproducible research - courses given to students - but they still do not know how to do it and take it into practice._

_Post-workshop surgeries to help with this. LEt people come for training for the second time._

_Jess: Give pilot projects to students post training e.g. play with git._

_Problem with motivation - people come too early and do not know why this teaching is valuable. _

_Illektra: mentoring scheme, follow up with students, set monthly meetings for this. Sitting and coding with them also helps, 1-2-1 approach. _

_Aleks: Like a post-workshop aftercare?  Some people come to SWC twice, the first time they didn’t quite see why it was important, come back once they’ve had the problem and understand the importance_

_Robin: Bring your own problem, almost 1-2-1 sessions_

_James: some RSGs have this - an RSE comes and spends an hour every other week with a certain project, almost like a temporary RSE placement in a particular group or project._

_Louise: The above is great - really rewarding when it works, but time is an issue for most RSE groups._

_Illektra: Community version of support - remote and using screen sharing, distributed mentoring. _

_Robin & Illektra: we may need github for this and than have some sort of matching between requests and mentors, or they can just scroll through and give comments_

_Jess: Someone volunteers an hour of their time and people can come and talk, would be useful for beginners in particular, set the vibe that there are no stupid questions_

_James: most people do not think their code is good enough to share, but need to make clear that we do not judge people for their code and some kind of policy or guidance to help improve and give advice to researchers writing code - make sure it’s fair and constructive - they have been trying to implement this at Soton, would like to do this but still at the initial policy level_

_Robin: not specific RSE help but questions around - am I putting enough comments, is my code in the right style for the programing language used?_

_Jess: documentation around whether someone else can reproduce this piece of code?_

_Illektra: The SSI should provide this system in some way for local RSGs to use_

