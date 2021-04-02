# Progress Report (April 2, 2021)
## Overview
Over the last several weeks, the team has continued our work on the research paper and completed a prototype implementation of the BB84 protocol for quantum key distribution, as well as initial work on the protocol described in Amerimehr and Dekordi's 2018 paper "Quantum Symmetric Cryptosystem Based on Algebraic Codes". We have been heavily focused on ensuring we have a comprehensive set of sources for use in our research, including representative samples of quantum cryptographic protocols that apply to confidentiality, integrity, and non-repudiation.

Additionally, we will put effort on concluding some concrete results with respect to Quantum Key Distribution Protocols (QKDP) that can help our client understands both advantages and disadvantages of currently existing QKDP and those basic procedures need to be executed during the communication. Hence, we did a widely research on quantum cryptographic algorithms, and we find most contemporary QKDPs are not possible to achieve because of the signal transmission channel losses, lack of ideal single photonic light source, and low detection efficiency of receiver etc. As a result, our goal is to seek out a QKDP that can be easy to implement with modern technological equipment and infrastructure, and it can also provide fairly sufficient security and transmission rate.

## Outcomes
During this period, the team accomplished several fundamental steps toward the eventual realization of this project, including initial development environment setup for all team members, progress on the paper outline, and additional research on quantum cryptographic protocols. In summary, we:
* Completed [environment setup guide for OS X/Windows/*nix](EnvironmentSetup.md)
* Completed [sample BB84 implementation](Resources/BB84-demo.ipynb)
* Began work on a [practical full quantum cryptosystem implementation](AD2018-demo.ipynb)
* Initial [outline of final paper](Resources/outline.docx)
* Refined literature review and identified new sources
* Defined classification criteria for algorithms
* Completed [QKD protocol comparison](QKD%20Protocols.md)

## Hinderances
Our team encountered several challenges during this period. We had several team members with significantly reduced availability due to professional obligations, which delayed our progress on the second milestone to some extent. We also encountered several major differences between operating systems when trying to configure our environments for prototyping, as Windows requires several undocumented dependencies to be installed in order for Anaconda and Jupyter Lab to work properly. We also found that while it was easy to follow a simple tutorial to implement BB84, it is significantly more challenging to translate a theoretical algorithm in a research paper into a practical implementation. As this is the core of our research project, however, this hinderance is to be expected and indicates that the problem is non-trivial. Surprisingly, the challenges which arose were not directly related to the quantum portion of the algorithm, but the surrounding portions of the process involving error correcting codes and their realization in Python.

## Ongoing Risks
In the second milestone, the risks we have encountered are mostly remaining the same as we have in the milestone one. In general, our team has identified the following risks to the successful completion of this project:
|Risk name (value)  | Impact     | Likelihood | Updated Status |
|-------------------|------------|------------|-------------|
| Team Unavailability (73) | 8 | 9 | Team unavailability has had a medium impact on progress to date and continues to be a concern due to various professional obligations. |
| Inexperience with Topic Domain (32) | ~~5~~ 4 | ~~10~~ 8 | The team has managed this risk well and worked hard to increase our knowledge of the domain. While it remains a risk as we move into more advanced areas of the project, the impact and likelihood have been reduced. |
| Infrastructure and Technology Incompatibility (30) | 5 | 6 | No change in status. |
| Lack of Experiment Tool (30) | 5 | 6 | Our team is needed to experiment multiple different QKD protocols, and all the QKD protocols have its own required equipments and processing environment, so it is impossible to measure the accurate result without using concrete tools in the lab examination. As a result, the team needs to pay attention on doing tests on virtual quantum simulation tool that has been developed by mature company like IBM Quantum Experience. |
| State of the Art Immaturity (25) | 5 | ~~5~~ 3 | As the team has continued our research, we have found that a sufficient body of work exists to conduct meaningful research in this area. Due to our change in scope to focus on providing a template by which quantum cryptographic protocols can be implemented, we have reduced the likelihood of this risk affecting the project. |
| Ineffective Assessment (15) | 3 | 5 | The team has continued to take steps to mitigate this risk by brainstorming evaluation criteria and seeking evaluations of our proposals. |
