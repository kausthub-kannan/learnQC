## Types of Algorithms:
1. **Long Term Algorithms:**
   - Long Term Algorithms are more powerful and assume perfect fault tolerant hardware.
   - These type of algorithms require millions of qubits which would help in isolating noise to acceptable level.
   - Ex: Grover's Algorithm
2. **NISQ (Noisy Intermediate Scale Quantum):** 
   - NISQ also called as Near term algorithms along side classical computer to perform more efficiently than classical one
   - Ex: VQE Algorithm
## Types of NISQ:
1. **Hybrid Algorithms:**
   - Hybrid algorithms use both quantum computing and classical computing to solve problems.
   - The Hybrid algorithms can follow the below steps:
     1. Quantum Computer (QC) runs your quantum circuit
     2. QC sends the result to the Classical Computer (CC).
     3. CC determines how to modify the circuit.
     4. CC sends new instructions to the QC
     5. The above steps iterate

2. **Variational Algorithms:**
   - Variational quantum algorithms use a process called *optimization* to find the best solution to the problem.
