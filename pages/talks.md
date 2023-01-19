---
layout: default
---

## Titles and Abstracts

---

#### Ahmed Bouajjani

(Mon 09:00--09:40)

*TBD*

---

#### Javier Esparza

(Mon 09:40--10:20)

*Interactive proofs and BDDs*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
IP=PSPACE is proved by exhibiting an interactive proof
system for QBF, often called the SumCheck algorithm.
SumCheck runs in polynomial time for Verifier, but in
exponential time for Prover.

Assume that Prover solves QBF instances using BDDs.
(That is, given a QBF formula $$\forall x_1 \exists x_2 \forall x_3 \dots \exists x_n F$$,
Prover constructs BDDs for $$F$$, $$\exists x_n F$$, $$\forall x_{n-1} \exists x_n F$$ etc.)
We give an implementation of SumCheck in which Prover runs
in polynomial time *in the size of the BDDs*. In particular,
a BDD-based QBF-solver can be easily instrumented so that
it produces interactive certificates.

More generally, we are implementing a BDD library that
produces interactive proof certificates. I'll report on
this work.
</details>

---

#### Radu Iosif

(Mon 10:50--11:30)

*Reasoning about Distributed Reconfigurable Systems*

Joint work with Emma Ahrens and Joost-Pieter Katoen (RWTH Aachen), Marius Bozga and Lucas Bueri (Verimag).

<details markdown=1>
<summary markdown="span"> Abstract</summary>
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

---

#### Wang Yi

(Mon 11:30--12:10)

*MIMOS: from theory to tools for embedded software design & update*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Today, the functionality and economical value of industrial systems and products, such as cars, airplanes, and medical equipment, is deﬁned and realized by embedded software. Dynamic software updates are critical for new features, product customization and security patches, but presently are not well supported for safety-critical systems. MIMOS is a tool environment providing a new design paradigm and software tools for building embedded software which can be updated on demand dynamically, safely, and securely over their operational life-time. The talk will be concluded with a tool demo.
</details>

---

#### Constantin Enea

(Mon 13:40--14:20)

*Using Concurrent Objects in Randomized Programs*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Atomic concurrent objects, whose operations take place instantaneously, are a powerful technique for designing complex concurrent programs. Since they are not always available, they are typically substituted with software implementations. A prominent condition relating these implementations to their atomic specifications is linearizability, which preserves safety properties of programs using them. However linearizability does not preserve hyper-properties, which include probabilistic guarantees about randomized programs. A more restrictive property, strong linearizability, does preserve hyper-properties but it is impossible to achieve in many situations. In particular, we show that there are no strongly linearizable implementations of multi-writer registers or snapshot objects in message-passing systems. On the other hand, we show that a wide class of linearizable implementations, including well-known ones for registers and snapshots, can be modified to approximate the probabilistic guarantees of randomized programs when using atomic objects. This is joint work with Hagit Attiya and Jennifer Welch.
</details>

---

#### Shaz Qadeer

(Mon 14:20--15:00)

*Reasoning with permissions using linear types and first-order logic*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Local reasoning is achieved when the specification of the effects of a code fragment can be used to reason effectively in any context where those effects are relevant. Local reasoning is essential for framing of loops and calls in sequential code and for noninterference reasoning in concurrent code.

The Civl approach to local reasoning combines two independent reasoning systems -- types and logic. Like many other verifiers (EscJava, Dafny, Viper, VeriFast, and Ivy to name a few), Civl uses a satisfiability solver for logical reasoning. In addition to the usual types whose values may be freely duplicated, Civl also provides linear types whose values may not be duplicated.

Civl enables local reasoning via programmable ownership expressed using permissions that must be held to perform critical operations that mutate state. Permissions are linearly-typed sets in Civl that may be split and joined but not duplicated. The Civl type system guarantees that at runtime permissions residing in distinct variables are disjoint. The verification condition generator in Civl soundly injects such disjointness facts as assumptions into the verification conditions of the program.

In this talk, I will motivate the need for permissions and illustrate their benefits. I hope to convince the audience that permissions are indispensable for tractable and automated local proofs.
</details>

---

#### Roland Meyer

(Mon 15:40--16:20)

*A Concurrent Program Logic with a Future and History*

Joint work with Sebastian Wolff (NYU) and Thomas Wies (NYU).

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Verifying fine-grained optimistic concurrent programs remains an open problem. Modern program logics provide abstraction mechanisms and compositional reasoning principles to deal with the inherent complexity. However, their use is mostly confined to pencil-and-paper or mechanized proofs. We devise a new separation logic geared towards the lacking automation. While local reasoning is known to be crucial for automation, we are the first to show how to retain this locality for (i) reasoning about inductive properties without the need for ghost code, and (ii) reasoning about computation histories in hindsight. We implemented our new logic in a tool and used it to automatically verify challenging concurrent search structures that require inductive properties and hindsight reasoning, such as the Harris set.
</details>

---

#### Markus Müller-Olm

(Mon 16:20--17:00)

*Logics for Asynchronous Hyperproperties*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Logics for Hyperproperties have received increasing attention in the last decade due to their importance e.g. for security analyses. Past approaches have focussed on synchronous properties, i.e. techniques in which different paths are explored lockstepwise. More recently automata models and logics supporting also asynchronous hyperproperties have been studied. In this talk I will survey recent research on logics for asynchronous hyperproperties.
</details>

---

#### Kostis Sagonas

(Tue 09:00--09:40)

*Awaiting for Godot: Stateless Model Checking that Avoids Executions where Nothing Happens*

This is joint work with Bengt Jonsson and Magnus Lång. It has been published at FMCAD 2022.

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Stateless Model Checking (SMC) is a verification technique for concurrent programs that checks for safety violations by exploring all possible thread schedulings. It is highly effective when coupled with Dynamic Partial Order Reduction (DPOR), which introduces an equivalence on schedulings and need explore only one in each equivalence class. Even with DPOR, SMC often spends unnecessary effort in exploring loop iterations that are pure, i.e., have no effect on the program state.

We present techniques for making SMC with DPOR more effective on programs with pure loop iterations. The first is a static program analysis to detect loop purity and an associated program transformation, called Partial Loop Purity Elimination, that inserts assume statements to block pure loop iterations. Subsequently, some of these assumes are turned into await statements that completely remove many assume-blocked executions. Finally, we present an extension of the standard DPOR equivalence, obtained by weakening the conflict relation between events. All these techniques are incorporated into a new DPOR algorithm, Optimal-DPOR-Await, which can handle both awaits and the weaker conflict relation, is optimal in the sense that it explores exactly one execution in each equivalence class, and can also diagnose livelocks. Our implementation in Nidhugg shows that these techniques can significantly speed up the analysis of concurrent programs that are currently challenging for SMC tools, both for exploring their complete set of interleavings, but even for detecting concurrency errors in them.
</details>

---

#### Rupak Majumdar

(Tue 09:40--10:20)

*Recent Results in Context-Bounded Exploration*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Context-bounded exploration is a way to structure the state space of a concurrent multithreaded program by restricting the number of times a thread can be context switched. Since its introduction by Qadeer and Rehof about two decades ago, it has led to many new and interesting results, both theoretical and practical.
I will survey some recent results in the theory of context-bounded exploration. Our model and results are inspired by a seminal paper of Atig, Bouajjani, and Qadeer from 2009.
</details>

---

#### Tayssir Touili

(Tue 10:50--11:30)

*On static malware detection*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
 The number of malware is growing extraordinarily fast. A malware may bring serious damage. Thus, it is crucial to have efficient up-to-date virus detectors. Existing antivirus systems use various detection techniques to identify viruses such as (1) code emulation where the virus is executed in a virtual environment to get detected; or (2) signature detection, where a signature is a pattern of program code that characterizes the virus. A file is declared as a virus if it contains a sequence of binary code instructions that matches one of the knownsignatures.These techniques are becoming insufficient. Indeed, emulation basedtechniquescan only check the program's behavior in a limited time interval. Asfor signaturebased systems, it is very easy to virus developers to get around them.Thus, a robust malware detection technique needs to check the behavior (not the syntax) of the program without executing it.We show in this talk how using behavior signatures allow to efficientlydetect malwaresin a completely static way. We implemented our techniques in a tool, andwe appliedit to detect several viruses. Our results are encouraging. Inparticular, our tool was able to detect more than 800 viruses. Several of these virusescould not bedetected by well-known anti-viruses such as Avira, Avast, Norton,Kaspersky and McAfee.
</details>

---

#### Ahmed Rezine

(Tue 11:30--12:10)

*Reachability in phaser programs*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
We consider the problem of statically checking control state reachability (as in possibility of assertion violations, race conditions or runtime errors) and plain reachability (as in deadlock-freedom) of phaser programs. Phasers are a modern non-trivial synchronization construct that supports dynamic parallelism with runtime registration and deregistration of spawned tasks. They allow for collective and point-to-point synchronizations. For instance, phasers can enforce barriers or producer-consumer synchronization schemes among all or subsets of the running tasks. Implementations are found in modern languages such as Habanero Java. Phasers essentially associate phases to individual tasks and use their runtime values to restrict possible concurrent executions. Unbounded phases may result in infinite transition systems even in the case of programs only creating finite numbers of tasks and phasers.
</details>

---

#### Tomás Vojnar

(Tue 13:40--14:20)

*Low-Level Bi-Abduction*

The paper was published at ECOOP’22, and it is a joint work with L. Holík, P. Peringer, A. Rogalewicz, and V. Soková from FIT BUT and F. Zuleger from TU Vienna.

<details markdown=1>
<summary markdown="span"> Abstract</summary>
The paper proposes a new static analysis designed to handle open programs, i.e., fragments of programs, with dynamic pointer-linked data structures - in particular, various kinds of lists - that employ advanced low-level pointer operations. The goal is to allow such programs be analysed without a need of writing analysis harnesses that would first initialise the structures being handled. The approach builds on a special flavour of separation logic and the approach of bi-abduction. The code of interest is analyzed along the call tree, starting from its leaves, with each function analysed just once without any call context, leading to a set of contracts summarizing the behaviour of the analysed functions. In order to handle the considered programs, methods of abduction existing in the literature are significantly modified and extended in the paper. The proposed approach has been implemented in a tool prototype and successfully evaluated on not large but complex programs.
</details>

---

#### Faouzi Atig

(Tue 14:20--15:00)

*Flattening String Constraints*

This talk will be based on joint work with Parosh Aziz Abdulla, Yu-Fang Chen, Bui Phi Diep, Julian Dolby, Lukás Holík, Denghang Hu, Petr Janku, Hsin-Hung Lin, Ahmed Rezine, Philipp Rümmer, Wei-Lun Tsai, Wei-Cheng Wu, Zhillin Wu and Di-De Yen.

<details markdown=1>
<summary markdown="span"> Abstract</summary>
String data type is present in all modern programming and is a part of the core semantics of programming languages such as JavaScript and Python. The testing and verification of such programs require a decision procedure for string constraints. The types of constraints include: (1) equality constraints of the form $$t_1 = t_2$$ where $$t_1$$ and $$t_2$$ consist of a sequence of string variables and constants, (2) regular constraints of the form $$x \in R$$ where $$x$$ is a string variable and $$R$$ is a regular language, and (3) integer constraints which are linear arithmetic formulas over the length of the string variables. In this keynote talk, we will present our recent decision procedure for string constraints. We will focus on the decision procedure that uses the Counter-Example Guided Abstraction Refinement (CEGAR) framework which contains both an under- and an over-approximation module running in an alternating manner. The flow of information between these modules is used to increase their precision in an automatic manner.
</details>

---

#### Eugene Asarin

(Tue 15:40--16:20)

*Timed pattern-matching*

This talk will be based on a series of joint works with O. Maler, D. Ulus, Th. Ferrère, D. Nickovic and A. Bakhirkin.

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Timed pattern matching consists in finding occurrences of a timed regular expression in a timed word. I will present a simple (and visual) algorithm, and discuss applications to runtime verification/log analysis. On the theoretical side I will address the complexity of the problem depending on the kind of expressions used, and present a couple of open questions.
</details>

---

#### Lukás Holík

(Tue 16:20--17:00)

*Counting in Regexes Considered Harmful: Exposing ReDoS Vulnerability of Nonbacktracking Matchers*

The paper was published at USENIX Security’22, and it is a joint work with L. Turonová, I. Homoliak, O. Lengál, T. Vojnar from FIT BUT and M. Veanes from Microsoft Research Redmond.

<details markdown=1>
<summary markdown="span"> Abstract</summary>
In this paper, we study the performance characteristics of nonbacktracking regex matchers and their vulnerability against ReDoS (regular expression denial of service) attacks. We focus on their known Achilles heel, which are extended regexes that use bounded quantifiers (e.g., '(ab){100}'). We propose a method for generating input texts that can cause ReDoS attacks on these matchers. The method exploits the bounded repetition and uses it to force expensive simulations of the deterministic automaton for the regex. We perform an extensive experimental evaluation of our and other state-of-the-art ReDoS generators on a large set of practical regexes with a comprehensive set of backtracking and nonbacktracking matchers, as well as experiments where we demonstrate ReDoS attacks on state-of-the-art real-world security applications containing SNORT with Hyperscan and the HW-accelerated regex matching engine on the NVIDIA BlueField-2 card. Our experiments show that bounded repetition is indeed a notable weakness of nonbacktracking matchers, with our generator being the only one capable of significantly increasing their running time.
</details>

---

#### Jean-François Raskin

(Wed 09:00--09:40)

*LTL Synthesis with a Few Hints*

Joint work with Mrudula Balachander and Emmanuel Filiot.

<details markdown=1>
<summary markdown="span"> Abstract</summary>
We study a variant of the problem of synthesizing Mealy machines that enforce LTL specifications against a hostile environment. In the variant studied here, the user provides the high level LTL specification $$\varphi$$ of the system to design, and a set $$E$$ of examples of executions that the solution must produce. Our synthesis algorithm works in two phases. First, it generalizes the decisions taken along the examples $$E$$ using tailored extensions of automata learning algorithms. This phase generalizes the user-provided examples in $$E$$ while preserving realizability of $$\varphi$$. Second, the algorithm turns the (usually) incomplete Mealy machine obtained by the learning phase into a complete Mealy machine that realizes $$\varphi$$. The examples are used to guide the synthesis procedure. We provide a completness result that shows that our procedure can learn any Mealy machine $$M$$ that realizes $$\varphi$$ with a small (polynomial) set of examples. We also show that our problem, that generalizes the classical LTL synthesis problem (i.e. when $$E=\emptyset$$), matches its worst-case complexity. The additional cost of learning from $$E$$ is even polynomial in the size of $$E$$ and in the size of a symbolic representation of solutions that realize $$\varphi$$. This symbolic representation is computed by the synthesis algorithm implemented in {\sc Acacia-Bonzai} when solving the plain LTL synthesis problem. We illustrate the practical interest of our approach on a set of examples.
</details>

---

#### Cezara Dragoi

(Wed 09:40--10:20)

*Reasoning about State Machine Replication*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
State machine replication protocols are the default mechanism for fault-tolerance in distributed systems. These are asynchronous systems where processes communicate by message passing, where messages may be dropped or delayed, or may processes crashing. Asynchrony and faults make these protocols tricky to reason about and therefore implementations buggy. In this talk we will look into alternatives more simple ways, to reason and develop these systems, inspired from the world of synchronous protocols. The talk presents a formalisation of the relation between synchronous and asynchronous fault-tolerant systems and it’s application in verification and execution environments.
</details>

---

#### Paul Fiterau-Brostean

(Wed 10:50--11:30)

*Automata-Based Automated Detection of State Machine Bugs in Protocol Implementations*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Model Learning (aka Automata learning) is an established class of techniques for inferring automata or mealy-machine models of a software component's input-output behavior by observing how it responds to a sample of input sequences.

For testing of communication protocols, model learning has proven effective in finding so-called *state machine bugs*, i.e., flaws in the implementation of a protocol's control logic that, e.g., permits to bypass authentication steps or establish insecure connections.
Model learning is used to automatically infer a state machine description of a protocol implementation.
The Mealy machine can then be analyzed to spot flaws in the implementation's control logic or check compliance with its specification.
We present a technique which automates the detection of bugs in learned protocol models.
It takes as input a catalogue of state machine bugs for the protocol, each specified as a finite automaton which accepts
sequences of messages that exhibit the bug. By adapting model checking techniques,
our technique constructs the set of sequences that (according to the model) can be performed by the implementation and
that (according to the automaton) expose the bug.
These sequences are then transformed to test cases on the actual implementation to find a witness for the bug or filter out false alarms.
We have applied our technique on widely-used implementations of security protocols: SSH and DTLS.
</details>

---

#### Bengt Jonsson

(Wed 11:30--12:10)

*Model Learning for Automata Models with Data*

<details markdown=1>
<summary markdown="span"> Abstract</summary>
Model Learning (aka Automata learning) is an established class of techniques for inferring automata or mealy-machine models of a software component's input-output behavior by observing how it responds to a sample of input sequences.

The previous approach used automata learning to learn finite state machine models of protocols. However, in many situations it is crucial for models to also be able to describe data flow, i.e., constraints on data parameters that are passed when the component interacts with its environment, as well as the mutual influence between control flow and data flow.
We present an extension of model learning algorithm for register automata, a class of finite state machines extended with data. Our algorithm is parameterized on a particular theory, i.e., a set of operations and tests on the data domain that can be used in guards.
Our algorithm is based on a generalization of the classical Nerode equivalence and canonical automata construction to the symbolic setting.
</details>
