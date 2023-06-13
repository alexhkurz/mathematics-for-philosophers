# Recursion

(May 31, June 13)

## Introduction

Recursion is a fundamental concept of logic, mathematics, linguistics and philosophy, maybe even engineering, certainly computer science.

... math is about the infinite, physics about the finite, from the point of view of physics the infinite is an approximation (abstraction) of the finite that makes sense for large quantities, from the point of view of math finite computations approximate infinite mathematical structures ...

... but can one reason about the infinite with finite means? Yes, using recursion (or even co-recursion) ...

... Chomsky argues that recursion is a defining feature of human languages, but see the debate between Chomsky and Everett ... 

... GEB argues that recursion is related to the self, to consciousness, to ...

## Example of a Recursive Definition

Recursion is closely related to paradoxes and vicious circles.

In logic an example of a vicious circle can be a definition that defines sth, say A, in terms of A itself.

But not all circular definitions are "vicious".

For example, the following definition of numbers in terms of numbers is perfectly fine.

**Definition:**

- `|` is a number.
- For all `n`, `|n` is a number if `n` is a number.

The following questions arise:

- Is this a definition?
- If yes, what does it define?
- Is it circular?
- If yes, why is it a valid definition?

**Explanation:** Let us go through these questions one by one.

- Yes, we consider this is a definition "by recursion".
- The two clauses together define, *recursively* as we say, a set of strings (=sequences of symbols), call it $\sf N$.[^setOfNumbers] 
    1. According to the first clause, the string `|` is in  $\sf N$ (think of the string `|` as the number 1).
    2. According to the second clause with `n` = `|` we have that `||` is in $\sf N$ (think of `||`  as 2).
    3. According to the second clause again (take `n` = `||`), `|||` is in $\sf N$.
    4. etc
- We consider the definition circular because the second clause defines `|n` in terms of `n` but `n` itself is not defined, it is just a placeholder (meta-variable[^meta-variable]) without a specified value. 
- We consider this to be a good definition because it builds up everything from smaller parts. As indicated in steps 1-3 above, we only build `|||` after we built `||` after we built `|`. Put differently, we reduce `|||` to `||` to `|`, which, in turn is an "axiom".

[^meta-variable]: In the section on propositional logic, we will see variables (propositional variables) that are part of the language defined by recursion. The variable `n`, is not part of the defined language (the object language) but part of the language used to define the object language (the meta language). 

[^setOfNumbers]: We can think of the definition as defining the (counting) numbers, but it is slightly more accurate to say that it defines the *set* of numbers.

**Circle of Explanations:** Note that there is something strange about this explanation: The whole point of the recursive definition is to define the infinite set 
$\sf N$ by a *finite set of rules* without using "etc" or "...". This works. In fact, recursive definitions are so powerful that all of mathematics (and computing) can be built on top of recursive definitions. But the human *explanation* of why it works has apparently to make use of a device like "etc", see item 4 above. [^wittgensteinsLadder]

**Question:** In what sense does our definition define numbers? We said above "think of the string `|` as the number $1$". What does "think of as" mean here? We could say that the number $1$ is the semantics of the syntax `|`, but this is not an explanation, just a restatement of ""think of the string `|` as the number $1$".

## The Definition of the Natural Numbers

The official definition of natural numbers in mathematics is a slight variation of the one above. The definition of the counting numbers via `|` has some drawbacks. Let us recall the definition:

- `|` is a number.
- For all `n`, `|n` is a number if `n` is a number.

Working with definitions like this, it pays off to distinguish between the `|` in the first rule and the `|` in the second rule. The `|` in the first rule is the starting point, a constant. The `|n` in the second rule can be thought of as a function that takes `n` as its argument. It behaves like the mathenatical function $f(n)=n+1$. So here is our updated definition of the natural numbers.

- `O` is a natural number.
- If `n` is a natural number, then `S n` is a natural number.

Here is another notation one often finds

$$ \frac{}{ 0 \in \mathbb N}$$
$$ \frac{n \in \mathbb N}{\sf S \it n \sf \in \mathbb N}$$

or also

$$ \frac{}{\sf O : N}$$
$$ \frac{\it n \sf : N}{\sf S \it n \sf : N}$$


**Remark on Semantics:** `S n` is also known as the successor function. We often think of functions as mathematical objects being in the realm of semantics. `S` can be understood as living both in syntax and semantics. Or maybe we can say that `S` is syntax that is its own semantics. What I mean by this is that writing `S n` is on the one hand just symbol manipulation but on the other hand it computes $n+1$.

If we want to highlight the order in which numbers are built we can use parentheses and write `S(S(S O))` instead of `S S S O`. If we want to be brief we may also write `SSSO`.

... add some history with links to Dedekind, Peano, ...

https://github.com/mdnahas/Peano_Book/blob/master/Peano.pdf page 22,23

## Further Reading

For an introduction on recursion read
- Chapter 1 of [Goedel, Escher, Bach](https://www.physixfan.com/wp-content/files/GEBen.pdf).

To get an impression of where one can go with this have a look at (this is also where the definition of numbers using `O` and `S` appears)
- Chapter 8 of [Goedel, Escher, Bach](https://www.physixfan.com/wp-content/files/GEBen.pdf).



[^wittgensteinsLadder]: Maybe explore references to Wittgentstein on rule following.
