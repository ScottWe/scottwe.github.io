---
title: "Inductive Predicate Synthesis Modulo Programs" 
date: 2024-09-12
tags: ["software verification","invariant synthesis","model-checking","compositionality","smart contracts"]
author: ["Scott Wesley","Maria Christakis","Jorge A. Navas","Richard Trefler","Valentin Wüstholz","Arie Gurfinkel"]
description: "This paper introduces IPS-MP to extend high-level languages with minimal synthesis features to guide analysis. IPS-MP is efficiently decidable in the Boolean case, and reduces to CHC-solving." 
summary: "This paper introduces IPS-MP to extend high-level languages with minimal synthesis features to guide analysis. IPS-MP is efficiently decidable in the Boolean case, and reduces to CHC-solving." 

---

---

##### Download

+ [Paper](https://arxiv.org/pdf/2407.08455)

---

##### Abstract

A growing trend in program analysis is to encode verification conditions within the language of the input program.
This simplifies the design of analysis tools by utilizing off-the-shelf verifiers, but makes communication with the underlying solver more challenging.
Essentially, the analyzer operates at the level of input programs, whereas the solver operates at the level of problem encodings.
To bridge this gap, the verifier must pass along proof-rules from the analyzer to the solver.
For example, an analyzer for concurrent programs built on an inductive program verifier might need to declare Owicki-Gries style proof-rules for the underlying solver.
Each such proof-rule further specifies how a program should be verified, meaning that the problem of passing proof-rules is a form of invariant synthesis.
 
Similarly, many program analysis tasks reduce to the synthesis of pure, loop-free Boolean functions (i.e., predicates), relative to a program.
From this observation, we propose Inductive Predicate Synthesis Modulo Programs (IPS-MP) which extends high-level languages with minimal synthesis features to guide analysis.
In IPS-MP, unknown predicates appear under assume and assert statements, acting as specifications modulo the program semantics.
Existing synthesis solvers are inefficient at IPS-MP as they target more general problems.
In this paper, we show that IPS-MP admits an efficient solution in the Boolean case, despite being generally undecidable.
Moreover, we show that IPS-MP reduces to the satisfiability of constrained Horn clauses, which is less general than existing synthesis problems, yet expressive enough to encode verification tasks.
We provide reductions from challenging verification tasks -- such as parameterized model checking -- to IPS-MP.
We realize these reductions with an efficient IPS-MP-solver based on SeaHorn, and describe a application to smart-contract verification.

---

##### Citation

```latex
@inproceedings{WCNTWG2024,
author    = {Scott Wesley and Maria Christakis and Jorge A. Navas and Richard Trefler and Valentin W\"{u}stholz and Arie Gurfinkel},
title     = {Inductive Predicate Synthesis Modulo Programs},
booktitle = {38th European Conference on Object-Oriented Programming (ECOOP 2024)},
year      = {2024},
publisher = {Schloss Dagstuhl -- Leibniz-Zentrum f{\"u}r Informatik},
doi       = {10.4230/LIPIcs.ECOOP.2024.43},
pages     = {43:1--43:30},
}
```

##### Related material

+ [Presentation slides](slides.pdf)
+ [Codebase](https://github.com/seahorn/seahorn)
