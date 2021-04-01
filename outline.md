# Paper Outline
- Contains a well-written 500 word or less abstract that previews the argument to be made in the paper.
- Has defined section headings for each of the sections you expect to have in your paper
- Has a bulleted list of talking points you expect to fall within each section
- Section headings and bullets build a narrative flow that is compatible with your main research argument.

0. Abstract
    1. 500 word or less abstract here
1. Introduction
    1. General Introduction
    2. Background & Problem Context
    3. Motivation
        1. Gaps that currently exist, how the literature has evolved over time, what we're actually talking about in this paper
        2. Related topics which are out of scope of this paper
    4. Research Questions
        1. **Research Question 1:** What are the impacts of quantum computing on today's commonly used cryptographic protocols for hashing, symmetric, and asymmetric encryption? Which of these protocols or classes of protocols need to be replaced by quantum or post-quantum solutions?
        2. **RQ2:** What are the most promising techniques, either quantum or a hybrid of classical and quantum techniques, for maintaining the confidentiality of data at rest and in motion?
        3. **RQ3:** What are ..., for verifying the integrity of data received?
        4. **RQ4:** What are ..., for ensuring the authenticity and non-repudiation of messages?
        5. **RQ5:** What standard process can be followed to translate a theoretical quantum algorithm into an implementation suitable for hands-on testing?
2. Related Work
    0. Basically recycling our literature review and chunking out into categories - port over, categorize, and refine
    1. Impacts of quantum computing on classical cryptography - Answers RQ1
        1. Shor's algorithm impact on RSA and digital signatures
        2. Grover's impact on AES and symmetric algorithms
        3. Impact on hashing functions and authenticated encryption
    2. Foundational papers in the different areas of quantum cryptography (like the original BB84 paper etc)
    3. Attacks against quantum cryptography techniques
        1. Photon splitting attacks
        2. Denial of service
        3. Man in the middle
        4. Any others uncovered in final literature review
    4. Include research methodology background for similar studies comparing different cryptographic algorithms
        1. Found two different papers which fall into this category, can discuss here (Jorstad and Khan)
    5. Post-quantum cryptography
        1. NIST competition
        2. Promising algorithms must not fall into BQP class (Bounded-error Quantum Polynomial)
3. Methodology
    1. Overview of methodology as described in technical plan
        1. How algorithms were selected
        2. How algorithms were classified
            1. Different classification scheme was used for each intended function
            2. Algorithms may appear in multiple categories if they provide multiple attributes e.g. both confidentiality and integrity
            3. Explanation of criteria and why each was selected - TODO for team: Fill these in
                1. QKD criteria -
                2. Confidentiality criteria -
                3. Integrity criteria -
                4. Non-Repudiation criteria -
        3. How algorithms were evaluated as implementation candidates
            1. Level of overall complexity
            2. Practical applicability to research questions
    2. Selection of algorithms
        1. QKD - https://github.com/Vidmaster/cybr8950-quantum/blob/main/QKD%20Protocols.md
        2. Confidentiality
        3. Integrity
        4. Non-Repudiation
    3. Classification
        1. Envisioning this section as basically just being several tables accompanied by discussion
    4. Evaluation
        1. Implementation
        2. Applicability to hypothetical use case
        3. Ways to evaluate against possible attacks (if we get that far)
    5. Revisit research questions and relevance to the methodology. If RQs overlap, can keep this structure, otherwise consider having a top level for each RQ and then go from there. Which part of our methodology addresses each question?
4. Analysis & Results
    1. Sample implementation of a selected algorithm
        1. Challenges encountered during implementation
        2. Limitations of our implementation
        3. How this implementation could be used in practice
    2. General formula for implementation of quantum algorithms - Answers RQ5
        1. How to identify an algorithm and turn it into a prototype implementation using Qiskit or similar
        2. Limitations of this approach - what it works for, what it doesn't work for
        3. Here’s a workflow that someone could follow to take a mathematical implementation from a research paper and turn it into an implementation using Qiskit or another framework.
        4. Here’s an example we did following these steps, here are the challenges we encountered, insight into how to translate other frameworks besides Qiskit
    3. Tie back to research questions - what's our answer, and how did we get there?
        1. RQ2 - Confidentiality
        2. RQ3 - Integrity
        3. RQ4 - Non-Repudiation
5. Conclusion
    1. General conclusions
    2. Future research

Think of structuring paper in terms of a chain of evidence/argument in support of our questions
Add some bullet points of notes on what we plan to discuss in the section if it's not 100% obvious
