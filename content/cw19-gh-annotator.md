---
title: "GitHub annotator/failure map"
author:
- Ilektra Christidi
year: 2019
type: collaborative-ideas
tags:
---
### Collaborations Workshop 2019 (CW19) #CollabW19          2019-04-01 to 2019-04-03

GitHub annotator/failure map - HP5-CW2CC


### **Hackday Idea Proposer**

Ilektra Christidi - ilektra.christidi@ucl.ac.uk

---

### Context / Research Domain

Documentation in general, but especially for software project handover. All research domains.


### Problem

Quite often, a lot of the detail of how and why a piece of software has been developed the way it did, is hidden inside GitHub Issue and PR discussion threads. 

The kind of information that tends to get lost this way are the approaches that didn’t work, since the ones that did have some hope of making it to the final documentation of the package, and they are the code implementation itself. But this failures information is crucial to future developers of the code, saving them time, effort and mistakes by warning them about the things that have been tried and failed.

Another category of information lost this way are the “loose ends”: things that can be improved or features that can be implemented, but did not due lack of time or other reasons. These can spawn new projects/proposals, or improve the codebase in the future.


### Solution

A GitHub app that would help developers keep track of the pertinent information hidden inside Issue and PR comments - not the code or commit message itself - and create a “map of failures”. 

The easiest way seems to be to automatically populate the repo wiki with such pertinent comments, every time a predefined trigger occurs. Possible triggers could be:



*   When closing an issue, you’d have to specify the reason (drop-down, prompt…?): if resolved, provide the PR that resolved it and move on with life (not added to the failures map). If not, provide a reason, which will be added to the map. Same for when closing a PR without merging.
*   When an issue or PR stays open longer than a predefined amount of time, prompt the developer for a reason. Have a “final” kind of text that would prevent bugging them again, possibly with the option to re-start.
*   Manually flag specific comments for persistification (with a magic string…). Hints for when to do this could be when the originally suggested way to solve an issue changes, or the development in an existing PR changes course due to code review comments...

In addition to adding the comment (with a timestamp?) and the link to the Issue/PR that generated it, ideally one would like to prevent the issue, PR and related branch from being deleted in the future.

Another way to present the same info, but not sure how doable it would be, is to annotate a GH timeline of branches/commits with the pertinent comments.


### Diagrams / Illustrations

