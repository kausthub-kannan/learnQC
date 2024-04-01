Error correction plays a vital role in Quantum Computing especially for longer algorithms. Noise is accompanied which causes issues with computation.

**Quantum Threshold Theorem**: It states that on the NISQ(Noisy Intermediate Scale Quantum) below a particular threshold even with noise, the computation can be performed and is called as **fault tolerant** .

## Quantum Error Correction (QEC)
These are set of techniques which are used to protect quantum computers from errors, often relying on quantum properties since classical approaches do not tend to work. 

This is done using encoding the information in such a way that it is protected from some or all errors and these encoding are called error correcting codes.

## Types of Noise and errors
Types of Noise:
1. Environmental
2. Hardware
3. Decoherence
4. Shot

Types of Errors:
1. Bit Flip
2. Phase Flip
3. Measurement 
4. Stuck

## Classical Repetition Codes:
   - Repeats the information of one bit across many bits. The original bit is called as the **logical bit** represented as $\text{\={0}}$ and **physical bits** as $000$. The majority vote is seen in the physical bit and the bit type having the most is considered as true bit. 
   - To cause error, multiple bits have to be flipped.
   - More the repetition bits, more it is error tolerant.  

### Code

```python
TO BE ADDED
```