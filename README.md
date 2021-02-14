# Quantum Communications and Cryptography
## Executive Summary
Quantum computers have the world on the brink of a second computing revolution. By using the unique properties of subatomic particles, they will be able to solve complex problems in minutes which would take a classical computer thousands of years. Foremost among these problems are many which are foundational to modern cryptography, such as the prime factorization problem at the core of internet security. While current quantum computers do not have the level of sophistication necessary to break today's encryption systems, it is only a matter of time before they gain that capability. We are undertaking this project to explore the implications of quantum computing on cryptography in order to stay ahead of this anticipated threat and preserve the security of sensitive communications as used for everything from internet browsing to military instructions.

In highly critical communications systems, such as those used to initiate a military action, messages must have guaranteed delivery, must not be tampered with, and must be authenticated and correct. These systems must not allow for false messages, as these could lead to widespread loss of life in the worst case, so non-repudiation is a primary concern. Our goal in this project is to identify the best ways for a critical system to send confidential messages with a guarantee of integrity and non-repudiation in a world where quantum computers are prevalent and capable. These cryptographic mechanisms may include quantum key distribution, quantum digital signatures, and quantum-resistant encryption algorithms performed on a classical computer.

## Project Goals
1. Research the impacts of quantum computing on the security of today's commonly used cryptographic protocols, such as AES, RSA, and SHA-256, to determine which are still capable of serving their intended purpose and which must be replaced by quantum or post-quantum solutions.
2. Evaluate the current state of quantum cryptography, including key distribution, encryption, hashing, and digital signatures, to identify the most promising protocols with regards to confidentiality, integrity, and non-repudiation.
3. Assess the viability of the most promising protocols for use in a real world scenario against sophisticated adversaries in which authenticated and correct messaging is of the utmost importance, implementing proof of concept versions of protocols where feasible.
4. Provide a set of recommendations regarding secure communications in a post-quantum world.

## Project Merit
Encryption is omnipresent in modern life, with uses ranging from internet browsing to medical devices, wireless car keys to nuclear control systems. Quantum computing threatens almost all current encryption protocols in one way or another, whether by effectively weakening key strength, or breaking the algorithm entirely. As such, an understanding of the significance of quantum computing and new cryptographic protocols is critical, with impacts in areas ranging from personal privacy to national security.


# Timeline
**For a more complete Timeline view, please check [Quantum Communications Timeline](https://unomaha675546.monday.com/boards/1010619675/).**

### Gantt Chart view
![Gantt Chart of Quantum Computation Key Distribution Project](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/Gantt%20view%20of%20Milestone%201.PNG)


### Timeline View
![Overview of Quantum Computation Key Distribution Project](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/Milestone%201%20timeline.PNG)

### Task Card of GitHub Project Board

The team's progress and individual tasks are tracked through a GitHub Project Board [which can be viewed at this link](https://github.com/Vidmaster/cybr8950-quantum/projects/1).


# Risks
Our team has identified the following risks to the successful completion of this project:

|Risk name (value)  | Impact     | Likelihood | Description |
|-------------------|------------|------------|-------------|
| Team Unavailability (73) | 8 | 9 | Members of the joint UNO and sponsor team are highly likely to become unavailable for planned and unplanned reasons during the course of this project. Type of impact will vary but, due to small team size, the magnitude of impact could be significant and will require increased coordination to mitigate. |
| Inexperience with Topic Domain (50) | 5 | 10 | As the team has already seen, the domain of this problem naturally presents issues in its density and breadth. Focused project scope and research discipline are necessary to avoid cycles wasted on work that does not contribute to the project goals. |
| Infrastructure and Technology Incompatibility (30) | 5 | 6 | The availability and capabilities of the infrastructure and technologies employed for our prototype deliverable could limit our ability to realize an ideal solution. Due in part to time contraints and available resources, the team may not identify the tools and technologies that are most likely to deliver optimal results. Enumerating available technologies, including their application and capabilites, will ensure that the team can pivot to appropriate alternates as necessary. |
| State of the Art Immaturity (25) | 5 | 5 | Because the goal to deliver a proof-of-concept that demonstrates real-world application of quantum schemes that ensure integrity, message authentication, and non-repudiation is highly dependent on the state of the art, any shortcomings of existing protocols will hinder the team's ability to realize a "complete" solution. As the team members are not experts in this field, and therefore unlikely to contribute truly novel solutions through research, it may need to consider re-scoping the requirements of its POC. |
| Ineffective Assessment (15) | 3 | 5 | Criteria by which the team's POC is assessed must be carefully selected and defined to ensure effective measurement of its performance and real-world viability. Criteria derived from existing studies may prove to be ineffective due to the scope or domain in which they were originally applied. The team should carefully consider criteria from a variety of existing studies - both quantum and classical - to ensure the capabilities of the POC are properly measured and accurately reported. |

# Methodology
## Initial Literature Review
Briefly discuss research question, methodology, and keywords used once complete.

Our [initial literature review is available here](LiteratureReview.md)

## Initial Technical Plan
Details of technical plan or a link if it's too long.

Our [initial technical plan is available here](TechnicalPlan.md)

# Resources Needed
We have identified the following resources as necessary for the successful completion of this project:

|Resource  | Dr. Hale needed? | Investigating Team member | Description |
|-------------------|---------|---------------------------|-------------|
|Qiskit| No | Bryan | A quantum computing open source framework that uses a python interface.  |
|e.g. PLC unit | Yes | Casey | A programmable logic controller from Siemens for investigation.|
|Qiskit | No | Henry | A quantum computing open source framework that uses a python interface.|
|Gantt | No | Zexi | A project planning chart. |

# Presentation
Link to slides and video here when available
