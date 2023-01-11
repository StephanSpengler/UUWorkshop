---
layout: default
---

## Program

#### Javier Esparza

*Interactive proofs and BDDs*

<details>
  <summary>▶ Abstract</summary>
  IP=PSPACE is proved by exhibiting an interactive proof
  system for QBF, often called the SumCheck algorithm.
  SumCheck runs in polynomial time for Verifier, but in
  exponential time for Prover.

  Assume that Prover solves QBF instances using BDDs.
  (That is, given a QBF formula Ax1 Ex2 Ax3 .. Exn F,
  Prover constructs BDDs for F, Exn F, Ax(n-1) Exn F etc.)
  We give an implementation of SumCheck in which Prover runs
  in polynomial time **in the size of the BDDs**. In particular,
  a BDD-based QBF-solver can be easily instrumented so that
  it produces interactive certificates.

  More generally, we are implementing a BDD library that
  produces interactive proof certificates. I'll report on
  this work.
</details>

#### Radu Iosif

*Reasoning about Distributed Reconfigurable Systems*

Joint work with Emma Ahrens and Joost-Pieter Katoen (RWTH Aachen), Marius Bozga and Lucas Bueri (Verimag).

<details>
  <summary>▶ Abstract</summary>
  We present a Hoare-style calculus for formal reasoning about
  reconfiguration programs of distributed systems. Such programs create
  and delete processes and/or interactions (communication channels) while
  processes in the network communicate by handshaking. Our proof calculus uses a
  resource logic, in the spirit of Separation Logic, to give local specifications of reconfiguration
  actions. Parameterized distributed systems with an unbounded number of
  processes are described using inductively defined predicates. The
  correctness of reconfiguration programs relies on havoc invariants,
  that are assertions about the ongoing interactions in a part of the
  system that is not affected by the structural change caused by the
  reconfiguration. The rest of the talk is concerned with automation issues,
  with a survey of the decision procedures (satisfiability, entailment) for the logic
  and the presentation of a method that proves havoc invariants automatically.
  The latter is inspired by Regular Model Checking, a domain of verification
  pioneered by Ahmed Bouajjani.
</details>

#### Roland Meyer

*A Concurrent Program Logic with a Future and History*

Joint work with Sebastian Wolff (NYU) and Thomas Wies (NYU).

<details>
  <summary>▶ Abstract</summary>
Verifying fine-grained optimistic concurrent programs remains an open problem. Modern program logics provide abstraction mechanisms and compositional reasoning principles to deal with the inherent complexity. However, their use is mostly confined to pencil-and-paper or mechanized proofs. We devise a new separation logic geared towards the lacking automation. While local reasoning is known to be crucial for automation, we are the first to show how to retain this locality for (i) reasoning about inductive properties without the need for ghost code, and (ii) reasoning about computation histories in hindsight. We implemented our new logic in a tool and used it to automatically verify challenging concurrent search structures that require inductive properties and hindsight reasoning, such as the Harris set.
</details>

#### Constantin Enea

*Reasoning About Consistency of Storage Systems and Applications.*

<details>
  <summary>▶ Abstract</summary>
  Modern applications such as e-commerce platforms are centered around using large-scale storage systems for storing and retrieving data. In the presence of concurrent accesses, these storage systems trade off consistency for performance. The weaker the consistency level, the more behaviors a storage system is allowed to exhibit and it is up to the developer to ensure that their application can tolerate those behaviors. However, these weak behaviors only occur rarely in practice and outside the control of the application, making it difficult for developers to check the robustness of their code against weak consistency levels.

  In this talk I will give an overview of algorithmic methods for checking whether a storage system conforms to a certain consistency level or that an application satisfies its intended specification when run under a given consistency level.
</details>

#### Tomas Vojnar

*Low-Level Bi-Abduction*

The paper was published at ECOOP’22, and it is a joint work with L. Holik, P. Peringer, A. Rogalewicz, and V. Sokova from FIT BUT and F. Zuleger from TU Vienna.

<details>
  <summary>▶ Abstract</summary>
  The paper proposes a new static analysis designed to handle open programs, i.e., fragments of programs, with dynamic pointer-linked data structures - in particular, various kinds of lists - that employ advanced low-level pointer operations. The goal is to allow such programs be analysed without a need of writing analysis harnesses that would first initialise the structures being handled. The approach builds on a special flavour of separation logic and the approach of bi-abduction. The code of interest is analyzed along the call tree, starting from its leaves, with each function analysed just once without any call context, leading to a set of contracts summarizing the behaviour of the analysed functions. In order to handle the considered programs, methods of abduction existing in the literature are significantly modified and extended in the paper. The proposed approach has been implemented in a tool prototype and successfully evaluated on not large but complex programs.
</details>

#### Lukas Holik

*Counting in Regexes Considered Harmful: Exposing ReDoS Vulnerability of Nonbacktracking Matchers*

The paper was published at USENIX Security’22, and it is a joint work with L. Turonova, I. Homoliak, O. Lengal, T. Vojnar from FIT BUT and M. Veanes from Microsoft Research Redmond.

<details>
  <summary>▶ Abstract</summary>
  In this paper, we study the performance characteristics of nonbacktracking regex matchers and their vulnerability against ReDoS (regular expression denial of service) attacks. We focus on their known Achilles heel, which are extended regexes that use bounded quantifiers (e.g., '(ab){100}'). We propose a method for generating input texts that can cause ReDoS attacks on these matchers. The method exploits the bounded repetition and uses it to force expensive simulations of the deterministic automaton for the regex. We perform an extensive experimental evaluation of our and other state-of-the-art ReDoS generators on a large set of practical regexes with a comprehensive set of backtracking and nonbacktracking matchers, as well as experiments where we demonstrate ReDoS attacks on state-of-the-art real-world security applications containing SNORT with Hyperscan and the HW-accelerated regex matching engine on the NVIDIA BlueField-2 card. Our experiments show that bounded repetition is indeed a notable weakness of nonbacktracking matchers, with our generator being the only one capable of significantly increasing their running time.
</details>

#### Markus Muller-Olm

*Logics for Asynchronous Hyperproperties*

<details>
  <summary>▶ Abstract</summary>
  Logics for Hyperproperties have received increasing attention in the last decade due to their importance e.g. for security analyses. Past approaches have focussed on synchronous properties, i.e. techniques in which different paths are explored lockstepwise. More recently automata models and logics supporting also asynchronous hyperproperties have been studied. In this talk I will survey recent research on logics for asynchronous hyperproperties.
</details>

#### Jean-Francois Raskin

*LTL Synthesis with a Few Hints*

(Mrudula Balachander, Emmanuel Filiot, and Jean-François Raskin)

<details>
  <summary>▶ Abstract</summary>
  We study a variant of the problem of synthesizing Mealy machines that enforce LTL specifications against a hostile environment. In the variant studied here, the user provides the high level LTL specification $\varphi$ of the system to design, and a set $E$ of examples of executions that the solution must produce. Our synthesis algorithm works in two phases. First, it generalizes the decisions taken along the examples $E$ using tailored extensions of automata learning algorithms. This phase generalizes the user-provided examples in $E$ while preserving realizability of $\varphi$. Second, the algorithm turns the (usually) incomplete Mealy machine obtained by the learning phase into a complete Mealy machine that realizes $\varphi$. The examples are used to guide the synthesis procedure. We provide a completness result that shows that our procedure can learn any Mealy machine $M$ that realizes $\varphi$ with a small (polynomial) set of examples. We also show that our problem, that generalizes the classical LTL synthesis problem (i.e. when $E=\emptyset$), matches its worst-case complexity. The additional cost of learning from $E$ is even polynomial in the size of $E$ and in the size of a symbolic representation of solutions that realize $\varphi$. This symbolic representation is computed by the synthesis algorithm implemented in {\sc Acacia-Bonzai} when solving the plain LTL synthesis problem. We illustrate the practical interest of our approach on a set of examples.
</details>

#### Rupak Majumdar

*Recent Results in Context-Bounded Exploration*

<details>
  <summary>▶ Abstract</summary>
  Context-bounded exploration is a way to structure the state space of a concurrent multithreaded program by restricting the number of times a thread can be context switched. Since its introduction by Qadeer and Rehof about two decades ago, it has led to many new and interesting results, both theoretical and practical.
  I will survey some recent results in the theory of context-bounded exploration. Our model and results are inspired by a seminal paper of Atig, Bouajjani, and Qadeer from 2009.
</details>

#### Tayssir Toulil

*On static malware detection*

<details>
  <summary>▶ Abstract</summary>
  The number of malware is growing extraordinarily fast. A  malware may
bring
serious damage. Thus, it is crucial to have efficient up-to-date virus
detectors.
Existing antivirus systems  use various detection techniques to identify
viruses
such as (1) code emulation where the virus is executed in a virtual
environment
to get detected; or (2) signature detection, where a signature is a
pattern of program
code that characterizes  the virus. A file is declared as a virus  if it
contains a
sequence of binary code instructions that matches  one  of the known
signatures.
These techniques are becoming insufficient. Indeed, emulation based
techniques
can only check the program's behavior in a limited time interval.  As
for signature
based systems, it is very easy to virus developers to  get around them.
Thus, a robust malware detection technique needs  to check the behavior
(not the syntax)
of the program without executing it.
We show in this talk how using behavior  signatures allow to efficiently
detect malwares
in a completely static way. We implemented our techniques in a tool, and
we applied
it to detect several viruses. Our results are encouraging. In
particular, our tool
 was able to detect more than 800 viruses. Several of these viruses
could not be
detected by well-known anti-viruses such as Avira, Avast, Norton,
Kaspersky and McAfee.
</details>

#### Ahmed Rezine

*Reachability in phaser programs*

<details>
  <summary>▶ Abstract</summary>
  We consider the problem of statically checking control state reachability (as in possibility of assertion violations, race conditions or runtime errors) and plain reachability (as in deadlock-freedom) of phaser programs. Phasers are a modern non-trivial synchronization construct that supports dynamic parallelism with runtime registration and deregistration of spawned tasks. They allow for collective and point-to-point synchronizations. For instance, phasers can enforce barriers or producer-consumer synchronization schemes among all or subsets of the running tasks. Implementations are found in modern languages such as Habanero Java. Phasers essentially associate phases to individual tasks and use their runtime values to restrict possible concurrent executions. Unbounded phases may result in infinite transition systems even in the case of programs only creating finite numbers of tasks and phasers.
</details>

#### Wang Yi

*MIMOS: from theory to tools for embedded software design & update*

<details>
  <summary>▶ Abstract</summary>
  Today, the functionality and economical value of industrial systems and products, such as cars, airplanes, and medical equipment, is deﬁned and realized by embedded software. Dynamic software updates are critical for new features, product customization and security patches, but presently are not well supported for safety-critical systems.  MIMOS is a tool environment providing a new design paradigm and software tools for building embedded software  which can be updated on demand dynamically, safely, and securely over their operational life-time. The talk will be concluded with a tool demo.
</details>

#### Faouzi Atig

*Flattening String Constraints*

This talk will be based on join work with Parosh Aziz Abdulla, Yu-Fang Chen, Bui Phi Diep, Julian Dolby, Lukas Holik, Denghang Hu, Petr Janku, Hsin-Hung Lin, Ahmed Rezine, Philipp Rümmer, Wei-Lun Tsai, Wei-Cheng Wu, Zhillin Wu and Di-De Yen.

<details>
  <summary>▶ Abstract</summary>
  String data type is present in all modern programming and is a part of the core semantics of programming languages such as JavaScript and Python. The testing and verification of such programs require a decision procedure for string constraints. The types of constraints include: (1) equality constraints of the form t1 = t2 where t1 and t2 consist of a sequence of string variables and constants, (2) regular constraints of the form x 2 R where x is a string variable and R is a regular language, and (3) integer constraints which are linear arithmetic formulas over the length of the string variables. In this keynote talk, we will present our recent decision procedure for string constraints. We will focus on the decision procedure that uses the Counter-Example Guided Abstraction Refinement (CEGAR) framework which contains both an under- and an over-approximation module running in an alternating manner. The flow of information between these modules is used to increase their precision in an automatic manner.
</details>
