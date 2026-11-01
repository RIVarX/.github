# Redundancy is a feature, not a bug — in noisy, agent-based (not only) communication.

> Modular reactive architectures for multi-way dataflow, consistency enforcement, and error-correcting runtimes.

---

## Overview: From Modularity to Noisy Channels

Welcome to the **RIVarX** organization, dedicated to the research and development of the **RIVar** (*Reactive Instance Variable*) computational model.

The original motivation behind RIVar is **software modularity**. Traditional Functional Reactive Programming (FRP) and dataflow architectures enforce strict Directed Acyclic Graphs (DAGs) and a Single Source of Truth (SSOT). While a DAG simplifies change propagation, it creates a fundamental tension between the **software architect** (who guards global consistency) and the **developer** (who needs local modular freedom). Because real-world domain logic is naturally cyclic and interdependent, banning cycles forces developers into manual event wiring, duplicated dependency graphs, or centralized constraint solvers that break Object-Oriented Programming (OOP) encapsulation.

RIVar resolves this tension by combining **FRP** with **OOP**, introducing a decentralized semantic model where cyclic dependencies and overlapping variable definitions are natively supported and deterministically resolved.

### The Next Horizon: Noisy Human & Agent Interaction
While the core model was designed to enable modular composition across decoupled software components, its ability to reconcile overlapping definitions opens a new research direction: **managing noisy communication channels**. 

Whether inputs originate from human practitioners working across different cognitive perspectives or from non-deterministic AI agents (LLMs), real-world interaction frequently involves partial, redundant, or conflicting specifications. Instead of prohibiting redundancy to satisfy DRY/SSOT, a reactive runtime can leverage overlapping specifications as an **error-correcting protocol** (analogous to parity checks in information theory).

---

* **Published Paper:** *Escaping the DAG Dogma: Toward Modular Reactive Architectures* (Rivka Altshuler and David H. Lorenz) — **ACM SIGPLAN SPLASH / Onward! '26**.
  * 📄 [Paper on ACM DL](https://doi.org/10.1145/3840586.3843206) | [Thesis & Sources (`RIVar-Thesis`)](https://github.com/RIVarX/RIVar-Thesis)
  * 🎥 Conference Presentation & Slides: [Recording](https://drive.google.com/file/d/1dZgsepp8xugbNl_sbTTKpRyABWWo1tz8/view?usp=drive_link) | [Slides](https://docs.google.com/presentation/d/1DR_ft8YXT_pJn4ALrHHPLbmFAMFiNcgIMFNQt3FGytA)
  * 🇮🇱 For Hebrew readers: [Short Presentation (PDF)](https://github.com/RIVarX/.github/blob/main/RIVar%20Presentation%20Short%20Heb.pdf) | [Comments & Feedback (Google Doc)](https://docs.google.com/document/d/1Um2lwUbT-AtxXbXzZViVSG5CjEsD5gMGdnKKIl30T-4)

> **Project Scope:** The core reactive OOP architecture, constructive assignment semantics, and provenance-based propagation algorithm are published and implemented in our proof-of-concept libraries. Extending the runtime into an active error-correcting protocol for noisy human/LLM interaction (and more) is an ongoing research direction.

---

## Brief: The Computational Model


RIVar redefines how state variables are declared, linked, and evaluated across three layers:

### 1. Constructive Assignment

- **Multiple Active Assignments**  
  Variables can have several active assignments simultaneously.
  ```text
  Amount := Concentration * Volume
  Amount := Dose * Duration
  ```

- **Mutual Recursions (Cycles)**  
  Circular dependencies and mutual recursions between variables are fully supported.
  ```text
  Amount := Concentration * Volume
  Volume := Amount / Concentration
  ```

### 2. Stream Merge

Variables and expressions act as streams of values. The constructive assignment handles a stream merge operation by subscribing to the expressions streams and propagating updates to the target variables. This produces the classic merge operation over streams.

### 3. Conflict Resolution / Merge Strategies

The behavior for detecting and handling conflicts can be plugged in and executed locally by the variable.

---

## Repositories

* **[rivarjs](https://github.com/RIVarX/rivarjs) (JavaScript):** A lightweight JavaScript-based proof of concept built on RxJS, including the clinical drug-administration prototype and HotDrink comparison.
* **[rivarts](https://github.com/RIVarX/rivarts) (TypeScript):** Fully typed TypeScript implementation of the RIVar reactive runtime engine and samples.
* **[RIVarCSharp](https://github.com/RIVarX/RIVarCSharp) (C#):** A C#-based core runtime engine.
---

## Discussions & Collaboration

We welcome questions, critiques, and research collaborations. If you are exploring **reactive architectures, language engineering (DSLs), multi-way dataflow, or reliable human/agent interaction protocols**, please start a conversation in the **[Discussions section](https://github.com/RIVarX/.github/discussions)**.
