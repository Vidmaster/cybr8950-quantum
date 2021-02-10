# Quantum Communications and Cryptography Literature Review

### Abstract format - remove me before submission!
1. Problem Statement: What is the primary problem that the study investigated? Why is this an urgent and/or severe problem?
2. Research question(s): What questions related to the problem have not been answered by prior research? Why are practitioners or prior research lacking an understanding of the phenomenon being studied?
3. Contribution: What is the contribution made by this manuscript to a current conversation in the literature? Why are the concept relationships, method, findings, or conclusions surprising or contributing new and important insights?
4. Rationale: How is the paper’s argument addressing the research questions? Why are the claims and propositions warranted?
5. Investigative Approach: What is the approach followed (e.g. field study, experience with a new or existing method, review, empirical, etc.) or what is the paper’s empirical rationale? Why is the method appropriate to develop or test the theoretical claims and propositions?
6. Lessons Learned: What are the primary findings from the study? Why might we expect a substantive impact on practice from the factors analyzed in this study?
7. Implications for practice: What advances in cybersecurity workforce capabilities are implied? Why is the study advancing cybersecurity workforce capabilities?
8. Implications for research: What advances in research are implied or new questions have been raised which future research should investigate? What new investigations are suggested by the findings?

Template:
1. **Citation:** \
**Problem Statement:** \
**Research Question(s):** \
**Contribution:** \
**Rationale:** \
**Investigative Approach:** \
**Lessons Learned:** \
**Implications for Practice:** \
**Implications for Research:**

## Quantum Key Distribution
1. **Abstract:** This is a paper published at 2018 that mainly describes the several QKD protocols structure like BB84, B92, and BBM92 and its usages. At the beginning, this article defines background of each protocol along with visual elaboration. Then, they have done a simulation to examine which protocol above has the most reliable photon exchanging rate. In their simulation, they have compared three results while these three QKD protocols have been eavesdropped by a third party to check how many keys can be received and how many errors can occur during the transmission. \
**Citation:** A. I. Nurhadi and N. R. Syambas, "Quantum Key Distribution (QKD) Protocols: A Survey," 2018 4th International Conference on Wireless and Telematics (ICWT), Nusa Dua, 2018, pp. 1-5, doi: 10.1109/ICWT.2018.8527822.

2. **Abstract:** As we all known, One-Time-Pad is the most secure way to build communication between two network nodes, so the Quantum Key Distribution (QKD) is taking advantage from it to build a much safer network environment called QKDN. However, the key generating rate of current QKDN is in a low speed. As a result, some other studies have explored other conception, which is called Quantum Key Pool (QKP), to mitigate the inefficiency of key production by storing generated keys. To be honest, traditional QKP brings other problems to the QKDN. Likely, the security of QKD will decrease because of the QKP needs to store keys for a while, and the basic performance of QKDN will be harmed. In this case, the author has denoted a conception “Multi-Path Based Quasi-Real-Time QKD” to enhance the security of QKD along with great dynamic response services in QKDN. More specially, the Quasi-real-time QKD could keep the absolutely secure of the quantum key after it has been generated in a dedicated time period, so they proposed the Virtual QKP to store quantum keys in different virtual space which is corresponding to separate secret key path.
**Citation:** X. Liu et al., "Multi-path based Quasi-real-time Quantum Key Distribution in Software Defined Quantum Key Distribution Networks (SD-QKDN)," 2019 18th International Conference on Optical Communications and Networks (ICOCN), Huangshan, China, 2019, pp. 1-3, doi: 10.1109/ICOCN.2019.8934684.

## Quantum Non-Repudiation
1. **Citation:** N. Hematpour, S. Ahadpour, and S. Behnia, “Presence of dynamics of quantum dots in the digital signature using DNA alphabet and chaotic S-box,” Multimed Tools Appl, Nov. 2020, doi: 10.1007/s11042-020-10059-5. [Online]. Available: https://doi.org/10.1007/s11042-020-10059-5. [Accessed: 07-Feb-2021]
\
**Problem Statement:** Digital signatures are an important aspect for verifying the integrity and authenticity of a message, and this study investigates the usage of quantum dots to provide digital signatures.
\
**Research Question(s):** Not explicitly stated, but the authors are attempting to provide an improved way of implementing digital signatures with security against repudiation and forgery, and with a high degree of entropy. This method provides a longer signature with fewer steps and more security than previous implementations.
\
**Contribution:** The authors develop a scheme which uses a dynamic map based on quantum dots, a permutation and substitution scheme similar to AES, and DNA coding to create a quantum digital signature with a high degree of security as long as the signature is of sufficient length. By sending a dynamic quantum system's control parameter and critical points as well as some initial point in phase space, two parties could implement these digital signatures using a quantum computer, but without requiring a quantum channel for transmission.
\
**Rationale:** The authors argue for the security of their system by analyzing the statistical likelihood of an attacker being able to forge the signature or repudiate a message and establish that it decreases exponentially as a function of message length, as well as conducting numerical analysis on their proposed S-box. The security of their dynamic system is based on Lyapunov exponents, which have been discussed in other reviewed works as well.
\
**Investigative Approach:** The authors provide a theoretical implementation of two different versions of this protocol with examples encoding a simple phrase, and compare their security.
\
**Lessons Learned:** The protocol was successfully modeled and analyzed, and found to have a high degree of security based on the mathematical operations used.
\
**Implications for Practice:** This system could be a viable candidate for implementation on a quantum computer on which operators are able to set control parameters and critical points, though might not be suitable for an implementation on a quantum simulator or cloud based quantum computer.
\
**Implications for Research:** It would be worth investigating if there are other encryption systems that can transmit classical values using a non-quantum channel but still obtain the same high level of security given by a quantum system.

2. **Citation:** M.-S. Kang, C.-H. Hong, J. Heo, J.-I. Lim, and H.-J. Yang, “Quantum Signature Scheme Using a Single Qubit Rotation Operator,” Int J Theor Phys, vol. 54, no. 2, pp. 614–629, Feb. 2015, doi: 10.1007/s10773-014-2254-y.
\
**Problem Statement:** Digital signatures are an important aspect for verifying the integrity and authenticity of a message, and this study investigates the signing of quantum messages using a single qubit and rotation operators.
\
**Research Question(s):** This paper investigates the usage of arbitrated quantum signatures (AQS) and attempts to improve on the security of previously used methods by introducing decoy photons to secure the communications channel.
\
**Contribution:** This source was surprising in that it showed that quantum signatures can be used for both classical and quantum messages. The ability to sign a message using only a single qubit and a trusted third party is valuable. They show that forgery is impossible with this technique, but perfect non-repudiation is not. However, they rebut several possible cases in which the signature could be repudiated.
\
**Rationale:** The paper uses extensive calculations to demonstrate the security of their method and also provide a comparison to a quantum public key technique.
\
**Investigative Approach:** This paper presents a theoretical implementation of a new AQS method as well as rigorous mathematical defense of its validity and security, which is appropriate in this case.
\
**Lessons Learned:** The signature scheme proposed by the authors works with only a single qubit and does not require the sharing of an entangled Bell state between two parties. They also show that the trusted third party in the signature scheme provides superior security to other similar schemes as it provides real time non-repudiation.
\
**Implications for Practice:** This signature scheme could be used for signing quantum messages, but it is not useful for signing classical messages. One interesting circuit introduced (to me at least) in this paper was the quantum swap test, which checks the equality of two qubits without measuring either of them.
\
**Implications for Research:** A major takeaway is that unconditionally secure quantum signatures for quantum messages are impossible. Another is that quantum one-way functions like those used in RSA are difficult to establish, though rotation operators are promising candidates and function in this manner under certain constraints.

3. 
