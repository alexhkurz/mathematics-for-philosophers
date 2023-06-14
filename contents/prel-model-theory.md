# Model Theory

(May 31)


Traditionally, modern logic is divided into two fields, proof theory and model theory.

Proof theory is what you did in the symbolic logic course when you learned how to do natural deduction proofs in first-order logic.

A well-known proof theorist is Giuseppe Greco.

Proof theory takes logic as being about manipulating strings (or trees) of symbols according to a finite and fixed set of rules. For example, in natural deduction, we have for each logical symbol an introduction and an elimination rule. Btw, this is similar to the MU-puzzle in Goedel, Escher, Bach.

On the other hand, we think of logical formulas as meaning something. The mathematical theory which tries to explain what logic means is called model theory.

You have not done model theory of predicate logic in your symbolic logic course. But you have done a little model theory for propositional logic.

---

In propositional logic the method of indirect truth tables (semantic tableaux) is a semantic or model theoretic method. To show that a formula is valid, we *systematically* search for models: *If there is no model that is a counterexample of the formula $\phi$ then $\phi$ is valid.*

This works in propositional logic, because every formula can have only finitely many models. [^truthTable]

[^truthTable]: In propositional logic, a model is a row in a truth table. If a formula has $n$ variables, then its truth table has $2^n$ rows. In computer science the algorith of (indirect) truth table has exponential worst case time complexity.

---

For predicate logic, the notion of model is more involved. In particular, there may be infinitely many models for a formula.

A model for predicate logic conists of a set $M$ together with an interpreation of all predicates.

The set $M$ is what the quantifiers range over. $M$ can be infinite. This is what makes predicate logic more powerful than propositional logic.

To make this text not too long I collected examples on a separate page.

![](https://hackmd.io/_uploads/SyzcxId83.png =400x)
![](https://hackmd.io/_uploads/H1wslUOUn.png)


