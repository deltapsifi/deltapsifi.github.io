---
layout: post
author: ΔΨφ
title: "Decoherence in Quantum Systems"
tags: 
  - "Decoherence"
  - "Density Matrices"
  - "Quantum Mechanics"
permalink: /2020-09-09-Decoherence-in-Quantum-Systems.md/
---

In Quantum Mechanics we define Quantum Systems by using the wavefunction (Ψ), which is a vector.

For example : - **|Ψ> = a |0> + b |1> + c |2> ..........**

Here what we write in "**ket**" notation (|>) are the possible quantum states and their coefficients are the probabilities for the particular states; these coefficients are complex numbers.

According to the **Born Interpretation** the square of the coefficients are the probabilities and also the sum of all the probabilities is 1. Let's take an example :

**|Ψ> = a|0> + b|1>**

now the probability of measuring state 0 = a.a\*

and the probability of measuring state 1 = b.b\*

\* = complex conjugate

Now in order to understand decoherence let's consider the system to be in superposition.

**|Ψ> = (1/√2) |0> + (1/√2) |1>**

probability of |0> = 1/2

probability of |1> = 1/2

If we add a complex number eiθ then it will not affect the probabilities because if it's product with it's conjugate will be 1.

Now, **$latex\\ket{\Psi} |Ψ> = (1/√2) |0> + (1/√2) \\exp{iθ}|1>$**

We insert this complex number to signify the phase of the system.

**Density Matrices** contain all the (accessible) information about a quantum mechanical system. These take the role of the state vectors discussed so far. A density matrix (**ρ**) is the **ket-bra product** of the wavefunctions.

**ρ** **\= |Ψ><Ψ| = ![](images/image-1.png)** 

Each time the particle bumps into another particle the phase of the system randomly changes and what we actually measure is the average of all these phase changes. Now if we visualize a complex plane every number with an absolute value of 1 lies on a circle and if we take the average then we find that it is not on the circle but at center of the circle i.e. at 0. This means that the phase factors in the matrix become 0. The density matrix now is :

**ρ** = ![](images/image-2.png)

As the phase becomes 0, it destroys the ability of the state to make an interference pattern with itself. What does this decohered density matrix tell us? It tells us the classical probability of each of the states this is because the quantum characteristic of the system has gone away since the phase is 0. So decoherence converts quantum probabilities to classical probabilities. It is necessary to realize that decoherence merely gives us probabilities for what we observe. Decoherence is the only reason we don't see strange quantum behaviour (as observed at the quantum level) because this behaviour goes away with all the interactions of the particles, regardless of the fact whether we measure them or not. For example, when we open the box in Schrödinger's cat experiment, we don't see that the cat is both dead and alive or after a coin toss, we don't see that we have both heads and tails, thanks to decoherence we only see one outcome, otherwise imagine how strange and different the universe would be.

**This, my friends is DECOHERENCE !**