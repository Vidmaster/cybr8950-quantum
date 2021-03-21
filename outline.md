# Paper Outline
- Contains a well-written 500 word or less abstract that previews the argument to be made in the paper.
- Has defined section headings for each of the sections you expect to have in your paper
- Has a bulleted list of talking points you expect to fall within each section
- Section headings and bullets build a narrative flow that is compatible with your main research argument.

0. Abstract
    1. 500 word or less abstract here
1. Introduction
    1. General Introduction
    2. Background
    3. Motivation
    4. Related topics which are out of scope
2. Related Work
    1. Expect this section to focus more on background and foundational papers in the different areas of quantum cryptography like the original BB84 paper
    2. Attacks against quantum cryptography techniques
    3. Include research methodology background for similar studies comparing different cryptographic algorithms
    4. Any interesting cryptographic techniques that aren't suitable for inclusion in our methodology
    5. Post-quantum cryptography
3. Methodology
    1. Selection of algorithms
        1. QKD
        2. Confidentiality
        3. Integrity
        4. Non-Repudiation
    2. Classification
        1. Each scheme to be evaluated according to its intended function. Some may appear in multiple sections if they provide multiple attributes e.g. both confidentiality and integrity
        2. Explanation of criteria and why each was selected
    3. Evaluation
        1. Implementation
        2. Applicability to hypothetical use case
        3. Possible attacks
4. Analysis
    1. Present selected algorithms
    2. Show classification
    3. Sample implementation of an algorithm
    4. Formula for implementation of quantum algorithms
        1. How to identify an algorithm and turn it into a prototype implementation using Qiskit or similar
        2. Limitations of this approach - what it works for, what it doesn't work for
        3. Here’s a workflow that someone could follow to take a mathematical implementation from a research paper and turn it into an implementation using Qiskit or another framework.
        4. Here’s an example we did following these steps, here are the challenges we encountered, insight into how to translate other frameworks besides Qiskit
5. Conclusion
    1. General conclusions
    2. Future research
