## Types of Qubits
There are different types of Qubits which vary in:
- Errors
- Scalability
- Use Case

### Photonic Qubits
- Photonic Qubits utilise light particles, specifically photons, as the fundamental units of quantum information. 
- They are manipulated by optical elements, such as prisms and silicon photonic chips, with beam-splitters and mirrors serving as quantum gates. 
- Photonic Quantum Computing (PQC) allows for the encoding of quantum information in various ways, including through the polarisation of photons or their paths of travel. 
- This technology is advantageous for its resilience to certain types of noise sources and the ability to travel long distances along existing fibre optic cables, supporting the idea of a quantum internet. 
- However, it faces challenges like the need for quantum error correction and the requirement for cryogenic equipment for certain components.

### Super Conducting Qubits
- Superconducting Qubits operate at critical low temperatures where resistance is nearly zero, allowing for the representation of current flowing in different directions as 0 and 1. 
- These qubits are manipulated using electromagnetic pulses to control the magnetic flux, electric charge, or phase difference across specific areas of the superconducting circuit.
- They are known for their speed, simple gates, and high-quality operations but face challenges such as short lifespan, requiring extensive error corrections, and the need for cooling to very low temperatures. 
- Superconducting qubits are used by companies like Google and IBM in their quantum computers, showcasing their potential for high-speed operations.

### Trapped Ion Qubits
   - Trapped ion qubits are based on the electronic and nuclear spin states of individual ions that are trapped and manipulated using electromagnetic fields. They can be implemented using ions like calcium, magnesium, and beryllium.
   - Each ion acts as a qubit, and interactions between them are controlled using laser or microwave radiation. This radiation is used to execute logic gates by coupling the ground states of the ion to the motion of the ions, inducing entanglement. This allows the system to perform more complex computations.
   - Trapped-ion qubits have particularly long coherence times, which is how long a system maintains its quantum state. It can be orders of magnitude higher than in superconducting qubits, reducing error correction requirements. This allows quantum information to be stored and manipulated for longer, allowing for high-fidelity operations.
   - While trapped-ions themselves don't need to be super-cooled during operation and can be at room temperature, the surrounding machinery does need temperature control to maintain a high vacuum and stable electromagnetic field. The heat from the lasers also needs to be cooled.

### Topological Qubits
   - Topological qubits are a highly experimental type of qubit that use a unique form of particle known as anyons. These qubits are made resistant to noise and errors through their braided nature, requiring far fewer qubits to achieve utility .
   - They operate in a non-Abelian quantum phase of matter known as a topological state of matter, which was largely theoretical until recent breakthroughs by researchers from Microsoft and Quantinuum proved it was possible.
   - Topological quantum computers may still require super=cooling like superconducting qubits, as the topological state of matter is very delicate and could be easily disturbed by thermal fluctuations. Coherence times and scalability for these qubits are not yet fully understood.
   
### Nitrogen Vacancy Centre Qubits
   - Nitrogen Vacancy (NV) centres are created by replacing a single carbon atom in a diamond’s atomic lattice with a nitrogen atom and leaving a neighbouring lattice node empty. This creates a flaw, or blemish, in an otherwise super-pure atomic structure.
   - In this setup, electrons occupy orbitals inside the vacancy of the NV centre while the NV centre's electronic spins react with the nuclear spin of some of the carbon atoms nearby. Both the NV centre and the adjacent carbon atoms function as qubits, and the diamond lattice keeps them stationary and entangled.
   - These qubits—called solid-state spin qubits—are limited since the system can only have as many qubits as there are neighbouring carbon atoms. NV centres are difficult to control, which means they might not be as scalable as other options. However, they can operate at room temperature, which is a significant advantage.
   - Researchers have entangled an NV centre's electronic spin with the spins of nine nearby nuclei, indicating promising progress in this burgeoning technology.

## Issues with Qubits:
Qubits are highly sensitive are sensitive to many factors are cause **errors**.
1. Temperature
2. Light
3. Vibrations
4. Other qubits
5. Cosmic rays

These factors are called as Noise and can lead to decoherence of qubits .i.e
1. **Relaxation:** Switching from high level to low level state
2. **Dephasing:** Loss of Phase information

## Goof Quantum Computer
The Da Vincenzo's criteria for a good QC is:
1. Well characterised and scalable qubits
2. Initialisation Qubits
3. Long coherence items
4. Universal set of gates
5. Efficiently measurable 

## Code (Noise)
```python
```