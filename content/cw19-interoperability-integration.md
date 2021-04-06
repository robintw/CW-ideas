---
title: "Interoperability & Continuous Integration"
author:
- Kirstie Whitaker
- Mosè Giordano
- Richard Gilham
- Aleksandra Nenadic,
- Alexander Konovalov
- Adrian Castravete
year: 2019
type: collaborative-ideas
tags:
---
### Collaborations Workshop 2019 (CW19) #CollabW19          2019-04-01 to 2019-04-03

Interoperability & Continuous Integration - DSR2-CW2CC


### **Reporter**

Alejandra Gonzalez-Beltran - University of Oxford, [http://agbeltran.github.io/](http://agbeltran.github.io/),twitter: [@alegonbel alejandra.gonzalez.beltran@gmail.com](http://twitter.com/alegonbel) 


### **Participants**



*   Kirstie Whitaker, Alan Turing Institute, [https://whitakerlab.github.io](https://whitakerlab.github.io), twitter: [@kirstie_j](https://twitter.com/kirstie_j), [kwhitaker@turing.ac.uk](mailto:kwhitaker@turing.ac.uk) 
*   Mosè Giordano, UCL, [https://giordano.github.io](https://giordano.github.io), Twitter: [@MoseGiordano](https://twitter.com/MoseGiordano)
*   Richard Gilham (Met Office) [richard.gilham@metoffice.gov.uk](mailto:richard.gilham@metoffice.gov.uk)
*   Aleksandra Nenadic, The Software Sustainability Institute, [a.nenadic@manchester.ac.uk](mailto:a.nenadic@manchester.ac.uk) 
*   Alexander Konovalov, University of St Andrews, [alexander.konovalov@st-andrews.ac.uk](mailto:alexander.konovalov@st-andrews.ac.uk) 
*   Adrian Castravete, figshare, [adrian@figshare.com](mailto:adrian@figshare.com)


### **Notes from the discussion**

_Please use the area below to capture notes from the discussion session._



---


What is the definition of interoperability? Data (validation), systems, configuration 

Metadata in github and check validation 

Swagger for API definitions, describe what your data should look like for request and response

Integration tests to check the data

Meta-languages

What kind of training is needed in this aspect? What SSI can do to support this intermediary level training? What materials are needed?

What is the meaning of being interoperable? What is the metric that measures interoperability? Continuous integration as the tool that could help to achieve it. Interoperability as an end goal.

Other view is continuous integration as the tool that allows you to do integration testing and then interoperability as one of the steps along the way

What do you we mean for continuous integration?

CI for testing but actually is a part. 

Making sure that your systems communicate like that

Regression tests, continuous means I’m running them for any change in the code; the action is triggered by every commit. 

Weekly test payloads - HPC for testing to deal with the Met Office data 

Foundation of interoperability - as CI runs in a “different machine” 

Freezing/pinning library versions - 

Defining continuous integration:



*   integration: you’re combining all the new versions into the main project and running tests to see if you’ve changed the behaviour of the software
*   continuous: you’re ALWAYS testing, every change you make triggers a new run of the suite of tests

Defining integration: 

Problem with dependencies - mock testing - how can CI help in testing system interoperability? Can it be used?

Documentation-driven development vs test-driven development, this is the next step - you need to figure out what you need and what you are going to output - then you write your doc stings/method signatures - then write the tests based on the spec and then you write the code.

In terms of training, can you talk about testing and testing quality, without mentioning interoperability? Yes, you can teach them separately and then bring them together. One is a practice , another one is a goal. It is the mindset, you need to understand the concept of someone else will be doing something else with your code or extending your code or dataset - there should be some consideration a priory of what that person's will need. System interoperability is moving towards continuous integration. No one knows how to review code when it is submitted to a journal. 

Notion that someone else will use your code, someone else will use your dataset

Data standards

MRI data, brain imaging, machine learning people would like interoperability standards, so it is driven by research.

Standard, not a tool. Standard as a concept, not just a tool. You are working with concepts rather than specific things, as people get bogged down in a specific tool. People need to appreciate that the value is not in their lines of code or their data it’s what they do with it. People who see value in their source code - they won’t share. It is closed off and not interoperable. 

Software horror stories due to interoperability issues: NASA, use of metrics units and English units.


### **Speed Blog**

_Please use the area below to draft the speed blog. Consult [https://www.software.ac.uk/speed-blogging-and-tips-writing-one](https://www.google.com/url?q=https://www.software.ac.uk/speed-blogging-and-tips-writing-one&sa=D&ust=1554126888920000) for information, tips and examples._



---



## What is the relationship between continuous integration practices and interoperability?

Continuous integration (CI) practices and interoperability are two separate concepts that can also complement each other in practical terms, but first let’s try to motivate why different people in an academic ecosystem would care about these two concepts.

<span style="text-decoration:underline;">Case study 1</span>: Jane, a **researcher** who wants other people to use her data.

Jane needs to think at the beginning of her study about what the other users will need to know when the data collection is complete. She thinks about documenting her protocol, adding metadata to each of the variables she collects, and (if available) adhering to a particular data standard relevant to her research field. She wants to make it really easy for new people to download her data and know what each row, column and file contains.

It’s great that Jane is thinking about _interoperability_ at the start of her project...but we all know that things may change as the real data starts coming in. Maybe there needs to be an additional column or free text comment? Perhaps there will be an additional file to note repeated measurements? In these cases it’s good to think about some tests to make sure that the documentation stays in sync with the actual data. Specially when using an existing data standard, it is necessary to add tests checking that the representation is valid after every change. Thus, we’d recommend that she _continuously integrates_ her data with tests as she proceeds with her study, rather than wait until the end to fix all the things that changed in the design.

<span style="text-decoration:underline;">Case study 2</span>: João is a **research software engineer** who wants other people to use his software.

We recommend that João talks to a lot of potential users of his code. The main thing he needs to think about at the beginning of the project is what format they’re expecting to read the data in from, and how they expect the output data to look. What he’ll probably find is that different teams have different requirements, so he might want to consider building a few different input/output commands, and adding some _continuous integration_ tests to make sure that they work as he builds the code. If the researchers have to do some additional work to re-format their datasets before they hit this point in their workflow they’re much less likely to use this new tool. If his software is _interoperable_ with other tools that researchers are using then hopefully they will adopt this new process.

<span style="text-decoration:underline;">Case study 3:</span> Juan is a **data librarian** who wants to make it easy for researchers in the digital humanities to access and reuse lots of different datasets for their natural language processing analyses.

Each of these different research groups are using different corpora and that means their analysis code is written specifically for their corpora and it makes it difficult to adapt their code for others. One thing that Juan can do is work on making the most popular collections _interoperable_. He can write a little piece of code that will move one corpus into the format of a different one. Before the researchers use this transformed data they should probably check that it matches what they expect! Are there any empty columns? Are the values scaled in a different way? If not, then they should tell Juan that his piece of code needs updating. If they are _continuously integrating_ these changes then Juan doesn’t have to go running around the department making sure that everyone else is using the most up to date (and most correct) version!


### What is interoperability?

Interoperability is usually defined as the capability of a system to exchange and make use of information. There are different aspects of interoperability: interoperability at the data level (systems exchanging data) and interoperability at the systems level (systems interacting and sharing common interfaces). Data interoperability can be further categorised between syntactic and semantic interoperability. Syntactic interoperability concerns the use of data formats, while semantic interoperability refers to the uses of common vocabularies. Standards are fundamental resources to achieve interoperability. 


### What are continuous integration practices?

Continuous integration is a tool that can help in achieving data and system interoperability. For example, via continuous integration it is possible to validate data against the specific standards. CI can also be used to verify requests and responses when defining API interfaces. 

Continuous integration (often abbreviated as CI) is the next step after the project established a set of regression tests (which could be integration tests, unit tests, or both). Using CI tools, one can run these tests for every change made in the code (e.g. commit to the master branch) or being proposed (in the form of a pull request). It helps to ensure that suggested/committed changes do not break the functionality of the application. “Continuous” means that the set of tests is run for EVERY change and not, for example, nightly or weekly - the latter approach will work if computational resources are limited, but will make identifying changes that broke it more difficult. Note: using CI efficiently requires certain commit discipline: we recommend to commit often and made commits atomic: e.g. do not combine several unrelated changes in one commit, and do not spread related changes in several commits (this will break bisecting the history of changes). [Maybe too many technical details, needs shortening]. 

CI tools allow to automate testing in a range of different combination of settings (OS, dependencies, configuration, etc.)

 

What you can test with CI if you have data, not software?



*   Run automated tests that check data integrity (e.g. format of each entry matches the documentation) and consistency (e.g. there are no logical contradictions between values of different variables)
*   That data may be processed by a variety of tools working under different OS, built in various settings (e.g. 32-bit, 64-bit)


### How Continuous Integration can help achieve interoperability?

_What is the metric that measures or maintains interoperability? Continuous integration is a tool that can help to achieve interoperability by providing means to test what you are interested in over all plausible use cases. Successful use of integration testing achieves the aim of interoperability._

_Interoperability is about standards and concepts, not reliance on specific tools. Tools can help ease the workflow to achieving it._

_Foundation of interoperability - that fact that CI runs on a “different machine”._

_Other view is continuous integration as the tool that allows you to do integration testing and then interoperability as one of the steps along the way._

_What do you we mean for continuous integration?_

_CI for testing but actually is a part. _

_Making sure that your systems communicate like that_

Regression tests, continuous means I’m running them for any change in the code; the action is triggered by every commit. 

Weekly test payloads - HPC for testing to deal with the Met Office data 


### How can training help addressing the potential skills gap to apply Continuous Integration in the context of Interoperability?

Courses on CI and interoperability can be totally independent of each other, and in fact, teaching on each of these concepts does not need to include mentions of the other concept. We believe that there is an opportunity to offer separate training courses around (1) quality of code and testing and (2) interoperability, and then bring them together. One can be thought of as a good practice, while the other one is the end goal. Interoperability is also the mindset - people need to understand and be trained in the concept of someone else using, extending or doing something entirely else with their code or dataset - so there should be some consideration a priory of what that next person's may do or need. 

