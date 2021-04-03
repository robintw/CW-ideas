---
title: "DUQI (Documentation Utility & Quality Interrogator)"
author:
- Rebecca J Arnold
year: 2019
type: collaborative-ideas
tags:
---
### Collaborations Workshop 2019 (CW19) #CollabW19 2019-04-01 to 2019-04-03

DUQI


![alt_text](../images/cw-19-duck.jpg)


(Documentation Utility & Quality Interrogator) - HP8-CW2CC


### Hackday Idea Proposer

Rebecca J Arnold - rjarnold1@sheffield.ac.uk



---


_Idea formed in discussion with group 11_


### Context / Research Domain

All research domains. Helping people improve their documentation.  \
Specifically this should benefit small projects without established documentation practices.

**Problem**

A common question researchers trying to improve their code quality ask is “how do I know if what I’ve written is good, and how do I know what I need to improve?”.  One of the biggest problems with code is poor documentation, with faults such as undefined variables, few comments, no docstrings and broken links. In many small projects, the majority of the documentation consists of comments within the codebase; and this is perfectly acceptable if that is easily navigable.

However there are not easy-to-use tools available for checking for faults such as these, and reporting them. While tools exist for automatic API documentation (e.g. Doxygen) they are relatively complicated and intended more for complex libraries than for the simple scripts that many researchers use for their own work (which can then, later, grow into shared libraries).

Checking documentation quality can be laborious and time consuming, especially for a pre-existing codebase. This means even for experienced coders that are fully aware of best practice, an automated documentation quality reporting tool would be highly desirable.


### Solution

A program which takes code files as input and provides a report/statistics about different facets of documentation quality. Checks/measures could include:



*   Success rate of external link resolution (i.e. find stale web links)
*   Comment to code ratio
*   Completeness of docstrings based on analysis of function definitions

Where possible these would be implemented in a generic way, allowing application to multiple programming languages (e.g. Python, R and Fortran) via a parsing/translation layer. This tool should also be extensible so that modules that check further facets of documentation quality can be included.

If time permits an extension to this project could be to add a documentation enhancement tool. Via this tool following reporting, _optional_ enhancements may be provided (e.g. missing function arguments and type specifications), allowing the coder to edit the existing information. A final step if there has been any enhancement will be to dump the new documentation back to the source code files.

