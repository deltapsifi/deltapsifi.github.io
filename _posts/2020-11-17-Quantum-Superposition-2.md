---
layout: qcinqs
author: ΔΨφ
title: "Quantum Superposition - 2"
date: "2020-11-17"
tags: 
  - "quantum-bits"
  - "quantum-computing"
  - "quantum-mechanics"
  - "quantum-superposition"
  - "qubits"
permalink: /Quantum-Superposition-2.md/
---

![](/assets/img/1lng2gvwfhgqefn9vjkzk8a.gif)

Hello !! It is very important that you read my previous post on [Quantum Superposition](/2020-11-12-Quantum-Superposition.md/) in order to understand this.

As promised, in this post I will be guiding you on how to make a 2-qubit quantum circuit and then create superposition between the two qubits.

However, you must first understand what a qubit is. A qubit -- short for quantum bit -- is a unit of quantum information and has 2 orthogonal basis states i.e. it can be compared with the Hilbert space (H) with an orthonormalized basis states zero and one. Thus, in the general case, the qubit state is a superposition of states zero and one taken with complex coefficients.

![](https://deltapsifi.files.wordpress.com/2020/11/image-3.png?w=283)

These are the two states of the qubit which can be represented by Ket vectors \|0> and \|1>

This is the quantum state of the qubit :

![](https://deltapsifi.files.wordpress.com/2020/11/image-4.png?w=183)

**Qubits** are generally compared to **polarized photons** or the **spin of an electron** to signify the 2 levels of a qubit. However, the qubits used to make quantum computers are artificially created by isolating two energy levels.

(Make sure to download anaconda on your computer, here is the link : [https://www.anaconda.com/products/individual](https://www.anaconda.com/products/individual))

I'll be working with IBM's Qiskit on Jupyter Notebook. Qiskit is an open source framework for working with quantum computers. Let's start.

Open your anaconda prompt and run the following command :

```bash
pip install qiskit
```
![](https://deltapsifi.files.wordpress.com/2020/11/image-17.png?w=731)

Now open Jupyter Notebook and run the following commands :

```python
from qiskit import *

qr = QuantumRegister(2)
cr = ClassicalRegister(2)

circuit = QuantumCircuit(qr, cr)

%matplotlib inline

circuit.draw('mpl')
```

![](https://deltapsifi.files.wordpress.com/2020/11/image-8.png?w=465)

We have successfully made a quantum circuit with 2 qubits and 2 bits. We can see that both these qubits have the state \|0>. Let's put a Hadamard gate on the first qubit and measure it. We already know that quantum superposition is the linear combination of 2 or more states, so let's see that in action.

![](https://deltapsifi.files.wordpress.com/2020/11/image-10.png?w=720)

I have applied the Hadamard gate in line 6; inside the bracket we write the qubit on which the gate is to be placed. And in the next line inside the bracket we write the qubit (to be measured) and the bit (in which the measurement is to be stored). Now let's look at our circuit once.

![](https://deltapsifi.files.wordpress.com/2020/11/image-11.png?w=417)

"H" is for the Hadamard gate and the speedometer looking thing signifies the measurement.

Now let's execute these circuits. Instead of running these circuits on an actual quantum computer I will be running them on a simulator. The simulator can be imported from " Aer " and the name of the simulator is " qasm simulator ". The name " qasm " comes from quantum assembly language. Then we will execute the circuit and obtain the results.

![](https://deltapsifi.files.wordpress.com/2020/11/image-12.png?w=642)

In the execute command we can also specify the number of shots i.e. the number of measurements that will be made by writing : "shots=(a number)" without the inverted commas; if you don't specify the number of shots then by default it will run 1024 times.

We will get the probability of the measurement of the state of the first qubit, initially in state |0>, through a histogram.

![](https://deltapsifi.files.wordpress.com/2020/11/image-13.png?w=691)

So you can see that we get a roughly 50% probability or 0.5 for the quibit to be in state |0> and |1>. This error is because we are running only a limited number of shots on our simulation instead of an infinite number of shots. You don't have to believe me you can verify this by increasing the number of shots. Although the maximum number of shots cannot exceed 1000000, we get a fair idea. Now you may be thinking that why did this guy take a 2-qubit circuit, he showed superposition with just a single qubit !

I showed you superposition in a qubit that was initially in state |0>. Now we will see superposition in a qubit in state |1> .

How will I do that ?

You may have heard of logic gates in almost all classical programming language such as python etc. One of the most basic gate is the "NOT gate". We have that in quantum computing too, it's sometimes referred to as an " X gate ". This gate changes the state of the qubit. In the same circuit, we will now work on the second qubit.

We will start by placing an X gate and then we will place a barrier. The barrier has no physical importance it's just used for clarity when we visualize our circuit. Speaking of which here is your code and the circuit :

![](https://deltapsifi.files.wordpress.com/2020/11/image-14.png?w=745)

Now that we have the qubit in |1> state, we will take the same steps that we took in the previous case : place an H gate and measure the state.

![](https://deltapsifi.files.wordpress.com/2020/11/image-15.png?w=775)

Now we will once again use the "qasm simulator", execute the circuit, get the results, and visualize the probabilities though a histogram.

![](https://deltapsifi.files.wordpress.com/2020/11/image-16.png?w=812)

See in line 20 I have taken 1000000 shots, which is the maximum number of shots that an be taken, this is the reason why we are getting absolute measurements

Now you may be wondering what's up with these 4 bars, in the previous case we only got 2 !

In this case our circuit includes 2 qubits where both the qubits, though initially in different states, are in a uniform superposition. When we execute the circuit, this entire system gets executed and we get the results for all the four possible outcomes. We can see that we get an entirely random probability : for all the four states of the system we have the probability of 0.25. The first bar, which is for the state " 00 ", signifies that the state of the circuit in which both the qubits are in |0> state has a probability of 0.25. Similarly, in the second bar the first qubit is in |0> state and the second qubit is in |1> state with 0.25 probability and the reverse of this is applicable to the third case. In the fourth case, both the qubits are in state |1> with a probability of 0.25 . I would recommend you to make your own single qubit the circuit and perform the functions that I took in the case of the second qubit. It is necessary to understand the intuition behind this and then anyone can make a circuit and perform a variety of operations.

Please tell me in the comments how you feel about this article and if I should make any changes. Criticism is welcome.