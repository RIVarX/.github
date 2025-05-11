# RIVar
**RIVar** stands for *Reactive Instance Variable*: a combination  of *Reactive Variable* from FRP (Functional Reactive Programming) with *Instance Variable* (i.e., object's variable) from OOP (Object Oriented Programming).  It aims to integrate automatic change propagation of FRP within principles of OOP.

For Hebrew readers, a **Hebrew presentation** is available [link to PDF](https://github.com/RIVarX/.github/blob/main/RIVar%20Presentation%20Short%20Heb.pdf). You may comment on it here [link to Google Doc](https://docs.google.com/document/d/1Um2lwUbT-AtxXbXzZViVSG5CjEsD5gMGdnKKIl30T-4).

## Core Concept
**RIVar** is built upon the established concept of calculated fields. Considering a formula like `Amount=Dose*Duration`, in which `Amount` is automatically computed based on the values of `Dose` and `Duration`. In using **RIVar**, the meaning of creating computed fields is reserved for when the formula declares `Amount` firstly. The extended meaning is of adding a *filling option*, or adding an *indirect input option*. Concretely, we can add a formula `Amount=Concentration*Volume` with the meaning that filling `Dose` and `Duration` is an *option added* to fill `Amount`.

## Internal Implementations
The current provided implementation is that each variable is an *observable stream* from [RxJS](http://reactivex.io/rxjs). Also the assigned expressions for these variables are implemented as observable streams. The observable stream of a variable is created from merging the observable streams of the whole assigned expressions.

## Repositories
* **RIVar-Thesis**: The thesis source and its PDF output
* **rivarjs**: An implementation in JavaScript
* **RIVarCSharp**: An implementation in C#

## Usage Suggestions (Future/Needs Evaluation)
* Reduce code repetition
* Two-Way Binding
* Constraints Programming
* Support Cycles (No need for unidirectional data flow)
* Reduce the need for event programming
* Generate cascading dropdowns from many-to-many relationships
* "Complex forms in simple form"
*  [Support redandancy](https://docs.google.com/document/d/e/2PACX-1vQZizHpNh3RJpGnGctksGZcdIg9Oq9KQbprNT1lgHnquucBGROVJ1WAoZOWyZm1l1mwM0KYrdFFLCxr/pub)

## Future Research
* Fine grained changes
* Default values
* DB persistence
* Transparent FRP
