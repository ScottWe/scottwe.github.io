---
title: 'The Geometry of Toffoli-Hadamard Circuits'
tags: ["quantum computing","quantum circuits","equational theory","toffoli-hadamard","E8 lattice","lattice","circuit synthesis","circuit complexity"]
description: "Toffoli-Hadamard circuits can be viewed as the simplest class of universal quantum circuits. The goal of this project is to understand their relations and complexity through Coxeter geometry."
summary: "Toffoli-Hadamard circuits can be viewed as the simplest class of universal quantum circuits. The goal of this project is to understand their relations and complexity through Coxeter geometry."
date: 2021-01-01
startYear: 2021
hideAuthor: true
cover:
    image: "toffoli_circuit.png"
---

---

#### Contributors:

+ Scott Wesley :cat:
+ Matthew Amy (Simon Fraser University)
+ Neil J. Ross (Dalhousie University)

---

#### Project overview

Reversible computing is a model of computation in which each operation is invertible.
The simplest reversible gate is the $X$-gate (also called a NOT gate), which permutes the basis states $\ket{0}$ and $\ket{1}$.
A slightly more sophisticated construction is the reversible conditional statement $C( G )$, which applies the gate $G$ if and only if some *control wire* is in state $\ket{1}$.
It was shown by Toffoli in 1980 [T1980] that all classical reversible circuits could be constructed using only the following gates.
$$\mathcal{G}_C = \lbrace X, C( X ), C( C( X ) ) \rbrace$$
Since the Hadamard gate $H$ sends $\ket{0}$ to $\ket{+}$ and $\ket{1}$ to $\ket{-}$, the following gate set can then be thought of as classical reversible computing extended with the ability to prepare uniform superpositions.
$$\mathcal{G}_Q = \lbrace X, C( X ), C( C( X ) ), H \rbrace,$$
Circuits over $\mathcal{G}_Q$ are referred to as *Toffoli-Hadamard circuits*, and can be thought of as the simplest truly quantum circuit language.

It can be shown [AGR2020] that the circuits expressible over $\mathcal{G}_Q$ are *essentially* the orthogonal matrices over $\mathbb{Z}[ 1 / 2] = \lbrace n / 2 : n \in \mathbb{Z} \rbrace$ up-to a factor of $1 / \sqrt{2}$.
Despite these operators being strictly real, this gate set is universal for quantum computation in the *appropriate* sense [A2003,S2003].
More recently [P2011,G2020], it was observed that the $3$-qubit circuits expressible over $\mathcal{G}_Q$ recover the automorphisms of the $E8$-lattice, $W( E_8 )$.
A natural question is whether this geometric structure can be used to better understand this simple yet universal circuit family.

This project considers applications such as circuit presentations, circuit complexity, and circuit synthesis.

---

#### Publications and preprints

+ [ARS2024](/papers/qpl2024/): Finds a presentation for the $3$-qubit $\mathcal{G}_Q$-circuits via the enactment of $W( E_8 )$ as a subgroup; obtains new Toffoli bounds for these circuits.

---

#### Future work

Coxeter groups are a combinatorial abstraction of finite reflection groups and form a class of automatic groups.
It is well-known that $W( E_8 )$ is a Coxeter group [H1990].
The full group of $3$-qubit Toffoli-Hadamard circuits can be obtained from $W( E_8 )$ by adding the reflection $C( C( Z ) )$.
Since this group is infinite, it is not immediately clear whether it is Coxeter.
If this group was shown to be Coxeter, then it would follow immediately that the $n$-qubit Toffoli-Hadamard circuits are also Coxeter, opening the door for a quadratic time solution [E1992] to the Toffoli-Hadamard word problem.

Another direction for future work is lattice-based circuit synthesis.
In the exact circuit synthesis problem you are provided with an orthogonal matrix over $\mathbb{Z}[ 1 / 2 ]$ and are asked to find a circuit over $\mathcal{G}_Q$ enacting the matrix.
Lattice-based methods have proven very successful for exact circuit synthesis [KBRY2015].
We would like to make use of the $E8$-lattice to derive new circuit synthesis algorithms for $\mathcal{G}_Q$.

---

#### Project material

+ [A poster describing the 3-qubit presentation](cms2023.pdf) (2023).
+ [Rough notes on how rewriting could be used to prove complexity bounds](2bit_cnot_complexity.pdf) (2024).

---

#### Related work

+ [[A2003](https://arxiv.org/pdf/quant-ph/0205115)] Proves that $\mathcal{G}_Q$ is universal for quantum computation.
+ [[AGLR2023](https://arxiv.org/pdf/2305.11305)] State-of-the-art method for exact synthesis over $\mathcal{G}_Q$.
+ [[AGR2020](https://arxiv.org/pdf/1908.06076)] Provides a number-theoretic characterization of $\mathcal{G}_Q$.
+ [[E1992](https://doi.org/10.1201/9781439865699)] A reference text on automatic groups.
+ [[G2009](https://etd.ohiolink.edu/acprod/odb_etd/ws/send_file/send?accession=toledo1250224470)] A thesis on the complexity of Toffoli circuits via group presentations.
+ [[G2020](https://cp4space.hatsya.com/2020/05/10/minimalistic-quantum-computation/)] Observes that a subgroup of $\mathcal{G}_Q$ enacts $W( E_8 )$.
+ [[H1990](https://doi.org/10.1017/CBO9780511623646)] A reference text on finite Coxeter groups.
+ [[KBRY2015](https://arxiv.org/pdf/1510.03888)] Includes a summary of lattice-based synthesis techniques up-to 2015.
+ [[LRS2021](https://arxiv.org/pdf/2106.01175)] Provides a presentation for $\mathrm{O}( \mathbb{Z}[ 1/ 2 ])$.
+ [[P2011](https://arxiv.org/pdf/0904.3691)] An earlier paper connecting $\mathcal{G}_Q$ to $W( E_8 )$.
+ [[S2003](https://arxiv.org/pdf/quant-ph/0301040)] An alternatives proof that $\mathcal{G}_Q$ is universal for quantum computation.
+ [[T1980](https://link.springer.com/chapter/10.1007/3-540-10003-2_104)] Establishes the completeness of $\mathcal{G}_C$.

---
