# RIVar

RIVar is built upon the established concept of calculated fields. Considering a formula like `Amount=Dose*Duration`, in which `Amount` is automatically computed based on the values of `Dose` and `Duration`. In using RIVar, the meaning of creating computed fields is reserved for when the formula declares `Amount` firstly. The extended meaning is of adding a *filling option*, or adding an *indirect input option*. Concretely, the formula `Amount=Concentration*Volume` means that filling `Dose` and `Duration` is an *option added* to fill `Amount`.

## Impact

* Two-Way Binding.
* Support Cycles (No need for unidirectional data flow).
* Constraints Programming.
* Reduce code repetition.
* Reduce need for event programming (and coupling).
