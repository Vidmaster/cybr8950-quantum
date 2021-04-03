# Diagrams

## Qiskit

The following are circuit diagrams and post-measure analytics for an [implementation](https://github.com/Vidmaster/cybr8950-quantum/blob/main/Resources/BB84-demo.ipynb) of the BB84 QKD protocol.

This icon symbolizes a measurement operation, where the value of a qubit is measured and saved to the output.

![Measure gate](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/QK_measure_gate.png)

This icon symbolizes a Hadamard gate, which creates a superposition and results in measurement with equal probabilities for 0 and 1.

![Hadamard gate](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/QK_H_gate.png)

This circuit diagram shows how Hadamard gates can be combined to encrypt communications between Alice and Bob.

![BB84 Circuit](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/QK_bb84_AB.png)

Upon measuring the qubit sent by Alice, Bob observes a probability of 1.0 that he receives the value prepared by Alice.

![BB84 Circuit Measured](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/QK_bb84_AB_measured.png)

This is the same circuit diagram as above, but shows where an eavesdropper may attack this system by measuring the qubit prior to Bob's receipt, which is represented by the second measurement.

![BB84 Circuit - Eavesdrop](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/QK_bb84_AEB.png)

The results of Bob's measurement show approximately equal probability of receiving 0 and 1, indicating that the transmission has been compromised.

![BB84 Circuit - Eavesdrop Measured](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/QK_bb84_AEB_measured.png)

## Eavesdropping

The following diagram illustrates how an attacker, Eve, might compromise the photonic transmission of qubits from Alice to Bob. *([Link](https://lucid.app/lucidchart/invitations/accept/8b2ddd33-ce11-4184-84df-14ea27d31d76) to diagram in Lucidchart)*

![Eavesdropping](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/eavesdropping_diagram.png)

## Amerimehr Encryption Scheme

The following process diagram is an overview of the symmetric quantum cryptosystem proposed by Amerimehr and Dehkordi. *([Link](https://lucid.app/lucidchart/invitations/accept/50b8bbf1-894a-420e-b940-4401e2995cc2) to diagram in Lucidchart)*

![Amerimehr Scheme](https://github.com/Vidmaster/cybr8950-quantum/blob/main/image/AD2018-qc.png)
