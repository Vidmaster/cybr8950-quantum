# Quantum Key Distribution Protocols Analysis

## Make QKD practical: 
Our original goal for this project is to seek out a proper and efficient Quantum Key Distribution protocol to satisfy both performance and security during the key transmission
between two network nodes or even more users. Since the real implementation of QKD is different with the theoretical way, we would like to do some research with respect to make 
QKD practical. In the below list, we have provided a general view of those different QKD protocols that either are under analyzing by other researchers or have been experimented 
using real quantum related devices. 

## BB84: Transmission distance: 200 km with multiplexing and 240km without it
*	**Definition:**   
    It is proposed in 1984 by Bennett and Brassard – that’s where the name comes from. The idea is to encode every bit of the secret key into the polarization state of a single
    photon. Because the polarization state of a single photon cannot be measured without destroying this photon, this information will not be available to the eavesdropper 
    without reveal himself or resend the photon. 
*	**Advantages:**  
    1.	Absolute security in theory.    
    2.	Possible to be attacked, but difficult to get correct key – the measurement from Eve side will change the qubit itself.   
*	**Disadvantages:**  
    1.	If there is an Eavesdropper, the measurement result will be affected.   
    2.	Hard to be 100% achieved because the real QKD tools are not fully developed, so there exist security loopholes on both sender and receiver.   
*	**Basic Process:** 
    1.	Alice transmits a random sequence of 0s and 1s qubit, alternating the bases × and + randomly. 
    2.	Bob receives the qubit sequence from Alice and randomly alternates the measures between bases × and +. 
    3.	Alice broadcasts the succession of bases used in a public channel. 
    4.	Bob reports to Alice in what cases he was able to guess the origin bases. 
    5.	They both select a part of result to compare to see if the error rate is above or under the requirement. 
    6.	By using the bits of two match identical bases, they both have defined a random succession of bits that will do as OTP for transmission. 
*	**Visual Illustration:**  
    ![BB84](/image/bb84(1).png)

## Protocol E91: 200 km with multiplexing and 240km without it
*	**Definition:**   
    Developed by Arthur Ekert in 1991. This protocol is based on quantum entanglement. To start, entangled photons are produced, so if Alice and Bob measure the photon’s 
    orientation (whether is vertical or horizontal) they will always obtain opposite responses, the same way as if they measure diagonal bases. The individual results are
    completely random, meaning that it cannot predict what Alice will obtain on her measure. Additionally, same with the BB84 procedure, in E91 protocol Alice and Bob choose
    a random basis for measurement and discussing them in classical channel. If Alice and Bob use the same basis, then according to the quantum principle they should get
    opposite results. E91 protocol using Bell’s Inequality test to detect the presence of eavesdropper.
*	**Advantages:**  
    Using the opposite measured response, so the attacker cannot predict the result.
*	**Disadvantages:**  
    1.	Could have the same base as a coincidence, which increases the re-transmission rate. 
    2.	Too much resources consumption including system, hardware, or supplement. For example, it has technological difficulties of computing resources, since it relies on quantum entanglement.  
*	**Basic Process:** 
    1.	N pairs of entangled states are generated in a random way, and the initial length of the key is ‘n’. 
    2.	For each pair of entangled state, one is sent to Alice and another to Bob. 
    3.	Alice and Bob independent and randomly choose a measure bases and apply them to each photon. 
    4.	After the measures, Alice and Bob uncover their bases (keep obtained results secretly).
    5.	They will have the common key except the case while same bases they have used.
*	**Visual Illustration:**   
    ![E91](/image/e91(2).png)


## MDI-QKD:  Transmission distance: 404 km (Best choice in current protocol)
*	**Definition:**   
    Measurement device independent QKD (MDI-QKD) as a simple solution to remove all (existing and yet to be discovered) detector side channels, arguably the most critical 
    art of the implementation, and show that it has both excellent security and performance.
*	**Advantages:**  
    It offers an immense security advantage over standard security proofs such as Inamori-L¨utkenhaus-Mayers (ILM) and GottesmanLo-L¨utkenhaus-Preskill (GLLP). Furthermore,
    compared to standard security proofs, it has a key advantage of removing all detector side channels, and it can double the transmission distance covered with conventional
    QKD schemes using WCPs. Moreover, it has a rather high key generation rate which is comparable to that of standard security proofs. 
*	**Disadvantages:**  
    Only a minor drawback because Alice’s and Bob’s signal sources can be attenuated laser pulses prepared by themselves. Their states can thus be experimentally verified in 
    a fully protected laboratory environment outside Eve’s interference through random sampling.
*	**Basic Process:** 
    1.	Both Alice and Bob prepare phase randomized weak coherent pulses (WCPs) in the four possible BB84 polarization states and send them to an untrusted relay Charlie (or Eve) located in the middle. 
    2.	Once the quantum communication phase is completed, Charles uses a public channel to announce the events where he has obtained a successful outcome in the relay, including his measurement result as well. 
*	**Visual Illustration:**   
    ![MDI-QKD](/image/mdiqkd(2).png)


## B92 Protocol:  200 km with multiplexing and 240km without it
*	**Definition:**   
    B92 protocol is simplified version of BB84 protocol that proposed by Bennett in 1992. B92 protocol only use one of two polarization non-orthogonal states while in BB84 use     one of four photon polarization states. The B92 protocol utilizes most of the BB84 scheme steps that are based upon the polarization of the states, but it takes a critical     action when Bob measures Alice’s qubits in two bases to produce two states. 
*	**Advantages:**  
    1. A single non-orthogonal basis can be used for encoding and decoding QKD protocol without affecting the ability to detecting the presence of eavesdropper. In other              words, it can be considered as an "unconditional secure" over either lossy channel or noisy channel. 
    2. While the receiver selected the wrong bases, he/she will not measure anything, and this mechanism is known as erasure. 
*	**Disadvantages:**  
     The B92 is using strong reference pulse, so the attacker can obtain more detail about the encryption key in B92 than BB84 protocol based on the dedicated error level. As
     a result, the security level of B92 is explicitly lower than BB84.
*	**Basic Process:** 
    1.	Alice initiates N random qubits through two bases (×, +) and two non-orthogonal states |0> and |1>.
    2.	Bob measures the received qubits in random basis follow with some patterns shown below. (? represent whatever Alice sent)
        |  Alice Bases | + | + | × | × |
        | ------------ | - | - | - | - | 
        | Alice Qubit  | 0 | 0 | 1 | 1 |
        |  Alice Sent  | 🡒 | ? | ? | 🡕 |
        |   Bob Bases  | + | × | + | × |
        | Bob Received | 🡔 | 🡒 | 🡕 | 🡑 | 
   
    3.	 Alice contact with Bob in a public channel to tell what qubit result that.
    4.	 Bob need to expose some uncentain measurement to Alice, so Alice can ignore those.
*	**Visual Illustration:**   
    ![B92](/image/b92.svg)



## Twin-field quantum key distribution，TF-QKD: transmission distance: 509 km
*	**Definition:**   
    The twin-field (TF)-QKD protocol, proposed by Lucamarini and the other scietists. TF-QKD represents a novel QKD approach whose principal merit is to beat the point-to-         point private capacity of a lossy quantum channel, thanks to performing single-photon interference in an untrusted node. In other words, In TF-QKD the information is           encoded in the phase of the optical pulses prepared by the two users that want to establish the secure communication, and the secret key is retrieved via a single photon       interference measurement made by a user in the middle.   
    
*	**Advantages:**  
    1. It can solve the PLOB bound, which focuses on finding the upper bound of security key rate. Such as, the secret key rate without quantum repeaters must satisfy R ≤              −log(1 − η).
    2. Compare to measurement-device-independent (MDI) QKD woth using two-photon interference, TF-QKD makes use of single-photon interference to generate keys, and on average        only one photon passes through either Alice's or Bob's channel—which allows to key rate to scale with transmittance over only half the distance between Alice and Bob. 
    3. It can ensure the security by switching probabilistically between a code mode and a test mode. Hence, the code mode is using for key generation, and the test mode is          for parameter estimation. 
    4. This can break the distance limitation to make quantum repeater and quantum memory become practical. Such as, TF-QKD can use different phase of interference to amplify        the quantum signal, so it can be utilized at a long distance almost twice as long as traditional QKD protocols with enought security level.  
  
*	**Disadvantages:**  
    1. The generation of twin optical fields mode-match system from two space-separated laser sources are difficult to construct.  
    2. The stabilisation of the channel used during the communication has to be strictly dedicated and precise compare to original QKD protocols. 
    3. The control systems (e.g.Weak-Coherent-Pulses(WCP) Phase-locking maintaining system; WCP Timing control system, Frequency-locking wavelengths matcher system, and              Polarization control system) are much difficult to operate between two lasers sources.   
  
*	**Basic Process:** 
    1.	 Alice and Bob randomly choose code mode or test mode to make sure it satisfies the security requirement.
    2.	 If a code mode is selected, Alice (Bob) randomly generates a key bit ka (kb) and a random number x (y) and then prepares the coherent state. 
    3.	 Both parties send their optical pulses to the untrusted node Charlie via optical channels in a synchronized manner.
    4.	 The central node Charlie applies a balanced beamsplitter to the incoming pulses and features two threshold detectors at its output ports 
    5.	 The node Charlie announces the measurement outcome kc (kd) of detector Dc(Dd), corresponding to a no-click and a click event, respectively 
    6.   Alice and Bob form their raw keys with the bits ka and kb collected when both parties chose the X-basis and node Charlie reported a click in only one detector (kc +            kd). Bob then flips his bits kb for which the click occurred in detector Dd.
    7.   Alice and Bob perform information reconciliation and privacy amplification to extract the final secure keys. 
*	**Visual Illustration:**   
    ![tfqkd](/image/tfqkd.png)
    
    
 # Resources (Paper's Topic without links)
 * Comparison and Analysis of BB84 and E91 Quantum Cryptography Protocols Security Strengths (Luis Cáceres Alvarez, Patricio Collao Caiconte).
 * Research on Plug-and-Play Twin-Field Quantum Key Distribution (Chang Hoon Park, and others).
 * Measurement device independent quantum key distribution (Hoi-Kwong Lo and others).
 * Analysis of Secure Bit Rate for Quantum Key Distribution based on EDU-QCRY1 (Damayani Suyitno and others).
 * Quantum Key Distribution (QKD) Protocols: A Survey (Ali Ibnun Nurhadi, Nana Rachmana Syambas).
 * Optimized protocol for twin-field quantum key distribution (Rong Wang and the others). 
 
