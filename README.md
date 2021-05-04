# Quantum Communications and Cryptography
This repository documents our group's Master of Science in Cybersecurity capstone project, which was undertaken at the University of Nebraska, Omaha, in Spring of 2021. Team members were Henry McNeil, Zexi Xing, Casey Schmitz, and Bryan Tomey.

## Executive Summary
Quantum computers have the world on the brink of a second computing revolution. By using the unique properties of subatomic particles, they will be able to solve complex problems in minutes which would take a classical computer thousands of years. Foremost among these problems are many which are foundational to modern cryptography, such as the prime factorization problem at the core of internet security. While current quantum computers do not have the level of sophistication necessary to break today's encryption systems, it is only a matter of time before they gain that capability. We are undertaking this project to explore the implications of quantum computing on cryptography in order to stay ahead of this anticipated threat and preserve the security of sensitive communications as used for everything from internet browsing to military instructions.

In highly critical communications systems, such as those used to initiate a military action, messages must have guaranteed delivery, must not be tampered with, and must be authenticated and correct. These systems must not allow for false messages, as these could lead to widespread loss of life in the worst case, so non-repudiation is a primary concern. Our goal in this project is to identify the best ways for a critical system to send confidential messages with a guarantee of integrity and non-repudiation in a world where quantum computers are prevalent and capable. These cryptographic mechanisms may include quantum key distribution, quantum digital signatures, and quantum-resistant encryption algorithms performed on a classical computer.

## Project Goals - TODO update
1. Research the impacts of quantum computing on the security of today's commonly used cryptographic protocols, such as AES, RSA, and SHA-256, to determine which are still capable of serving their intended purpose and which must be replaced by quantum or post-quantum solutions.
2. Evaluate the current state of quantum cryptography, including key distribution, encryption, hashing, and digital signatures, to identify the most promising protocols with regards to confidentiality, integrity, and non-repudiation.
3. Assess the viability of the most promising protocols for use in a real world scenario against sophisticated adversaries in which authenticated and correct messaging is of the utmost importance, implementing proof of concept versions of protocols where feasible.
4. Provide a set of recommendations regarding secure communications in a post-quantum world.

## Project Methodology
TODO - update (specific methodology followed in the project, reuse from milestone 1/2, update if scope changed)
### Initial Literature Review
The initial literature review conducted by our team was broad in scope and contains a significant amount of important background material, as well as works relating to the topics of key distribution, confidentiality, integrity, and non-repudiation. Several valuable papers concerning studies similar to ours were also included, as we believe they will provide valuable guidance as we continue this project.

Our [initial literature review is available here](LiteratureReview.md)

### Initial Technical Plan

Our [initial technical plan is available here](TechnicalPlan.md)

## Results / Findings
(brief overview of outcomes - what did you achieve?, list milestone 1/2/3 outcomes, make an effort to logically collect and organize the findings)

(bulleted lists can also be helpful to structure your results discussion)
* outcome 1
* outcome 2

## Install Instructions
During the course of this research, we produced implementations of BB84, Amerimehr and Dehkordi's 2018 symmetric quantum cryptosystem, and Kak's Three-Stage Protocol.

### Requirements
(list of any software / hardware requirements necessary to run the code/app/etc)

### Installation Instructions
(list of steps to install the product/app/code/etc)

### Getting started
(list of any steps to run the code after installation and/or manage the apps over their lifecycle)

## Presentations
Our team's [initial project presentation can be viewed here](https://use.vg/DffurR)

Our [second project presentation can be viewed here](https://use.vg/xZB3Gb)
