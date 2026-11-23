---
title: 'LinguaQuanta: A Quantum Circuit Transpiler'
tags: ["quantum computing","source-to-source translation","quantum circuits","pipeline architecture","categorical specifications"]
description: "LinguaQuanta is a collection of libraries, tools, and scripts to translate logical quantum circuits between Quipper and various subsets of the OpenQASM family of languages."
summary: "LinguaQuanta is a collection of libraries, tools, and scripts to translate logical quantum circuits between Quipper and various subsets of the OpenQASM family of languages."
startYear: 2023
hideAuthor: true
cover:
    image: "placeholder.jpg"
---

---

#### Contributors:

+ Scott Wesley :cat:
+ Xiaoning Bian (Tsinghua University)
+ Christopher Dean (Alice and Bob)
+ Peter Selinger (Dalhousie University)
+ Simon Tsang (Peraton Labs)

---

#### Project overview

As quantum computing evolves, many important engineering questions emerge, such as how best to represent quantum programs, and how to promote interoperability between quantum program analysis tools.
These questions arise naturally in the design of quantum transpilers, which translate between quantum programming languages.
This project aims to better understand these questions through hands-on design and implementation within the LinguaQuanta framework.

LinguaQuanta is a collection of libraries, tools, and scripts to translate logical quantum circuits between the [Quipper](https://www.mathstat.dal.ca/~selinger/quipper/) programming language and various subsets of the [OpenQASM](https://openqasm.com/versions/3.0/intro.html) family of languages.
The design of each module within LinguaQuanta is informed by the [UNIX philosophy](https://en.wikipedia.org/wiki/Unix_philosophy).
Each translation is designed to be "well-behaved", insofar that all round-translations are idempotent operations.
Furthermore, each parser in the LinguaQuanta library is a categorical retraction to its corresponding code generator.
Formally, a program $f: X \rightarrow Y$ is a retraction to a program $g: Y \rightarrow Z$ if $f \circ g = 1_Y$.
In practice this means that using the output from one LinguaQuanta tool as the input to a another LinguaQuanta tool is equivalent to writing a new LinguaQuanta tool which composes the functionality of the first tool with the functionality of the second tool.
In this way LinguaQuanta provides a family of flexible tools, that provide reasonable guarantees on their outputs.

---


#### Publications and preprints

+ [[S2024](/papers/rc2024/)]: Describes the core philosophy, design, and features of LinguaQuanta.
+ [[LDWB2024](https://arxiv.org/pdf/2311.10686)]: A resource estimation pipeline using LinguaQuanta as a transpiler.

---

#### Future work

The following language features are not yet supported in LinguaQuanta.

- Hierarchically defined unitary gates from OpenQASM 3.
- Opaque unitary gates.
- Support for bounded loops via loop unrolling.
- Classical control from Quipper.
- Classical computation from OpenQASM 3.

The following features are planned but not yet implemented in LinguaQuanta.

- Constant propagation to support more programs.
- Power modifier simplification (e.g., handling gates of finite order).

We would also like to further explore the design of programming tools with categorical semantics.
In particular, we are interested in the following questions.

- How should idempotent operations compose with retracts?
- What specifications should endomorphic tools (pre/post-processing) satisfy?
- Can we characterize the failure for round translations to compose to the identity function using posetal categories and Galois connections?

On the more practical side, we would like to verify the preservation and fluency of our categorical semantics, as defined in [S2024].
We would also like to explore the potential for white-box fuzzing in pipeline design with categorical semantics.

---

#### Project material

+ [Codebase for LinguaQuanta](https://github.com/onestruggler/qasm-quipper).
+ [Presentation slides for the initial proposal of LinguaQuanta](iwqc2023.pdf) (2023).
+ [Presentation slides accompanying the LinguaQuanta paper](/paper/rc2024/slides.pdf) (2024).

---

#### Related work

+ [[CJABBHRSSGJ2021](https://arxiv.org/pdf/2104.14722)]: The design paper for OpenQASM 3.
+ [[CVPPPG2025](https://link.springer.com/article/10.1007/s11227-024-06892-2)]: A survey of quantum intermediate representations.
+ [[GK2008](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/tr-2007-154.pdf)]: An introduction to white-box fuzzing.
+ [[GLRSV2013](https://arxiv.org/pdf/1304.3390)]: The design paper for Quipper.
+ [[M1989](https://www.cs.tufts.edu/comp/150FP/archive/bill-mckeeman/DifferentailTesting.pdf)] An introduction to differential testing.

---
