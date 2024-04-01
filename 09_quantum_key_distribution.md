# Quantum Key Distribution
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

## Code Snippets (Cirq):
#### BB84 Protocol

**Transmitter Code:**
```python
encode_gates = {0: cirq.I, 1: cirq.X}
basis_gates = {'Z': cirq.I, 'X': cirq.H}

num_bits = 5
qubits = cirq.NamedQubit.range(num_bits, prefix = 'q')

alice_key = choices([0, 1], k = num_bits)
alice_bases = choices(['Z', 'X'], k = num_bits)
alice_circuit = cirq.Circuit()
for bit in range(num_bits):
	encode_value = alice_key[bit]
	encode_gate = encode_gates[encode_value]
	basis_value = alice_bases[bit]
	basis_gate = basis_gates[basis_value]
	qubit = qubits[bit]
	alice_circuit.append(encode_gate(qubit))
	alice_circuit.append(basis_gate(qubit))
```

**Receiver Code:**
```python
bob_bases = choices(['Z', 'X'], k = num_bits)

bob_circuit = cirq.Circuit()
for bit in range(num_bits):
	basis_value = bob_bases[bit]
	basis_gate = basis_gates[basis_value]
	qubit = qubits[bit]
	bob_circuit.append(basis_gate(qubit))
	bob_circuit.append(cirq.measure(qubits, key = 'bob key'))


bb84_circuit = alice_circuit + bob_circuit
sim = cirq.Simulator()
results = sim.run(bb84_circuit)
bob_key = results.measurements['bob key'][0]
```

**Comparing**
```python
final_alice_key = []
final_bob_key = []

for bit in range(num_bits):
	if alice_bases[bit] == bob_bases[bit]:
		final_alice_key.append(alice_key[bit])
		final_bob_key.append(bob_key[bit])

if final_alice_key[0] == final_bob_key[0]:
	final_alice_key = final_alice_key[1:]
	final_bob_key = final_bob_key[1:]
else:
	print('\n\nEve was listening, we need to use a different channel!')
```