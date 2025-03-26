# RIVar

## Background
**RIVar** stands for *Reactive Instance Variable*: a combination  of *Reactive Variable* from FRP (Functional Reactive Programming) with *Instance Variable* (i.e., object's variable) from OOP (Object Oriented Programming).  It aims to integrate automatic change propagation of FRP within principles of OOP.

## Core Concept
**RIVar** is built upon the established concept of calculated fields. Considering a formula like `Amount=Dose*Duration`, in which `Amount` is automatically computed based on the values of `Dose` and `Duration`. In using **RIVar**, the meaning of creating computed fields is reserved for when the formula declares `Amount` firstly. The extended meaning is of adding a *filling option*, or adding an *indirect input option*. Concretely, we can add a formula `Amount=Concentration*Volume` with the meaning that filling `Dose` and `Duration` is an *option added* to fill `Amount`.

## Internal Implementations
The current provided implementation is that each variable is an *observable stream* from [RxJS](http://reactivex.io/rxjs). Also the assigned expressions for these variables are implemented as observable streams. The observable stream of a variable is created from merging the observable streams of the whole assigned expressions.

## Evaluation (Current)
* Reduce code repetition.

## Usage Suggestions (Future)
* Two-Way Binding.
* Support Cycles (No need for unidirectional data flow).
* Constraints Programming.
* Reduce need for event programming (and coupling).
* Complex forms in simple form.
