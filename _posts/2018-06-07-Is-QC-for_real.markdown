---
[comment]: <> (layout: default.)  
[comment]: <> (published by: Omer.)   
#### Title: Is Quantum Computing for Real?
#### Gist: D-Wave engineer explains Quantum Annealing - notice, the title is misleading - it is only focused on QA.
---
**_Intro_**   
D-Wave is the global leader in Quantum Annealing (henceforth QA). Their Quantum Processing Unit (QPU) is designed to solve a group of problems known as Adiabatic Optimization Problems (basically, they are discrete problems with multiple solutions and we are trying to find the best solution given the constraints.)

The latest edition of thier qubit's computer will include 2048 qubits. Companies who have already purchased D-Wave's beasts include Google, NASA, some universities and the defense giant Lockheed Martin.

**_Important Comments_**   
The author points : _"no theoretical guarentees available on how cloe the optimal solition will be, or on how much time it would take to find an optimal solution"_.  
An important point is that the real challenge is the translatino of the problem to a quantum model so it can be solved.  
There is a tradeoff between running time and the quality of the problem.  
And important challenge is that we cannot know in advance which inputs will be easy or hard for which heuristics. 
A big challenge is isolating the QPU from ambient noise, which in experiments often times we fail to do.  

The good part of the article starts after page 8:

**_Essentialy, the process of using the machine includes the following setps:_**  
1. Translating the problem such that it becomes a spin assignment problem.  
2. Setting the system into the initial superposition state.  
3. Anneal the system by assigning weights to the graph. Those weights constitute the problem mapped.  
4. Let the qubits turn either way.  
5. Measure the qubits and translate to bits.  

The article uses an anology of water which I found very useful. Notice the equation explainig how the Hamiltonian works with the system before and after the annealing.  

Anothe point worth taking is the explanation regarding entanglement which I found useful.  


**_The Ising Model_**   

_Why we care about this model?_   
Essentialy, optimization problems can be transformed into the ising model problem since it is inherently an optimization problem that explores binary configurations that entail a set of solutions. Since the Ising model solves for the lowest energy state, it essentialy solves an optimization problem.

The D-Wave machine essentialy solves the Ising mode. That's it. The Ising model is a way to understand phase transitions (i.e. transformation between phases of matter via heating). The model assigns inputs such the the system evaluates to True state (using ordinary gates). Then, the gates are transformed to booleans. The booleans are then represented in IM Expression with assigned spins, which correspond to the bits (0= is -1, 1 is 1).  
Notice the fact that when the sets of equations solve for 1, becomes a new problem in which the sum of all expressions is minimized.


