# Project name
## Executive Summary
Quantum computers have the world on the brink of a second computing revolution. By using the unique properties of subatomic particles, they will be able to solve complex problems in minutes which would take a classical computer thousands of years. Foremost among these problems are many which are foundational to modern cryptography, such as the prime factorization problem at the core of internet security. While current quantum computers do not have the level of sophistication necessary to break today's encryption systems, it is only a matter of time before they gain that capability. We are undertaking this project to explore the implications of quantum computing on cryptography in order to stay ahead of this anticipated threat and preserve the security of sensitive communications as used for everything from internet browsing to military instructions.

In highly critical communications systems, such as those used to initiate a military action, messages must have guaranteed delivery, must not be tampered with, and must be authenticated and correct. These systems must not allow for false messages, as these could lead to widespread loss of life in the worst case, so non-repudiation is a primary concern. Our goal in this project is to identify the best ways for a critical system to send confidential messages with a guarantee of integrity and non-repudiation in a world where quantum computers are prevalent and capable. These cryptographic mechanisms may include quantum key distribution, quantum digital signatures, and quantum-resistant encryption algorithms performed on a classical computer.


## Project Goals
1. Research the impacts of quantum computing on the security of today's commonly used cryptographic protocols, such as AES, RSA, and SHA-256, to determine which are still          capable of serving their intended purpose and which must be replaced by quantum or post-quantum solutions.
2. Evaluate the current state of quantum cryptography, including key distribution, encryption, hashing, and digital signatures, to identify the most promising protocols with      regards to confidentiality, integrity, and non-repudiation.
3. Assess the viability of the most promising protocols for use in a real world scenario against sophisticated adversaries in which authenticated and correct messaging is of      the utmost importance, implementing proof of concept versions of protocols where feasible.
4. Provide a set of recommendations regarding secure communications in a post-quantum world.

## Project Methodology

### Technical Plan
The field of quantum cryptography is very broad, with numerous theoretical and practical concerns that will influence the nature and scope of our work on this project. As alluded to by our project goals, we have set out to answer the following research questions:
* **Research Question 1:** What are the impacts of quantum computing on today's commonly used cryptographic protocols for hashing, symmetric, and asymmetric encryption? Which of these protocols or classes of protocols need to be replaced by quantum or post-quantum solutions?
* **RQ2:** What are the most promising techniques, either quantum or a hybrid of classical and quantum techniques, for maintaining the confidentiality of data at rest and in motion?
* **RQ3:** What are ..., for verifying the integrity of data received?
* **RQ4:** What are ..., for ensuring the authenticity and non-repudiation of messages?
The focus of our research will be primarily on quantum cryptography, but we would also be amiss in our duty as researchers if we did not acknowledge that some purely classical algorithms may emerge as the best candidates for use in these areas. To serve as a representative sample of classical post-quantum algorithms, i.e. those which are resistant to all known attacks by quantum computers, we intend to consider different types from the current round of [NIST's post-quantum cryptography initiative](https://csrc.nist.gov/projects/post-quantum-cryptography).

The first steps in answering **RQ1** have largely been completed through the course of our initial literature review. It is well understood that Shor's Algorithm provides a polynomial-time solution to the factorization problem, and can be extended to other problems in the BQP complexity class[[1]](https://cgsr.llnl.gov/content/assets/docs/QuantumComputingandCryptography-20190920.pdf). This algorithm is "able to break many of the public-key cryptosystems currently in use"[[2]](https://csrc.nist.gov/projects/post-quantum-cryptography), breaking RSA, Elliptic Curve Diffie-Hellman, and other protocols in this algorithmic complexity class. This tells us that the currently used asymmetric encryption and digital signatures that underpin internet communications will need to be replaced with new quantum-resistant protocols in order to preserve confidentiality and authenticity of messages. Symmetric algorithms such as AES are weakened by Grover's algorithm, but are not broken by any known quantum algorithms. Work has been done to assess the security of AES against quantum attacks[[3]](https://hal.inria.fr/hal-02397049), but it appears to be quantum-resistant and is likely to provide security for many years to come when a 256-bit key is used. If additional security were needed beyond even that level, an encrypt-decrypt-encrypt style operation similar to 3DES could be used to extend its lifetime to the point that the entire energy content of the universe would need to be expended to brute force even a single key. The security of hashing algorithms, used to provide integrity and authenticity, is currently more threatened by the classical [van Oorschot-Weiner algorithm](http://people.scs.carleton.ca/~paulv/papers/JoC97.pdf) than by known quantum algorithms, though this topic still requires additional research.

To answer **RQ2-4** we intend to take a multi-step approach consisting of identification, classification, and evaluation of protocols identified through our initial literature review. In greater detail, we envision these steps as follows:
1. **Identification:** Continue to review literature pertaining to proposed schemes for encryption, key distribution, integrity, and non-repudiation and compile a list of proposed protocols in these areas.
2. **Classification:** For each of the schemes identified in step 1, classify it according to its intended function, capabilities, and other known (as opposed to evaluated) properties, with the goal of verifying that we have a representative sample of the state of the art in each of the three areas we are studying and can easily explore other candidates if initial evaluations do not pan out in a given area. While the exact classification criteria have yet to be determined, they may include such items as relationship between signature length and message length, usage of entanglement, reusability of signatures, verification type (blind, arbitrated, etc.), and number of interactions between parties.
3. **Evaluation:** Using the work produced in step 2, conduct an evaluation a subset of protocols on a number of criteria to determine their suitability in real world applications. This step will include proof of concept implementation and testing of representative protocols where possible, assessment against common attacks, and other criteria to be determined as our research continues. In the testing of protocol implementations, we intend to examine such characteristics as performance, ease of eavesdropper detection, size of messages to which the protocol can be applied based on current hardware, and more.

Once the classification and evaluation of various protocols has been completed, we anticipate that we will be able to make a set of recommendations toward confidentiality, integrity, and non-repudiation based on the state of the art in quantum cryptography, as well as demonstrating their usability where implementations are feasible. We believe this research will be valuable, as there are many possible approaches being proposed for quantum cryptography, but very few broad surveys of all these diverse techniques. Through the enumeration, classification, and evaluation of various protocols, we hope to guide both researchers looking to iterate on past work and practitioners looking for ways to begin implementing quantum cryptography.

### Technical Implememntation

1. At the beginning, to satisfy out client goal, we need to explore several different QKD protocols to decide which existing QKD protocol is achieveable and implementable with    respect to modern quantum communication. Hence, we put effort on concluding some concrete results with respect to Quantum Key Distribution Protocols (QKDP) that can help our    client understands both advantages and disadvantages of currently existing QKDP and those basic procedures need to be executed during the communication. To accomplish that,    we did a widely research on quantum cryptographic algorithms, and we find most contemporary QKDPs are not possible to achieve because of the signal transmission channel        losses, lack of ideal single photonic light source, and low detection efficiency of receiver etc. Finally, after comparing couple QKDP, we find BB84 is an appropriate QKD      protocol to focus on, since it can be implemented with modern technological equipment and infrastructure, and it can also provide fairly sufficient security and transmission    rate. Here is the list that we did the [comparsion for QKD protocols along with some visual illustration.](QKD%20Protocols.md) 

2. We are mainly explored the BB84 QKD protocol and generated some reasonable consequence. The first sample demo can be access through [sample BB84 implementation](Resources/BB84-demo.ipynb)
3. After we have analyzed basic BB84 simulation, we would like to pursue on achieveing [practical full quantum cryptosystem implementation](Resources/AD2018-demo.ipynb)

## Results / Findings

During this period, the team accomplished several fundamental steps toward the eventual realization of this project, including initial development environment setup for all team members, progress on the paper outline, and additional research on quantum cryptographic protocols. In summary, we:
* Completed [environment setup guide for OS X/Windows/*nix](EnvironmentSetup.md)
* Completed [sample BB84 implementation](Resources/BB84-demo.ipynb)
* Began work on a [practical full quantum cryptosystem implementation](Resources/AD2018-demo.ipynb)
* Initial [outline of final paper](Resources/outline.docx)
* Refined literature review and identified new sources
* Defined classification criteria for algorithms
* Completed [QKD protocol comparison](QKD%20Protocols.md)
* Created/located [diagrams and other visual aids for use in final paper](Diagrams.md)

## Install Instructions (if applicable)


### Requirements
(list of any software / hardware requirements necessary to run the code/app/etc)
Qiskit,IBM Quantum Experience, Jupyter Lab, Python >=3, Anaconda or Miniconda, Windows/Linux/MAC OS, Visual C++ build tools. 

### Installation Instructions
(list of steps to install the product/app/code/etc)
* The [environment configuration guide for OS X/Windows/*nix](EnvironmentSetup.md)

### Getting started
(list of any steps to run the code after installation and/or manage the apps over their lifecycle)
