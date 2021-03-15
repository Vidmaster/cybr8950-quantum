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
    1.	Alice transmits a random sequence of 0s and 1s qubit, alternating the bases  and  randomly. 
    2.	Bob receives the qubit sequence from Alice and randomly alternates the measures between bases  and . 
    3.	Alice broadcasts the succession of bases used in a public channel. 
    4.	Bob reports to Alice in what cases he was able to guess the origin scheme. 
    5.	They both select a part of result to compare to see if the error rate is above or under the requirement. 
    6.	By using the bits of two match identical bases, they both have defined a random succession of bits that will do as OTP for transmission. 
*	**Visual Illustration:**
    ![BB84](/image/bb84.png)

## Protocol E91: Same with BB84
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
    ![E91](/image/e91.png)


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
    ![MDI-QKD](/image/mdiqkd.png)


## B92 

## Twin-field quantum key distribution，TF-QKD: transmission distance: 509 km
