# RIVar

Welcome to the RIVarX organization! We are focused on the development and promotion of the innovative **RIVar concept**.
Given that this is an early exploration, some aspects might appear complex at this stage. We encourage interested individuals to ask questions and share their thoughts in the Discussions section.

## Brief Explanations

RIVar stands for a variable, built upon the established concept of calculated fields. Considering a formula like `Amount=Dose*Duration`, in which `Amount` is automatically computed based on the values of `Dose` and `Duration`. In using RIVar, the meaning of creating computed fields is reserved for only when the formula declares `Amount` firstly. We can then add a formula `Amount=Concentration*Volume`. This provides an extended meaning: adding a *filling option*, or adding an *indirect input option*.

The current provided implementation is that each variable is an *observable stream* from [RxJS](http://reactivex.io/rxjs). Also the assigned expressions for these variables are implemented as observable streams. The observable stream of a variable is created from merging the observable streams of the whole assigned expressions.

The presented characteristic is resulted from a distinctive approach of combining Functional Reactive Programming (FRP) with Object Oriented Programming (OOP). The name RIVar stands for *Reactive Instance Variable*: a combination  of *Reactive Variable* from FRP with *Instance Variable* (i.e., object's variable) from OOP.  It aims to integrate automatic change propagation of FRP within principles of OOP.

For Hebrew readers, a [presentation](https://github.com/RIVarX/.github/blob/main/RIVar%20Presentation%20Short%20Heb.pdf) is available. You may comment on it here [link to Google Doc](https://docs.google.com/document/d/1Um2lwUbT-AtxXbXzZViVSG5CjEsD5gMGdnKKIl30T-4).

## Repositories
* **RIVar-Thesis**: The thesis source and its PDF output. [https://github.com/RIVarX/RIVar-Thesis]
* **rivarjs (JavaScript):** A JavaScript-based POC. [https://github.com/RIVarX/rivarjs]
* **RIVarCsharp (C#):** A C#-based POC. [https://github.com/RIVarX/RIVarCSharp]

## Usage Suggestions (Future/Needs Evaluation)
* Reduce code repetition
* Two-Way Binding
* Constraints Programming
* Support Cycles (No need for unidirectional data flow)
* Reduce the need for event programming
* Generate cascading dropdowns from many-to-many relationships
* "Complex forms in simple form"

## Need to add support
* Fine grained changes
* Default values
* DB persistence
* Transparent FRP
