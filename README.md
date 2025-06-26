# SOC_2025

## Week 1 - Fundamentals of Quantum Mechanics
In the first week, I brushed up on the basics of quantum mechanics, required for understanding Quantum Computing.
<br>The topics covered were -
1) Quantum Formalism - Including vector spaces, inner products, tensor products, operators etc.
2) The postulates of Quantum Mechanics
3) Projective and POVM measurements

Resources -
<br>Chapter 2, Quantum Computation and Quantum Information, Nielsen and Chuang

## Week 2 - Basics of quantum gates and circuits
### Qubits
A qubit is a quantum object that carries information. While a classical bit can only be either 0 or 1, a qubit can be in a _superposition_ of both states.
<br>$|0\rangle$ and $|1\rangle$ are called the _basis_ states of a single qubit. Hence, a qubit that is in some superposition of both states, is written as -
<br>$|\psi\rangle$ = $a|0\rangle + b|1\rangle$, where $|a|^2 + |b|^2 = 1$.
<br>Hence, we can visulaize the qubits as unit vectors in a 2-d vector space.
<br>Upon measuring, a qubit, it outputs either 0 or 1, with probability $|a|^2$ and $|b|^2$ respectively. After the measurement, the qubits _collapses_ to the state $|0\rangle$ or $|1\rangle$, and is, effectively, destroyed.
### Gates
Gates are **unitary** operators that act on qubits. Some commonly encountered gates are X, Y, Z, Hadamard, CNOT, and so on. Gates may take multiple qubits as input, and output multiple qubits, e.g., CNOT inputs 2 qubits and outputs 2 qubits.
### Entangled State
In simple words, two qubits are said to be in an entangled state, when their combined state is not a _product_ state. This means that making a measurement on one of the qubits is not independent of making a measurement on the other. Rather, measurement on one entangled qubit affects the state of the other. The Bell states are a famous example of an entangled state. A single pair of entangled qubits is called an ebit.

Resources -
<br>Sections 1.2, 1.3 and Chapter 4, Quantum Computation and Quantum Information, Nielsen and Chuang
<br>Basics of Quantum Information, course by John Watrous, IBM Quantum Learning

## Week 3 - Implementing quantum circuits in qiskit
In this week, I installed and set-up qiskit. Then I learnt how to create my own simple quantum circuits in qiskit, and then moved on to create the follwoing famous circuits -
### Quantum Teleportation
Quantum Teleportation refers to a protocol for transferring 1 qubit from one person (Alice) to another person (Bob), only requiring that both Alice and Bob have 1 shared ebit, and Alice must communicate to Bob 2 classical bits of information.
### Superdense Coding
Superdense Coding is a protocol for transferring 2 classical bits of information from one person (Alice) to another (Bob), and requires them to have 1 shared ebit, and Alice must be able to communicate 1 qubit to Bob. Hence, it is complementary to Teleportation in some sense.

Resources -
<br>Basics of Quantum Information, course by John Watrous, IBM Quantum Learning

## Week 4 - Quantum Algorithms
For certain tasks, quantum algorithms offer a certain advantage in performance over classical counterparts. In week-4, I learnt about Deutsch and Detsch-Jozsa algorithms 
### Deutsch Algorithm
Given an unknown function f that takes as input 1-bit, and outputs 1-bit, we are insterested to know whether f is a 'constant' function, or whether it is 'balanced'.
<br>We call f, 'constant', if it outputs the same bit for all inputs. We call f, 'balanced', if it outputs 0 for exactly half of all possible inputs, and 1 for the rest. We shall assume that the given f **must be** either constant or balanced. Note that in the 1-bit case, it will always be so.
<br>A classical approach to the problem requires 2 queries on the function f, i.e., both f(0) and f(1) need to evaluated in order to determine whether f is contant or balanced. However, we can implement a quantum algorithm called the **Deutsch Algorithm** to determine the same by making only 1 quantum qeury.
<br>The Deutsch algorithm is implemented using a quantum circuit that I implemented in qiskit.

### Deutsch-Jozsa Algorithm
The Deutsch-Jozsa algorithm is the extension of the Deutsch algorithm for the case that f can have multiple-bit inputs. Note that in the classical case, for a function f with n-bit input, we need $2^{n-1} + 1$ queries to say whether f is constant or balanced. However, using the Deutsch-Jozsa, we need to only make 1 qunatum query to get our answer!
<br>I am still working on the qiskit implementation of this algorithm.

Resources -
<br>Section 1.4, Quantum Computation and Quantum Information, Nielsen and Chuang
<br>Fundamentals of Quantum Algorithms, course by John Watrous, IBM Quantum Learning
