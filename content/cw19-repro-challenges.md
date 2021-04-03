---
title: "Reproducibility and Collaboration Challenges in interactive / exploratory research"
author:
- Adam Jackson
- Dav Clark
- Adam Jackson
- Becky Arnold
- Ben Krikler
- Joanna Leng
year: 2019
type: collaborative-ideas
tags:
---
### Collaborations Workshop 2019 (CW19) #CollabW19          2019-04-01 to 2019-04-03

Reproducibility and Collaboration Challenges in interactive / exploratory research


### **Reporter**

Adam Jackson - magicguy@gmail.com


### **Participants**

**_Dav Clark_**

_Programmer / Evangelist at [Gigantum](https://gigantum.com/)._

**_Adam Jackson_**

_Computational scientist / researcher (from pure PostDoc -> RSE). Produced code as part of research, mostly glue for expensive HPC._

**_Becky Arnold_**

_Astrophysics PhD at Sheffield. Worked on [Turing Institute](https://www.turing.ac.uk/) project. _

**_Ben Krikler_**

_More of a user - particle physicist at CERN. Cluster-based computing. Often exploratory, determine appropriate distributions, features, etc. Python - more Jupyter, using Binder for interactive reporting (though not for sharing back very much)._

_“Data gravity” is a problem? Data replication with URI is a solution used there. Some increase in sharing software._

**_Joanna Leng_**

_C++ enthusiast. EPSRC (UK org) RSE fellow. Works with physicists on imaging data, recently with sociologists. Also works at Diamond Light Source - funding for soft matter microscopy vs. hard matter. Is working across modalities, which leads to desired common software base._


### **Notes from the discussion NOT for inclu**sion in blog

_One concern (Dav+Joanna): enabling collaboration between diverse skillsets (e.g. sociology + RSE)._

_Problematising current RSE title - maybe needs to be differentiated more, allowing for different kinds of roles._

_Funding for tools that are useful outside of one grant._

_Also concern about losing true expertise. Faculties are being reduced and integrated - using same tools. Tension between disciplinary boundaries vs. fluid interdisciplinarity._

_Minimizing lines of explanation about the exploratory process (e.g., “this didn’t converge, so we nudged it”).Conversion of programs to a literate product. More on the post-processing (not the expensive stuff)._

_Concern about cache hanging around in notebooks._

_Interactive / exploratory visualization._

_Chris Woods (from Bristol) about future of Cloud computing -> shifting HPC to the cloud. Ben is working on this as well. Working with Oracle for cluster in the cloud. Enables doing viz while computation is happening. Concern about user support for Cloud._

_How could we do bursty exploratory analysis? Probably leads to under-utilization of system. Maybe if you have a set of expected potential outcomes you can code this a little more efficiently._

**_Topics_**

*   _Rapid Human QA / Viz_
    *   _e.g., well-designed plots for brain imaging_
    *   _3D plots are hard to do any way except interactive_
    *   _Infinite set of ways that things can be wrong - human visual system is so fancy_
    *   _Hypothesis generation - concerns about automated data cleaning_
*   _Understanding outputs of complex, automated analyses_
    *   _Understanding machine learning for separation of examples - what has the algorithm done?_
*   _Transparency / Reproducibility_
    *   _Version control everything_
    *   _Restricted data (esp. for reproducibility)_
    *   _Capture computational environment_
        *   _Containers are hard to design without knowing what data will be used, what will be persisted_
    *   _Git all the time, changelog? Capturing meaningful points in time?_
*   _Scaling from locally tested to scaled-up/out, etc._
    *   _Data portability_
    *   _Data restrictions_
    *   _Availability / cost of compute_



---



### **Speed Blog**

_Please use the area below to draft the speed blog. Consult [https://www.software.ac.uk/speed-blogging-and-tips-writing-one](https://www.google.com/url?q=https://www.software.ac.uk/speed-blogging-and-tips-writing-one&sa=D&ust=1554127339457000) for information, tips and examples._



---


At the Software Sustainability Institute’s 2019 Collaborations Workshop, many discussions for the speed-blogging session focused on deposit of relatively fixed data and analysis code. Our group noted that there is value in reproducibility across the research process - e.g., in facilitating collaboration within a team, or even portability across compute environments within a lab. Moreover, it is well documented that even basic computational reproducibility with the same code and data remains a challenge. Baking in concerns about reproducibility starting at the earliest explorations could increase the number of projects that are genuinely reproducible and amenable to extension and further exploration. Below we highlight key topics and include example suggestions, practices, and tools that can facilitate reproducibility and collaboration from the start of the research project.

**Reproducibility/transparency**

Exploratory research often treads a winding path, circling back on itself and running into dead ends. This presents a barrier to reproducibility as it makes it difficult to track backwards from the final conclusions of a research output and the path of code/results/hypothesis that lead to them.

Making extensive use of a version control tool such as [Git](https://git-scm.com/) can be a big step towards mitigating/eliminating this problem. By using atomic commits (committing each small unit of work to version control) with a detailed commit message explaining why the step was taken can allow others (or your future self) to “retrace your steps”.

Another important step for making research reproducible is to capture the computational environment it was conducted in as the behaviour of software can change depending on it environment. In research this translated to the same piece of code generating different results on different computers- i.e. the result will be irreproducible. There are a number of ways of capturing computational environments, all of which have their own strengths and weaknesses. Containers offer possibly the most “complete” or fully-controlled approach to replication, but present a steep learning curve. Further they can be inflexible if, after further exploratory research, the environment needs to be changed, for example by adding another piece of software.

Another barrier to reproducible research is when the research involves working with confidential information such as medical or commercially sensitive data. In cases like these, full anonymisation of results may be difficult and laborious, making it undesirable to apply to every step of the research process. This skirts the boundaries of open research and reproducible research. Research can be reproduced far more widely if it is open, but reproducible research does not _necessarily_ have to be open. Even if only those with clearance to access the information are able to reproduce it, the research is still reproducible. As such it is good practice to carefully document and version control all steps of the research process, even if those cannot be shared. Working reproducibly has a myriad of benefits for research quality even if the research cannot be shared.

Interactive exploratory research presents another barrier to reproducibility. Say a researcher generates a 3D plot, interacts with it, spins it around, and comes to a conclusion, then that process and what that researcher exactly saw can be difficult to reproduce. This is an example of why it is so important for researchers to take extensive and detailed notes.  

**Portability and Subsetting of data**

Exploratory work will often be performed with relatively “raw” data, which in turn can involve large files and mixed formats. In the early stages of a study it may not be clear how high-quality or noisy the data is, or indeed what is relevant to later outcomes. As a result, some of the best-practices for reproducible research (_“upload everything with human- and machine-readable metadata to somewhere as available and immutable as possible”_) become more cumbersome or even technically or economically infeasible. 

During an interactive process we want to access and process data quickly, which generally means working with a local copy. It is not generally practical (or even permissible) to upload all of the data that was even considered for analysis, which means a curation/pruning step is needed to present a reproducible environment. Containers are an emerging and powerful tool for robust well-defined computational processes, but the technology is led with a focus on web applications. The run-time environment of a container is destroyed when the container is stopped, and best-practices around durable data persistence are not well defined. For example, bind-mounts may incur a large performance penalty (especially on Windows or macOS) but at the same time, they provide easy persistence and accessibility. 

The results is that separate protocols are needed for making data available to a container session, and also for extracting and persisting useful outputs. There seems to be a conflict between the design to make sessions independent and predictable, and the desire to freely explore while logging the progress (a conflict that is similarly expressed in the problems of invisible state persisting between Jupyter cell executions)

.

**Portability and Easy Configurability of Compute**

Mobility of compute is defined by Greg Kurtzer in [his paper describing Singularity](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0177459). The basic idea is that compared to the bits required to describe your data, the bits required to describe your computational steps are typically far fewer - and therefore more portable. A challenge arises due to the dramatic differences between some compute contexts. For example:



*   file systems differ, including distributed networks;
*   different compute architectures may be available: multi-core, GPU, other accelerators
    *   (In some cases, libraries (e.g. linear algebra) may need to be compiled specifically for an architecture and may have even have different semantics); and
*   different modes of interaction may be required, e.g. desktop vs. batch systems.

So, while in theory container approaches like Docker or Singularity “solve” the challenge of portability of compute, there are many details that remain to be addressed.

We are aware of a variety of approaches to addressing these remaining challenges. The approach adopted by Gigantum is to reduce cognitive load and streamline standardized strategies. E.g., by defining a dataset which may be attached to a compute project, and which can intelligently fetch only needed data for local tyre-kicking, and provides sensible descriptors for data location on an HPC system. Another class of approaches is to define an API that intelligently maps onto a variety of back end compute architectures. For example, Dask reproduces a subset of numpy and pandas APIs that work on distributed clusters (cf. Spark, etc.), libraries like PyTorch flexibly work across CPU and GPU, and the PARSL library provides annotations that allow users to inform the runtime of what functions can be run in parallel.

Even having solved these technical challenges, most strategies are still going to require a modest amount of “dev ops” sophistication. Docker can be cumbersome, designing good requirements files for package installation requires a balance between hard requirements and flexibility of working across versions of needed packages. While many voices in reproducible research advocate for training and practices, there remains a clear place for innovation in tools. For example, the repo2docker project provides a set of standard approaches that will reliably support a binder instance that can be inspected by anyone. Tools like Gigantum take this further by automating Git and providing a UI around things like package management and Dockerfile generation and execution.

**Rapid Human Quality Assurance / Visualisation**

Exploratory data analysis and visualisation is the process of iteratively improving your understanding of the underlying data and physical processes in order to respond to a particular research question.  

It occurs in two possible research processes, either in incremental research when an existing research approach and work flow is being slightly updated or tested on relatively similar, but new, data; or in disruptive research when a completely new approach to the experiment or analysis is used.  

In incremental research, one normally has an understanding of what to expect, and open-ended exploration will only kick in when an anomaly is observed. Being able to compare the anomaly to a previous result, or using a simulated or parameterised model can help understand how the anomaly has occurred. Alternatively, variation of the analysis workflow can allow the researcher to test several different hypothesis for what has produced the anomaly. In both cases, getting new updated results quickly and keeping them organised is important to identify what has gone wrong.

In a disruptive approach, however, there is some expectation as to what the data will show but the approach needs to be open to spotting problems. Often in this case the research question itself might evolve, as will the analysis workflow, since it is difficult to predict before starting the research process what will be the best approach to answer the research question.

**Summary**

The contributors to this post widely agreed on the clear challenges for computational reproducibility, and how these challenges are exacerbated by the demands of interactive and exploratory work. Our suggestions range from training and practices for manually tracking activity and computational environments to near-complete automation in an integrated graphical environment. We look forward to hearing from others in the larger conversation as we proceed to improve the state of reproducibility and collaboration across the entire research lifecycle!

