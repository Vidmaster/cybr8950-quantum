# Progress Report (May 7, 2021)
## Overview
During this milestone, we refined our research on quantum cryptography, experimented with an implementation of Amerimehr and Dehkordi's 2018 symmetric quantum cryptosystem based on algebraic codes (AD18), and developed a general methodology for the implementation of quantum cryptographic algorithms. Our research on cryptographic techniques has shown us that quantum key distribution has a large number of very promising techniques, both in terms of simulation and experimental realizations over varying distances. Non-Repudiation of quantum data has been well researched, and we identified several protocols which seem simple and robust enough for real world applications. Other areas of quantum cryptography are not as mature, with few protocols addressing confidentiality and integrity of data. A very promising protocol which combines all three desired features of our project stakeholders was AD18, and as such it made an ideal candidate for a prototype implementation.

Our implementation of AD18 revealed that while the cryptosystem had a great deal of promise, it likely would not be feasible for our anticipated use cases due to the large amount of error correcting data required to have a high chance of success in the receipt of a message. As guaranteed delivery was expressed as a high priority by our stakeholders, a "mostly works" protocol will not suffice for their needs. We hope that a greater benefit to our stakeholders has been realized by our creation of a generalized methodology for the implementation of other algorithms, as we believe this will allow for greater experimentation and a more accurate evaluation of existing and newly discovered cryptosystems. Our group has also worked extensively on a final research paper summarizing our work, which we aim to publish in conference proceedings or a journal, and has assembled a set of recommendations for actions organizations can take today and in the future to prepare for the growth of quantum computing.

## Outcomes
This milestone produced several major technical outcomes for our group, including refinement of a [Qiskit-provided BB84 sample](Resources/BB84-demo.ipynb), an implementation of the [AD18 cryptosystem](Resources/AD2018-demo.ipynb), the creation of a standard methodology for implementing other quantum cryptographic algorithms, and an implementation of [Kak's Three-Stage Protocol](Resources/Kak-Three-Stage-demo.ipynb) which was completed as an example following our standard methodology.

The standard methodology for implementing quantum cryptographic algorithms is discussed in greater detail in our research paper, but we will present a summary in this document as well. To create this methodology, we first recognized that most quantum cryptographic algorithms share the same overall structure of preparation, sender processing, transmission, and recipient processing. From there, we were able to propose the following standard set of steps:
* Categorize parts of algorithm by stage and implement stub methods
  * Ex. alice_prepare_message, bob_decrypt_message
* Identify and initialize shared values and configuration
  * Ex. preshared_key = 12345, backend = ‘qasm_simulator’
* Implement simplest possible version of protocol
  * Initialize circuit using identity gates and measurement only, and returning static values from other methods
  * Add comments and debugging statements to assist in implementation and troubleshooting
* Implement classical portion of protocol
  * Including classical encryption, hashing, etc.
* Implement quantum portion of protocol
  * Actual rotation operators, entanglement, etc.

In short, our primary outcomes of this final milestone were:
* Concluded research on quantum cryptography for this project
* Refined implementation of BB84 to produce practical keys
* Implemented and analyzed AD18 cryptosystem
* Implemented Kak's Three-Stage Protocol
* Created a generalized framework for implementation of quantum cryptographic algorithms
* Survived graduate school

## Hinderances
Besides the usual hinderances of challenging subject material and lack of teammate availability, we encountered two new hinderances during this milestone. The first challenge was encountered during our implementation of AD18, where we learned that algebraic error correcting codes are very difficult to understand and implement correctly, as they come in a wide variety of styles and each is suited to a different sort of task. This was fortunately overcome through research, patience, and caffiene. The second challenge was encountered during the writing of the final paper, when we learned that different team members had significantly different visions of the final paper and our goals for it. Fortunately much of the content produced was useful and could be fitted into the final product without a great deal of editing, but we believe we should have spent more time aligning our goals and coming to a shared understanding instead of going off and separately writing sections of what seemed like entirely different papers and struggling to combine them at the end.
