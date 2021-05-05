# Quantum Communications and Cryptography
This repository documents our group's Master of Science in Cybersecurity capstone project, which was undertaken at the University of Nebraska, Omaha, in Spring of 2021. Team members were Henry McNeil, Zexi Xing, Casey Schmitz, and Bryan Tomey.

## Executive Summary
Quantum computers have the world on the brink of a second computing revolution. By using the unique properties of subatomic particles, they will be able to solve complex problems in minutes which would take a classical computer thousands of years. Foremost among these problems are many which are foundational to modern cryptography, such as the prime factorization problem at the core of internet security. While current quantum computers do not have the level of sophistication necessary to break today's encryption systems, it is only a matter of time before they gain that capability. We are undertaking this project to explore the implications of quantum computing on cryptography in order to stay ahead of this anticipated threat and preserve the security of sensitive communications as used for everything from internet browsing to military instructions.

In highly critical communications systems, such as those used to initiate a military action, messages must have guaranteed delivery, must not be tampered with, and must be authenticated and correct. These systems must not allow for false messages, as these could lead to widespread loss of life in the worst case, so non-repudiation is a primary concern. Our goal in this project is to identify the best ways for a critical system to send confidential messages with a guarantee of integrity and non-repudiation in a world where quantum computers are prevalent and capable. These cryptographic mechanisms may include quantum key distribution, quantum digital signatures, and quantum-resistant encryption algorithms performed on a classical computer.

## Project Goals
The goals of this project were as follows:
1. Research the impacts of quantum computing on the security of today's commonly used cryptographic protocols, such as AES, RSA, and SHA-256, to determine which are still capable of serving their intended purpose and which must be replaced by quantum or post-quantum solutions.
2. Evaluate the current state of quantum cryptography, including key distribution, encryption, hashing, and digital signatures, to identify the most promising protocols with regards to confidentiality, integrity, and non-repudiation.
3. Assess the viability of the most promising protocols for use in a real world scenario against sophisticated adversaries in which authenticated and correct messaging is of the utmost importance by implementing proof of concept versions of one or more protocols.
4. Create a generalized methodology which can be followed by other researchers or engineers to implement other quantum cryptographic algorithms.
5. Provide a set of recommendations regarding secure communications in a post-quantum world.

## Project Methodology
Our approach to this project involved first conducting an extensive literature review to gain an understanding of the state of the art in quantum cryptography, as well as to determine if similar research had been previously conducted. The initial literature review conducted by our team was broad in scope and contains a significant amount of important background material, as well as works relating to the topics of key distribution, confidentiality, integrity, and non-repudiation. Several valuable papers concerning studies similar to ours were also included, as we believed they would provide valuable guidance throughout the course of this project. The focus of our research was primarily on quantum cryptography, but we also briefly examined the leading protocols in the current round of [NIST's post-quantum cryptography initiative](https://csrc.nist.gov/projects/post-quantum-cryptography).

The field of quantum cryptography is very broad, with numerous theoretical and practical concerns that will influence the nature and scope of our work on this project. As alluded to by our project goals, we ultimately set out to answer the following research questions:
* **Research Question 1:** What are the impacts of quantum computing on today's commonly used cryptographic protocols for hashing, symmetric, and asymmetric encryption? Which of these protocols or classes of protocols need to be replaced by quantum or post-quantum solutions?
* **RQ2:** What are the most effective quantum protocols for the creation and distribution of cryptographic secret keys?
* **RQ3:** What are the most promising techniques, either quantum or a hybrid of classical and quantum techniques, for maintaining the confidentiality of data at rest and in motion?
* **RQ4:** What are some reasonable transmission protocols that can be used for verifying the integrity of quantum data?
* **RQ5:** What are the best quantum cryptographic algorithms for ensuring the authenticity and non-repudiation of messages?
* **RQ6:** Can a standard process be followed to translate a theoretical quantum algorithm into an implementation suitable for hands-on testing?

The steps to answer **RQ1** were largely been completed through our initial literature review. It is well understood that Shor's Algorithm provides a polynomial-time solution to the factorization problem, and can be extended to other problems in the [BQP complexity class](https://cgsr.llnl.gov/content/assets/docs/QuantumComputingandCryptography-20190920.pdf). This algorithm is ["able to break many of the public-key cryptosystems currently in use"](https://csrc.nist.gov/projects/post-quantum-cryptography), breaking RSA, Elliptic Curve Diffie-Hellman, and other protocols in this algorithmic complexity class. This tells us that the currently used asymmetric encryption and digital signatures that underpin internet communications will need to be replaced with new quantum-resistant protocols in order to preserve confidentiality and authenticity of messages. Symmetric algorithms such as AES are weakened by Grover's algorithm, but are not broken by any known quantum algorithms. Work has been done to assess the [security of AES against quantum attacks](https://hal.inria.fr/hal-02397049), but it appears to be quantum-resistant and is likely to provide security for many years to come when a 256-bit key is used. If additional security were needed beyond even that level, an encrypt-decrypt-encrypt style operation similar to 3DES could be used to extend its lifetime to the point that the entire energy content of the universe would need to be expended to brute force even a single key. The security of hashing algorithms, used to provide integrity and authenticity, is currently more threatened by the classical [van Oorschot-Weiner algorithm](http://people.scs.carleton.ca/~paulv/papers/JoC97.pdf) than by known quantum algorithms, though this topic still requires additional research.

To answer **RQ2-5** we took a multi-step approach consisting of identification, classification, and evaluation of the protocols identified through our initial literature review and subsequent research. In greater detail, these steps were as follows:
1. **Identification:** Conducted an extensive review of literature pertaining to proposed schemes for encryption, key distribution, integrity, and non-repudiation and compiled a list of proposed protocols in these areas.
2. **Classification:** For a representative sample of the schemes identified in step 1, we classified them according to  intended function, capabilities, and other known (as opposed to evaluated) properties. The classification criteria used included such items as relationship between signature length and message length, key reuse, usage of entanglement, reusability of signatures, verification type (blind, arbitrated, etc.), and number of interactions between parties.
3. **Evaluation:** Using the work produced in step 2, we conducted an evaluation of a subset of protocols by implementing them in Qiskit in an attempt to determine their suitability in real world applications. The evaluation included BB84, AD18, and Kak's Three-Stage Protocol. To answer **RQ6**, this process led us to create a generalized methodology that can be followed to assist in the implementation of other quantum cryptographic algorithms, which is described in more detail below.

## Results / Findings
Over the course of this semester, we conducted a substantial amount of research on all aspects of quantum cryptography, and produced the following deliverables and findings:
* Produced three presentations summarizing our research throughout the semester
  * [First project presentation](https://use.vg/DffurR)
  * [Second project presentation](https://use.vg/xZB3Gb)
  * [Third project presentation](https://use.vg/pG8QQa)
* Produced a research paper and the following related artefacts
  * [Initial literature review](LiteratureReview.md)
  * [Final bibliography containing all sources examined](https://zbib.org/6b5ca46ffd954a329309469cc1f536a4)
  * [Initial technical plan](TechnicalPlan.md)
  * [Outline of final paper](Resources/outline.docx)
  * [QKD protocol comparison](QKD%20Protocols.md)
  * [Diagrams and other visual aids](Diagrams.md)
  * [Final Research Paper](final-paper.pdf)
* Proposed a generalized framework for implementation of quantum cryptographic algorithms
  * Recognized four common stages in most quantum cryptography protocols
    * Preparation
    * Sender Processing
    * Transmission
    * Recipient Processing
  * Identified five common steps that can be followed for implementations
    * Categorize parts of algorithm by stage and implement stub methods
    * Identify and initialize shared values and configuration
    * Implement simplest possible version of protocol
      * Initialize circuit, identity gates and measurement only, return static values
    * Implement classical portion of protocol (if present)
    * Implement quantum portion of protocol
* Implemented several quantum cryptography protocols and created supporting documentation
  * [Environment setup guide for OS X/Windows/*nix](EnvironmentSetup.md) which should be followed before experimenting with the Jupyter notebooks below
  * [Sample BB84 implementation](Resources/BB84-demo.ipynb)
  * [Amerimehr and Dehkordi's 2018 quantum cryptosystem](Resources/AD2018-demo.ipynb) based on algebraic codes, which is capable of providing confidentiality, integrity, and non-repudiation.
    * We used our BB84 implementation to produce the pre-shared keys used in this system.
  * Implemented [Kak's Three-Stage Protocol](Resources/Kak-Three-Stage-demo.ipynb) by following our implementation methodology.
* Produced a set of recommendations for individuals and organizations on quantum cryptography and the future of quantum computing.
* Survived graduate school

## Recommendations
### Quantum Protocols to Explore Further
As quantum computing and quantum cryptography are still developing fields, none of the algorithms we studied (besides BB84) have received a great deal of scrutiny from cryptographers and security professionals, so we would not recommend replacing classical cryptography with any of these at this time. Of the protocols we investigated, we believe the following protocols and concepts are worth further exploration and are likely to be important to future work:
* Key Distribution
  * Park et al., 2020, ["Research on Plug-and-Play Twin-Field Quantum Key Distribution"](https://doi.org/10.1109/ICTC49870.2020.9289265)
* Confidentiality
  * Pleşa, 2017, ["Hybrid scheme for secure communications using quantum and classical mechanisms"](https://doi.org/10.1109/ECAI.2017.8166458)
  * Amerimehr and Dehkordi, 2018, ["Quantum Symmetric Cryptosystem Based on Algebraic Codes"](https://doi.org/10.1109/LCOMM.2018.2844245)
* Integrity
  * Ben-Sasson et al., 2018, ["Scalable, transparent, and post-quantum secure computational integrity"](https://eprint.iacr.org/2018/046)
* Non-Repudiation
  * Kang et al., 2015, ["Quantum Signature Scheme Using a Single Qubit Rotation Operator"](https://doi.org/10.1007/s10773-014-2254-y)

### Preparing for Quantum Computing Today
Our first recommendation for organizations today is to gain an awareness of quantum computing, what problems it can and cannot be used to solve, and how it threatens current cryptographic systems. Outside of cutting edge security or research concerns, we do not believe it is necessary to immediately hire quantum specialists, but having an awareness of the state of the art in quantum computing will likely provide a competitive advantage to businesses over the next few years. Software engineers and security experts would benefit from learning the basic concepts of quantum computing as well, just as they have been encouraged to do with concepts such as cloud computing and machine learning in the recent past.

As today's most commonly used encryption systems are either weakened or broken by quantum computing, we highly recommend that companies be prepared to implement post-quantum encryption once final candidate algorithms are approved by NIST. Though quantum computers will not be capable of breaking RSA2048 for many years, encrypted data could still be captured by an adversary today and stored until decryption becomes feasible in the future. For data at rest, we recommend using AES with a 256-bit key length, and discontinuing the usage of 3DES and AES with 128- or 192-bit key lengths, as the impact of Grover's algorithm lowers the effective key lengths below those recommended by NIST in Section 3.4 of [Special Publication 800-175B](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-175Br1.pdf).

### Preparing for Quantum Computing in the Future
In the next two decades, we predict that quantum computing will become widespread. Quantum computers will become more capable and easier to access, and an increasing number of companies will hire quantum computing experts. Quantum algorithms will be commonly used for applications such as entropy generation, key distribution, and optimization problems. If dramatic hardware advancements are made, we may even see specialized quantum processing units with a small number of qubits appear in personal computers. To stay ahead of these predictions, we reiterate our previous recommendation that organizations begin building their quantum computing capabilities. We also recommend that organizations be wary of the inevitable wave of charlatan companies that will promise expensive quantum computing offerings which are capable of solving all the world's problems.

As quantum computers become ubiquitous and capable, we predict that large numbers of new algorithms will be discovered. These algorithms will have broad impacts, ranging from threatening the security of previously safe cryptographic protocols, to producing rapid advances in materials science, medicine, and artificial intelligence. The technological and sociopolitical impacts of these new discoveries may alter society as fundamentally as industrialization, automobiles, aviation, and the internet did. Our recommendation is that organizations be prepared to adapt to rapid paradigm shifts in the security and technology landscape.

## Install Instructions
During the course of this research, we produced implementations of BB84, Amerimehr and Dehkordi's 2018 symmetric quantum cryptosystem, and Kak's Three-Stage Protocol. These protocols were implemented in Jupyter Notebooks using Python, Qiskit, and several other supporting libraries.

### Requirements
No special hardware is required to run the jupyter notebooks we created, and they should function on any modern operating system. The simplest way to obtain all of the software required is by installing [Anaconda](https://docs.anaconda.com/anaconda/install/) and following the steps in the [Environment Setup Guide](EnvironmentSetup.md) to configure an environment with the appropriate dependencies. If installing manually, Python 3, Pip, `jupyterlab`, `qiskit`, `scikit-commpy`, `pycryptodome`, and `scipy` will all need to be configured.

### Installation Instructions
To install the code samples we produced, we recommend first following the instructions in our [Environment Setup Guide](EnvironmentSetup.md) using the [environment.yml](Resources/environment.yml) file provided. This will install the appropriate version of Python and other dependencies, as well as Jupyter Lab. The setup guide also provides additional troubleshooting steps and manual installation instructions in more detail.

The protocols we implemented are contained in the following three notebooks, which should be downloaded and saved to the same directory:
* [BB84 implementation](Resources/BB84-demo.ipynb)
  * This implementation was taken from the Qiskit textbook, but was modified slightly here and also appears in a refined version in the below notebook.
* [Amerimehr and Dehkordi's 2018 quantum cryptosystem](Resources/AD2018-demo.ipynb)
* [Kak's Three-Stage Protocol](Resources/Kak-Three-Stage-demo.ipynb)

### Getting started
To run the Jupyter Notebooks above, simply run the command `jupyter-lab` from the command prompt or terminal in the directory where the files were downloaded. Using the Jupyter interface, select the downloaded notebooks from the sidebar, then execute or modify the code appearing in each as desired.
