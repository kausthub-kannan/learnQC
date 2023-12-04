## Algorithms and Protocols:
Specific step wise procedure solving a problem is termed as algorithm whereas protocols are rules that are used to allow the procedure to take place.  In terms of inter-computer communication, algorithm is the procedure to communicate and protocol allows the computer to communicate under regulations.

In Quantum algorithms a Q-state is applied to Q-circuit and measurement is applied on it. Quantum algorithm are termed useful if they are able to overcome the come backs of classical algorithms and solved a meaningful problem. Q-protocols allow the Q-computers to communicate with each other. 

### Q-protocols:
Quantum protocols are famously found as:
1. **Quantum Teleportation:** Sending quantum information more efficiently using quantum computers along with classical bits.
2. **Superdense Coding:** Sending classical information more efficiently using quantum computers along with classical bits.
3. **Quantum Key Distribution:** Create a secure password for classical communication by sending Qubits and classical bits.

### Quantum Key Distribution (QKD):
Cryptography protocols use encryption and decryption and sent via a channel. This ensure secure communication gateway.  To communicate securely, secret key is used which is shared using key distribution protocols. Allowing a Eave dropper to intercept the protocol would leak the secret key. 

### QKD BB84:
BB84 relies on state of qubit which can be altered using measurement. The information is encoded in qubits with a **specific basis**. Even if Eave dropping is done where the Qubits are measured in between, this would result in the eave dropper to not know the true information as he doesn't know the encoding basis. 

The process of BB84 is as follows:
1. The transmitter converts random bits (t-key) to qubits with a randomly chosen basis. These qubits are sent via channel to receiver. 
2. The receiver picks random qubits with random state and measure the qubit converting it back to bits (r-key). 
3. On the other hand in a classical channel, the transmitter communicates with receiver about if the basis the bits were encrypted in.
4. Both compare the bits (keys) they have measured and remove those bits which different basis were applied.

BB84 is secure due to the following reasons: 
1. By using Quantum Algorithms, BB84 protocol supports **No-cloning theorem.** The information about the basis can be exposed in classical communication to the Eave dropper. But the eave dropper cannot use this information as this communication is done after quantum communication. As cloning is not possible for quantum states, the Eave dropper cannot clone the states and apply the basis later
2. BB84 uses public channels alone. Quantum public channel is used for communication of states of bits and classical public channel to communicate basis.
