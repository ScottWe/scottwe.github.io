---
title: 'Control Flow in Superposition'
tags: ["quantum computing","quantum circuits","equational theory","quantum control","enrichment","quantum compilation","Frobenius algebra"]
description: "Control flow in superposition concerns quantum generalizations of condition statements. This phenomenon has been studied algebraically, categorically, and analytically. The project strives for a unified framework."
summary: "Control flow in superposition concerns quantum generalizations of condition statements. This phenomenon has been studied algebraically, categorically, and analytically. The project strives for a unified framework."
startYear: 2023
hideAuthor: true
cover:
    image: "placeholder.jpg"
---

---

#### Contributors:

+ Scott Wesley :cat:
+ Neil J. Ross (Dalhousie University)
+ William Schober (Università della Svizzera italiana)

---

#### Project overview

Classical programs are constructed using high-level control flow abstractions, such as the while-statement and the switch-statement.
It was shown in [YVC2024] that classical approach to implementing control flow does not lift to the quantum setting.
This means that before we can truly understand the design of quantum algorithms, we must learn to master control flow in superposition.

In recent years, much attention has been given to the quantum analogue of the if-then statement, which is a special case of the quantum switch statement.
Given a quantum operation $G$, the *controlled* version of $G$, denoted $C( G )$ can be obtained by linearizing the semantics of the classical if-then statement:
$$
    C( G ):
    \sum_{j=0}^{1}
    \alpha_j \ket{j} \otimes \ket{\psi_j}
    \mapsto
    \sum_{j=0}^{1}
    \alpha_j \ket{j} \otimes G^j \ket{\psi_j}
$$
It was shown in [DP2025] that many properties of $C( - )$ can be recovered through the notion of a *control functor* between PROP categories.
It was further shown in [HKL2025] that $C( - )$ can be fully characterized as a certain kind of control functor between PROPs with rig structures.
However, this construction is seemingly incompatible with two earlier lines of work which showed the following.

1. Controls admit a purely analytic characterization, in terms of the matrix exponential via a construction called *generalized control* [G2017,S2024].

2. controls admit a purely algebraic characterization in terms of morphisms between certain special commutative $\dagger$-Frobenius modules [HV2019].

The goal of this project is to reconcile these three points of view, and to use these insights to improve quantum compilation.

---

#### Publications and preprints

+ [[RW2025](https://arxiv.org/pdf/2607.16114)] Uses enriched category theory to fundamentally relate control functors to special commutative $\dagger$-Frobenius modules.
+ [[SW2026a](/preprints/iwqc2026.pdf)] Explores compilation in light of control functors and generalized control.
+ [[SW2026b](/papers/qpl2026/)] Corrects the soundness of [S2024]; proves completeness of the relations; estbalishes connections between matrix exponentials and control functors.
+ [[SW2026c](https://arxiv.org/pdf/2609.26591)] Applies generalized control to gain new insights on adder circuits.

---

#### Future work

Typically, quantum conditional statements are described as a linearization of the classical if-then statement.
However, not all generalizations of the quantum condition statement have obvious analogues in classical computing.
This motivates the following questions.

+ Can classical conditional statements be characterized using Frobenius algebras?
+ Is the analytic perspective a generalization of [discrete differential equations](https://arxiv.org/pdf/1810.02241v2)?

Regarding the analytic perspective, the following questions remain.

+ Can generalized controls be described purely categorically?
+ For which circuit languages is the [diagrammatic diagonalization](https://arxiv.org/pdf/2611.07207v1) (i.e., compiling generalized control statements) efficiently computable?

Regarding the enriched perspective, the following questions remain.

+ What conditions arise for control functors in compact closed categories?
+ Can this approach account for the special axiom of Frobenius structures?

Regarding compilation, there is also interesting engineering questions involving global phase.
In praticular, both control functions and generalized control allow for compositional reasoning about control statements.
Unfortunately, [this compositionality breaks](/preprints/iwqc2026.pdf) when circuits are considered modulo global phase.
It would be of interest to develop methods compositional reasoning about control statements modulo global phase.

---

#### Project material

+ [Early notes on rig categories and control](mscs2023.pdf) (2023).
+ [An abandoned preprint on enriched categorical methods](https://arxiv.org/abs/2501.12481) (2025).
+ [Slides on the challenge of finding a unified perspective](slides_f2025.pdf) (2025).
+ [A talk on generalized control in quantum compilation (PLanQC)](https://www.youtube.com/watch?v=ZTgbHmMRikE) (2026).
+ [A poster on generalized control in quantum compilation (IWQC)](iwqc2026.pdf) (2026).

---

#### Related work

+ [[DP2025](https://arxiv.org/abs/2508.21756)] Introduces an algebraic theory of quantum control.
+ [[G2017](https://algassert.com/post/1706)] Relates quantum conditional statements to matrix exponentials.
+ [[HKL2025](https://arxiv.org/abs/2510.05032)] Relates quantum condition statements to rig categories.
+ [[HV2019](https://academic.oup.com/book/43710)] Chapter 5 (*Section 6*) relates quantum condition statements to modules.
+ [[S2024](https://arxiv.org/abs/2410.02946)] A preprint introducing hierarchical quantum circuits.
+ [[YVC2024](https://dl.acm.org/doi/10.1145/3649811)] Identifies limitations of quantum conditional statements.

---
