---
layout: post
title: Basic Gates
permalink: /gates/
---
# Bases
Bases describe the state at which the current position is measured. In terms of Cartesian System it is often describe in the format of P(x,y,z). 

**Note:**
Generic representation considers z-axis to move upwards, x-axis to move towards (or away) us and y-axis to move side ways. 

## Quantum Gates 
Quantum Gates rotate the Qubit represented in the Bloch sphere to rotate. You can visualise these changes quickly in this [Bloch Sphere Simulator](https://bloch.kherb.io/). 
### Pauli's Gates:
1. **X Gate:**  
   Pauli's X gate rotates the Qubit by **108**$$^0$$ in X bases .i.e it switches the amplitudes of the $$|0⟩$$ and $$|1⟩$$ states. In the form of matrix, Pauli's X Gate is represented as follows:
   
   $$
   \begin{bmatrix}
   0 & 1 \\
   1 & 0
   \end{bmatrix} = \ket{0}\bra{1} + \ket{1}\bra{0}
   $$
   Consider the example of applying X gate to $$\ket{0}$$ which can be shown as follows: 
   
   $$
   X|0⟩ = \left( \begin{array}{cc} 0 & 1 \\ 1 & 0 \end{array} \right)
   \left( \begin{array}{cc} 1 \\ 0 \end{array} \right) = \left( \begin{array}{cc} 0 \\ 1 \end{array} \right) = \ket{1}
   $$

2. **Y-Gate:**  
   Similar to X-Gate, Y-Gate rotates the qubit in Y bases. In the form of matrix, Pauli's Y Gate is given as: 
   
   $$
   \begin{bmatrix}
   0 & -i \\
   i & 0
   \end{bmatrix} = -i\ket{0}\bra{1} + i\ket{1}\bra{0}
   $$
   
3. **Z-Gate:**  
   Similar to X-Gate, Z-Gate rotates the qubit in Z bases. In the form of matrix, Pauli's Z Gate is given as: 
   
   $$
   Z = \ket{0}\bra{0} + \ket{1}\bra{1}
   \begin{bmatrix}
   1 & 0 \\
   0 & -1
   \end{bmatrix}
   $$
   
### H Gate:
The Hadamard gate (H-gate) is a fundamental quantum gate. It allows us to move away from the poles of the Bloch sphere and create a superposition.  H-Gate is given as:

$$
\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix} 
$$

### P-Gates:
The P-gate (phase gate) is parameterised, that is, it needs a number $\phi$ to tell it exactly what to do. The P-gate performs a rotation of around the Z-axis direction. It has the matrix form:

$$
\begin{bmatrix}
1 & 0 \\
0 & e^{i\phi}
\end{bmatrix} 
$$

Where $$\phi$$ is a real number.

### I-Gate:
The *Identity* Gate does nothing! Applying the gate does nothing on the circuit. It's primarily used in 2 places:
1. To prove a gate is its own inverse: $$I = XX$$
2. It is often useful when considering real hardware to specify a ‘do-nothing’ or ‘none’ operation.

### S-Gate:
The S gate (also called $$\sqrt{Z}$$ gate) is a P gate with $$\phi = \frac{\pi}{2}$$
It does a quarter-turn around the Bloch sphere. It is important to note that unlike every gate introduced in this lab so far, the S-gate is not its own inverse! As a result, you will often see the $$S^†$$, which is a P gate with $$\phi = \frac{-\pi}{2}$$

The reason it's also called a $\sqrt{Z}$ gate is because two successive S gates is equal to a Z gate:
$$SS|\psi\rangle = Z|\psi\rangle$$

### T-Gate:
The T gate is also commonly used, which is a P gate with $$\phi = \frac{\pi}{4}$$.
It's also known as a $$\sqrt[4]{Z}-$$ gate

**Note:**
1. In physical sense, the state change is shown by applying specific polarised light to the Qubit. This changes the bases or the state of Qubit.
2. By default, gates and circuits are initialised with 0. 