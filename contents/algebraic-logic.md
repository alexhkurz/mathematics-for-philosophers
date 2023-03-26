# Algebraic Logic

...

## Universal Algebraic Definition of Semilattice

In *universal algebra*, one studies sets $A$ equipped with operations, which are subject to equations.

**Definition:** A **monoid** $(A,e,\cdot)$ has a constant $e\in A$ and a binary operation $\cdot:A\times A\to A$ satisfing the equations
\begin{gather}
e\cdot a = a\\
a\cdot e = a\\
a\cdot(b\cdot c) = (a\cdot b) \cdot c
\end{gather}

For example, numbers with $e=0$ and $\cdot$ as $+$ are a monoid. Similarly, numbers with $1$ and multiplication are a monoid or truthvalues with *False* and *Or* and truth values with *True* and *And*.

These are also example of what is known as a commutative monoid. A **commutative monoid** $(A,e,\cdot)$ is a monoid that is commutative, that is, it satifies
$$a\cdot b= b\cdot a$$

for all $a,b\in A$.

A monoid $(A,e,\cdot)$ is **idempotent** if 

$$a\cdot a= a$$ 

for all $a\in A$.

A commutative idempotent monoid is called a **bounded semilattice** (or sometimes semilattice for short). 

**Example:** 
- Truth values with *False* and *Or* are a bounded semilattice and truth values with *True* and *And* are a bounded semilattice.
- Sets with $\emptyset$ and $\cup$ are a semilattice.

We arrived at the algebraic definition of a (bounded) semilattice, that is, a definition in terms of operations and equations.

## Order-Theoretic Definition of Semilattices

### What is an order?

A **pre-order** $(A,R)$ consists of a set $A$ together with a relation [^times]
$$R\subseteq A\times A$$

[^times]:$A\times B = \{(a,b) \mid a\in A, b\in B\}$. And $X\subseteq Y$ means that $x\in X\Rightarrow x\in Y$.

such that

\begin{gather}
(a,a)\in R \\
\textrm{ if } (a,b) \in R \textrm{ and } (b,c)\in R \ \textrm{ then } \ (a,c)\in R
\end{gather}

In words, $R$ is *reflexive* (the first condition) and $R$ is *transitive* (the second condition). Usually one writes $aRb$ instead of $(a,b)\in R$ and also $\le$ instead of $R$. Finally, one often uses "," to mean "and" and $\Longrightarrow$ to mean "if ... then ...".

With this notation the two conditions above become

\begin{gather}
a\le a \\
a\le b, b\le c \ \ \Longrightarrow \ \ a \le c
\end{gather}

A **partial order** $(A,\le)$ is a pre-order such that 
$$a\le b, b\le a \ \Longrightarrow \ a=b$$



### Semilattices

In an order $(A,\le)$, an element $c\in A$ is an **upper bound** of $a$ and $b$ if $a\le c$ and $b\le c$. If for all $d\in A$ we have
$$a\le d,b\le d \ \Longrightarrow \ c\le d$$

then $c$ is called a **least** upper bound.

*Exercise:* Define greatest lower bound.

*Notation:* The least upper bound of $a$ and $b$ is denoted by $a\vee b$.

*Remind:* Let us recall or-introduction 
$$\frac a {a\vee b} \quad\quad \frac b {a \vee b}$$

and or-elimination
$$\frac {a\vee b \quad \frac {a}{d} \quad \frac{b}{d}} d$$

A **join-semilattice** is a partial order in which any two elements have a least upper bound.

A **meet-semilattice** is a partial order in which any two elements have a greatest lower bound.

## Equivalence of Algebraic and Order-Theoretic Definitions

...

todo

...

## Order in Algebraic Logic

In algebraic logic, the "logical order" $a\le b$ is read as "if $a$ then $b$".

We all expect "if $a$ then $a\vee b$".

Thus, $a\le a\vee b$. 

## Weak Kleene Logic according to Jose

I claim that in WK logic, we have $a\le\star$ for all $a$, if $\le$ is the logical order induced by $\vee$.

We have

$$a \ \le \  a\vee \star$$

$$ a\vee \star \ = \ \star$$

Therefore

$$ a \le \star$$

## References

https://en.wikipedia.org/wiki/Semilattice