# RIVar Ecosystem

Welcome to the RIVarX organization! This space hosts the foundational repositories, reference implementations, and proofs-of-concept for the **RIVar (Reactive Instance Variable)** concept.

---

## 📄 Published Research

- **Published Paper:** *Escaping the DAG Dogma: Toward Modular Reactive Architectures* (Rivka Altshuler and David H. Lorenz) — **ACM SIGPLAN SPLASH / Onward! '26**.
  * 📄 [Paper on ACM DL](https://doi.org/10.1145/3840586.3843206) | [Thesis & Sources (`RIVar-Thesis`)](https://github.com/RIVarX/RIVar-Thesis)
  * 🎥 Conference Presentation & Slides: [Recording](https://drive.google.com/file/d/1dZgsepp8xugbNl_sbTTKpRyABWWo1tz8/view?usp=drive_link) | [Slides](https://docs.google.com/presentation/d/1DR_ft8YXT_pJn4ALrHHPLbmFAMFiNcgIMFNQt3FGytA)
  * 🇮🇱 For Hebrew readers: [Short Presentation (PDF)](https://github.com/RIVarX/.github/blob/main/RIVar%20Presentation%20Short%20Heb.pdf) | [Comments & Feedback (Google Doc)](https://docs.google.com/document/d/1Um2lwUbT-AtxXbXzZViVSG5CjEsD5gMGdnKKIl30T-4)

---

## 💡 Brief Explanations

RIVar stands for a variable, built upon the established concept of calculated fields. Considering a formula like `Amount=Dose*Duration`, in which `Amount` is automatically computed based on the values of `Dose` and `Duration`. In using RIVar, the meaning of creating computed fields is reserved for only when the formula declares `Amount` firstly, and allows adding another formula `Amount=Concentration*Volume`. This provides an extended meaning: adding a *filling option*, or adding an *indirect input option*.

This characteristic is a result of a distinctive approach of combining Functional Reactive Programming (FRP) with Object Oriented Programming (OOP). The name RIVar stands for *Reactive Instance Variable*: a combination of *Reactive Variable* from FRP with *Instance Variable* (i.e., object's variable) from OOP. It aims to integrate automatic change propagation of FRP within principles of OOP.

---

## 📦 Repositories

- **[rivarjs](https://github.com/RIVarX/rivarjs) (JavaScript):** A lightweight JavaScript-based proof of concept built on RxJS, including the clinical drug-administration prototype and HotDrink comparison.
- **[rivarts](https://github.com/RIVarX/rivarts) (TypeScript):** Fully typed TypeScript implementation of the RIVar reactive runtime engine and samples.
- **[RIVarCSharp](https://github.com/RIVarX/RIVarCSharp) (C#):** A C#-based core runtime engine.

---

## 💬 Get in Touch & Collaboration

Given that this is an ongoing research and exploration, I would love to hear from researchers, developers, and anyone interested in architectural patterns, reactive programming, or potential workshops and collaborations. 

Feel free to reach out directly via email: **[brandrivka@gmail.com](mailto:brandrivka@gmail.com)**
