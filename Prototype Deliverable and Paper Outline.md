# Milestone 2: The Outline of Quantum Communication Network along with Optimzed Cryptographic Algorithm

## Due Date
Apr 2nd 

**Submit a GitHub repo link to canvas**
**Add Dr. Hale as a collaborator on your GitHub Repo**

## Overview

- [Setup Environments](#environment-setup)
- [Project realization](#project-realization) 
- [Research Paper Outline](#research-paper-outline)
- [Visual understanding (aka diagrams)](#diagrams) 
- [Issue Tracking / Planning](#issue-tracking-and-planning)
- [Presentation](#presentation)

## Environment setup -  Establish needed tooling and work environments
The Environment setup instruction will be available [here](https://github.com/Vidmaster/cybr8950-quantum/blob/main/EnvironmentSetup.md).

#### Grading Criteria

| | Meets expectations (27-30) | Some Issues (16-26) | Does not meet expectations (0-15)|
|---|---|---|---|
| Documentation | Documentation is clear and concise, but provides sufficient detail to understand the basic setup details. | Some documentation exists, but it is piecemeal or not entirely clear. | Little or no setup/configuration documentation or it is very hard to follow.|
| Works as expected | Installation instructions work as expected and correctly setup needed tooling/environments.  | Some minor problems during setup, but instructions mostly work. | Many significant issues in instructions makes setup difficult or impossible. |

**Total 60 points.**

## Project realization - Clearly document your efforts towards achieving the project methodology. Progress Report (04/02/2021)
 1. Identify tasks achieved from your backlog
 2. Document the product increments (an agile term for the things you produce) generated in this milestone
 3. Bind tasks, code artifacts, and documentation together

## Overview
(insert brief overview of efforts made)

As implementation of quantum cryptography protocols is a major goal of our project, we also need to consider which quantum programming languages or frameworks should be used. 
To a large extent this selection may be guided by the protocols themselves, as the different languages we have examined are suited for some uses over others. D-Wave provides
annealing quantum computers, while IBM provides gate-based quantum computers, and Xanadu provides photonic quantum computers. Each of these has its own strengths and 
weaknesses, and requires a different programming language to operate. As we consider the implementation of protocols further, we are likely to discover that some are simply 
not possible for us to implement currently, and others require implementation on a specific type of quantum hardware.

## Outcomes
 We anticipate that we will be able to make a set of recommendations toward confidentiality, integrity, and non-repudiation based on the state of the art in quantum 
 cryptography, as well as demonstrating their usability where implementations are feasible. We believe this research will be valuable, as there are many possible approaches 
 being proposed for quantum cryptography, but very few broad surveys of all these diverse techniques. Through the enumeration, classification, and evaluation of various 
 protocols, we hope to guide both researchers looking to iterate on past work and practitioners looking for ways to begin implementing quantum cryptography.

also list them out like this:
* outcome 1: Twin-field Quasi-real-time Quantum Key Distribution system can be used to enhance both security and efficiency during the transmission. 
* outcome 2: Optimized Decoy-state Quantum Key Distribution can be used for long distance comminication with lower latency. 
* outcome 3: BB84 QKD protocol is a most achieveable and reliable scheme to use in a short distance communication (around 200 ~ 240 km) with valid transmission rate. 
* outcome 4: Measurement device independent QKD (MDI-QKD) is the most secure QKD protocl in current stage becuase it remove all (existing and yet to be discovered) detector side channels.

We have analyzed several QKD protocols to seek out which one is best use or appropriate to our client. More comparison information can be visited at [here](https://github.com/Vidmaster/cybr8950-quantum/blob/main/QKD%20Protocols.md). 

## Hinderances
(insert brief discussion of challenges encountered)  

As implementation of quantum cryptography protocols is a major goal of our project, we also need to consider which quantum programming languages or frameworks should be used. 
To a large extent this selection may be guided by the protocols themselves, as the different languages we have examined are suited for some uses over others. D-Wave provides 
annealing quantum computers, while IBM provides gate-based quantum computers, and Xanadu provides photonic quantum computers. Each of these has its own strengths and weaknesses,and requires a different programming language to operate. As we consider the implementation of protocols further, we are likely to discover that some are simply not possible for us to implement currently, and others require implementation on a specific type of quantum hardware.

## Ongoing Risks
(address your project risks identified from Milestone 1 and update them based on your current progress, this should be a table)  

In the second milestone, the risks we have encountered are mostly remaining the same as we have in the milestone one. In general, our team has identified the following risks to the successful completion of this project:

|Risk name (value)  | Impact     | Likelihood | Description |
|-------------------|------------|------------|-------------|
| Team Unavailability (73) | 8 | 9 | Members of the joint UNO and sponsor team are highly likely to become unavailable for planned and unplanned reasons during the course of this project. Type of impact will vary but, due to small team size, the magnitude of impact could be significant and will require increased coordination to mitigate. |
| Inexperience with Topic Domain (50) | 5 | 10 | As the team has already seen, the domain of this problem naturally presents issues in its density and breadth. Focused project scope and research discipline are necessary to avoid cycles wasted on work that does not contribute to the project goals. |
| Infrastructure and Technology Incompatibility (30) | 5 | 6 | The availability and capabilities of the infrastructure and technologies employed for our prototype deliverable could limit our ability to realize an ideal solution. Due in part to time contraints and available resources, the team may not identify the tools and technologies that are most likely to deliver optimal results. Enumerating available technologies, including their application and capabilites, will ensure that the team can pivot to appropriate alternates as necessary. |
| State of the Art Immaturity (25) | 5 | 5 | Because the goal to deliver a proof-of-concept that demonstrates real-world application of quantum schemes that ensure integrity, message authentication, and non-repudiation is highly dependent on the state of the art, any shortcomings of existing protocols will hinder the team's ability to realize a "complete" solution. As the team members are not experts in this field, and therefore unlikely to contribute truly novel solutions through research, it may need to consider re-scoping the requirements of its POC. |
| Ineffective Assessment (15) | 3 | 5 | Criteria by which the team's POC is assessed must be carefully selected and defined to ensure effective measurement of its performance and real-world viability. Criteria derived from existing studies may prove to be ineffective due to the scope or domain in which they were originally applied. The team should carefully consider criteria from a variety of existing studies - both quantum and classical - to ensure the capabilities of the POC are properly measured and accurately reported. |
| Lack of Experiment Tool (30) | 5 | 6 | Our team is needed to experiment multiple different QKD protocols, and all the QKD protocols have its own required equipments and processing environment, so it is impossible to measure the accurate result without using concrete tools in the lab examination. As a result, the team needs to pay attention on doing tests on virtual quantum simulation tool that has been developed by mature company like IBM Quantum Experience. |


#### Grading Criteria
Your team will be graded as follows:

| | Meets expectations (33-40) | Some Issues (25-32) | Does not meet expectations (0-24)|
|---|---|---|---|
| Effort and progress | It is clear that the team has made non-trivial effort and progress towards project realization.| There is some evidence of effort and progress, but more could have been done in the time. | Little effort or progress was made.|
| Documentation | Code artifacts and tasks are documented well. Documentation is clear and illustrative. | Some code is documented, but large portions are not. | Little or no documentation.|
| Demonstrable Outcomes | The outcomes are successfully demoed for Dr. Hale. The team addresses and handles questions well. | The demo partially works, but there are some significant issues. | Many significant issues with artifacts (e.g. code, documents, etc).|


**Total 120 points.**

## Research Paper Outline  - Draft your Research Paper
You should focus, as part of this milestone, on drafting an outline of your research paper. The emphasis of this process is to prepare an outline early enough in the semester to work with Dr. Hale to refine it into your eventual paper. Even though you may not know all of your results and findings yet, you should be able to draft the skeleton of the paper and start drafting sections of the paper such as your literature review and methodology.

### Submission materials
Submit a draft document containing your outline on canvas using the milestone 2 project assignment. The outline can be in any document format, but .docx is preferable. 

### Grading Criteria
Your outline will not be graded using a rubric, but it is expected to meet the following requirements. 

1. Contains a well-written 500 word or less abstract that previews the argument to be made in the paper.
1. Has defined section headings for each of the sections you expect to have in your paper
1. Has a bulleted list of talking points you expect to fall within each section
1. Section headings and bullets build a narrative flow that is compatibile with your main research argument.

**Total: 80 points**

## Diagrams - Encapsulate your efforts diagrammatically (For now, just using Lucidchart) 
In addition to the project documentation, you should produce a set of process or conceptual diagrams suited to your project. This could be a set of activity diagrams for penetration-testing oriented projects, it could be software architecture diagrams for development-oriented projects, or it could be a process/conceptual model for other projects.

For more information about different types of diagrams, see:

Activity diagrams:
* [http://www.agilemodeling.com/artifacts/activityDiagram.htm](http://www.agilemodeling.com/artifacts/activityDiagram.htm)
* [http://www.uml-diagrams.org/activity-diagrams.html](http://www.uml-diagrams.org/activity-diagrams.html)

Process Diagrams:
* [http://asq.org/learn-about-quality/process-analysis-tools/overview/flowchart.html](http://asq.org/learn-about-quality/process-analysis-tools/overview/flowchart.html)
* [https://www.rds-london.nihr.ac.uk/RDSLondon/media/RDSContent/files/Research-process-flow-chart_A4_web.pdf](https://www.rds-london.nihr.ac.uk/RDSLondon/media/RDSContent/files/Research-process-flow-chart_A4_web.pdf)

Conceptual Model:
* [https://airbrake.io/blog/sdlc/conceptual-model](https://airbrake.io/blog/sdlc/conceptual-model)
* [http://boxesandarrows.com/conceptual-models-in-a-nutshell/](http://boxesandarrows.com/conceptual-models-in-a-nutshell/)

### Submission materials
You should create your diagrams using an architectural tool such as Lucidchart, MS Visio, or similar tools. You should include the diagrams in your main project README.md file and in your Progress report in your GitHub repo, as images and (where appropriate) include links to Lucidchart/other platforms.

### Grading Criteria
You should produce diagrams relevant to your project. Diagrams will be graded as follows:

| | Meets expectations (27-30) | Some Issues (16-26) | Does not meet expectations (0-15)|
|---|---|---|---|
| Relevant | The diagrams are useful for conveying project details. | There are some issues that prevent the diagrams from contributing to understanding | The diagrams are tangential or not present. |
| Descriptive | The diagrams clarify the interoperation or operation of a feature of interest. They provides descriptive clarity. | The diagrams provides limited descriptive clarity. | The diagrams do not help the viewer understand the project. |

**Total 60 points.**


## Issue Tracking and Planning  - Stay organized with approrpriate tracking of tasks
You should continue to document tasking related to your project following milestone 1. Use the issue tracker and/or Kanban board features in your GitHub repo to track your progress. I hope to see a sufficient number, specificity, and allocation of tasks to each person. 

### Graditing criteria
This category will be graded as follows:

| | Meets expectations (16-20) | Some Issues (11-15) | Does not meet expectations (0-10)|
|---|---|---|---|
| Coverage | Sufficient tasks commensurate with the duration of the milestone are defined. Each task is specific and relevant to the project. Forward progress is made on most tasks. | There are too few tasks and/or many tasks are not very specific or relevant to your project. | There are too few or no tasks. Most tasks are not specific or relevant to the project and/or there is little-to-no progress evident. |
| Allocation and status | Issues are all marked with a status tag or cards are placed in the appropriate column in the kanban. Each is in the backlog, finished and in the 'done' category, or allocated to someone for handling as part of the current sprint. | Some issues are marked up accordingly, but not all. | Many issues have not been appropriately updated. Status tags are clearly out of date or cards are not placed in appropriate columns. |


### Submission materials
This part of the milestone is strictly captured by your Kanban board and/our issue tracker. 

### Grading Criteria
**Total 40 points.**

## Presentation - Present your progress to the class
You will be expected to present your Milestone 2 achievements to the class following the deadline. It is important that you use this time to both inform your classmates of your activities and to practice for your final presentation. Things to be considered are 1) conveying a sense of interest and excitement about your project 2) cool product demos, and 3) interesting findings of conducting your projects.

### Submission Materials
Submit your slides to Dr. Hale by the presentation days. Submit them by posting and pinning them in your team slack channel and via canvas.

### Grading Criteria
You will be graded by a presentation rubric.

**Total 60 points.**

#### License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">CYBER4580 and related works</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://faculty.ist.unomaha.edu/mlhale" property="cc:attributionName" rel="cc:attributionURL">Matt Hale</a> are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
