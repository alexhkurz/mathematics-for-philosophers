# Equivalence Relations

(... preliminary notes, to be resumed ...)

## Introduction

In his [*An Essay Concerning Humane Understanding*](https://www.gutenberg.org/cache/epub/10615/pg10615-images.html), Book 2, Chapter 12 *On Identity and Diversity*, Section 12 *Consciousness makes personal Identity*, Locke writes (my emphasis):

> *in all these cases, our consciousness being interrupted, and we losing the sight of our past selves, doubts are raised whether we are the **same thinking thing**, i.e. the same SUBSTANCE or no. Which, however reasonable or unreasonable, concerns not **PERSONAL identity** at all. The question being what makes the **same person**; and not whether it be the **same identical substance**, which always thinks in the same person, which, in this case, matters not at all: **different** substances, by the **same consciousness** (where they do partake in it) being **united into one person**, as well as **different bodies** by the **same life** are **united into one animal**, whose identity is **preserved in that change** of substances by the **unity of one** continued life*

A few observations: 1) The text is difficult. 2) It is not clear whether the adjectives "same", "different", "united into" have a fixed meaning or change their meaning dependent on the nouns "substance", "person", "consciousness", "bodies", "animal" and "life". 3) As it often happens in philosophy, the author tries to illuminate one difficult notion (identity) by bringing in other unexplained notions (no less difficult) such as consciousness, person, preservation in change, life, unity. 

I want to emphasize the last item. As it is often the case, in every day reasoning or in philosophy or even in the sciences, it is all to easy to run into a **circle of explanations**. [^circleExplanations] To explain how mathematicians are able to break the circle of explanations is one of the main aims of these notes. [^circleExplanations2]

[^circleExplanations]: ... more examples ...

[^circleExplanations2]: Even in mathematics, one can have a discussion of how successful exactly the endeavor of breaking the circle of explanations was. Certainly, breaking the circle of explanations comes at a price and requires, from a philosophical point of view, compromise. But a practical proof that it can be done is given by the modern AI systems that are able to do mathematics. Maybe we can come back to this at the end of this course.

At this point, I wanted to understand better what philosophers have to say about identity in general and continued with the [SEP on the Logic of Identity](https://plato.stanford.edu/entries/identity/#LogiIden) (my emphasis):

> *Numerical identity can be characterised, as just done, as the **relation** everything has to itself and to nothing else. But this is circular, since “nothing else” just means “no numerically non-identical thing”. It can be defined, equally circularly (because **quantifying** over all **equivalence relations** including itself), as the **smallest equivalence relation** (an equivalence relation being one which is **reflexive, symmetric and transitive,** for example, having the same shape). Other circular definitions are available. Usually it is defined as the equivalence relation (or: the reflexive relation) satisfying Leibniz’s Law, the principle of the indiscernibility of identicals, that if x is identical with y then everything true of x is true of y. Intuitively this is right, but only picks out identity uniquely if “what is true of x” is understood to include “being identical with x”; otherwise it is **too weak**. Circularity is thus not avoided. Nevertheless, Leibniz’s Law appears to be crucial to our understanding of identity, and, more particularly, to our understanding of distinctness: we exhibit our commitment to it whenever we infer from “Fa” and “Not-Fb” that a is not identical with b. Strictly, what is being employed in such inferences is the **contrapositive** of Leibniz’s Law (if something true of a is false of b, a is not identical with b), which some (in the context of the discussion of vague identity) have questioned, but it appears as indispensable to our grip on the concept of identity as Leibniz’s Law itself.*

At this point, one may ask whether, again, one notion is "explained" by introducing other unexplained notions. But this time the situation is different. First-order logic and set theory can be used to provide rigorous mathematical definitions. 

This is what we outline in the following. 

The claim of this note is that understanding mathematics is essential to understanding what philosophers write about identity. Whether it helps to solve the philsophical problems is another matter.

## First-Order Logic

Before coming to set theory, I give a quick review of first-order logic. This is not meant to be self-contained, rather I would like to assume that the reader has taken the equivalent of an undergraduate course on symbolic logic (in which case I recommend to skip this section).

In fact, instead of writing out new notes, I link to my notes on [Discrete Mathematics (Logic and Relations)](https://hackmd.io/@alexhkurz/SkIp4pL3w) I use in an undergraduate course *Programming Languages*.

## Naive Set Theory

My initial understanding was that naive set theory suffices to clarify the philosophical discussion of the SEP entry and there will be no need to dive into formal set theory which we will briefly discuss in an appendix. [^naivesetheory] But while giving the course, it became clear that much of the philosophical interest in first-order logic and set theory depends on whether the formal development of mathematics can successfully break the circle of explanations. So I ended up trying to balance the rope between naive set theory and formal set theory as follows. I used the notation of formal set theory; I use it in an informal way, but I tried to explain how it can be formalised if one is willing to put in the (admittedly large) effort; I often referred informally to software tools for which proofs are programs and which can verify mathematical proofs.

[^naivesetheory]: Naive set theory mixes logic and mathematics in an intuitive way without clarifying their relationship. Formal set theory starts from a small set of operations on strings (which can all easily be implemented on a computer), bootstraps from there first-order logic as a set of rules of string manipulation, defines set theory as one particular theory in first-order logic and goes on to show that all of mathematics can be encoded in set theory. Formal set theory is important because it separates mathematics from meta-mathematics (mathematics about mathematics), object language from meta-language, etc. This, in turn, allows us to escape the [famous paradoxes](https://plato.stanford.edu/entries/russell-paradox/). It also helps to establish set theory as a beautiful and rich area of mathematics in its own right. 

### 1) First-Order Logic and Set Theory

Quick review of logic. Very rough sketch of how to build up mathematics from logic and set theory. [^first] The difference between $\subseteq$ and $\in$. That sets can be elements of sets. How to define numbers in set theory. The axiom defining the empty set $\emptyset$.

Review: [Logic](https://hackmd.io/@alexhkurz/SkIp4pL3w) and [Set Theory](https://hackmd.io/@alexhkurz/B1QX46L3P).

[^first]: We only introduced part of the language of set theory $\wedge, \vee, \neg, \forall,\exists, =$ plus notation for the empty set $\emptyset$ and comprehension $\{\ldots\}$. We talked about defining natural numbers and predicates such as $Even(x)$.

### 2) A Rational Number is a Set

- Functions and relations (partly from my [notes on Relations](https://hackmd.io/@alexhkurz/SJ1cc-dDr)). How to extend first-order logic by theories. Example: set theory extends FOL by adding the relation symbol $\in$ (plus a little more) and  axioms).
- The axiomatic method. How the axiomatic method breaks circular definitions (first, by building up theories "from below", second,  by breaking the "circle of explanations").
- Short digression on the difference between explicit definitions (such as $\subseteq$ from $\in$) and  implicit definitions (such as the empty set as the unique set satisfying $\neg\exists x \,.\, x\in\emptyset$). Further digression on explicit definitions $x=0$ and implicit definitions $(x + 2)\cdot 3 = 6$ and that arithmetic is special in that we can solve equations, that is, turn implicit defitions into explicit ones.
- Difference between the logical equality  $=$ built into first-order logic and a new relation symbol $\equiv$ that represents an equivalence relation. We introduced equivalence relations by saying that to understand a statement such as $1+1=2$ we need to acknowledge that, when we go back to the beginning, $1+1$ is different from $2$ (certainly, they are different as strings), so let us, just to be careful, replace $=$ by a new symbol $\equiv$ and write $1+1\equiv 2$ instead (and $1+1\not=2$).
- To get a different but more familiar and substantial example we turned to fractions and rational numbers. A fraction is a pair $(a,b)$, for example, we write now $(1,2)$ instead of $\frac 1 2$. We use now $=$ for the ordinary equality of integers (and we allow ourselves addition and multiplication of integers, we now do have again $1+1=2$ and all the other equations of integer arithmetic). We extend $=$ to pairs by saying that $(a,b)=(c,d)$ if $a=c$ and $b=d$. But this is not the right equality for fractions, for example we want $\frac 1 2 = \frac 2 4$, or, in our new notation $(1,2) \equiv (2,4)$. 
- Notice that to conduct our detailed analysis of identity of fractions, we need to distinguish $=$ and $\equiv$. Once we understand identity of fractions, we can blur this distinction again, but, for now, we are in the situation where we have
$$(1,2)\not=(2,4) \ \ \ \textrm{but want} \ \ \ (1,2)\equiv(2,4)$$
- How to define $\equiv$. Notice that we want to say that $(a,b)\equiv(c,d)$ if $a$ divided $b$ equals $c$ devided by $d$. But that would be circular: The definition of fractions should not be based on already assuming that we know how to divide (after all we want to define fractions in order to be able to do division of integers). What can we we do?
- We notice that in ordinary mathematics (but this notation is not available at the current stage of our development of formal mathematics), we have $\frac a b = \frac c d$ if and only if $a\cdot d= b\cdot c$. Remember that we do assume that we have multiplication of integers available. With this trick, we can break the circle of explanations and define: 
$$(a,b)\equiv (c,d) \ \  \textrm{ if } \ \ a\cdot d=b\cdot c$$
- We went on to define equivalence classes [^class] $$[(a,b)]_\equiv=\{(c,d) \mid (a,b)\equiv (c,d)\}$$
- We can now define the rational numbers as the set of equivalence classes $[(a,b)]_\equiv$ where $a$ is an arbitrary integer and $b$ is a positive integer. (We need to insist that $b\not=0$.)

[^class]: Here *class* is just another word for set, used for historical reasons. It would be perfectly fine to say "equivalence set" if it was not a very unusual expression. (Footnote: In set theory one sometimes makes a subtle distinction between sets and classes, but this is not relevant for our purposes.)

At this stage there is a lot to reflect upon. We finished with a short summary and promised to come back to all of this in the next session.

### 3) Review: Definition by equivalance class

We reviewed everything we have done so far and added one important bullet point (and several footnotes):

- Finally, we have
$$(a,b)\equiv (c,d) \ \  \textrm{ if and only if } \ \ [(a,b)]_\equiv = [(c,d)]_\equiv$$

*Notice that from now on, we can use $=$ again instead of $\equiv$ since equivalence of fractions (left-hand side) is ("if and only if") identity of equivalence classes (right-hand side).*
    
Notice that the sentence above contains three different notions of identity, namely, $\equiv$ and $=$ and "is". [^discuss]
    
[^discuss]: Discuss whether we were able to break the circle of explanations.
    
### 4) How to Calculate with Equivalence Classes

In this session, we dive into some technical work and show that the rational numbers (as defined via equivalence classes) satisfy indeed the usual rules of arithmetic.

- Review: The rational number $\frac a b$ is  set of all representations equivalent to $\frac a b$.
- We want to show that to multiply two rational numbers, it doesnt matter which representatives one chooses. That is, we want to prove that

$$(a,b)\equiv (a',b') \ \  \& \ \  (c,d) \equiv (c',d') \ \ \ \ \Longrightarrow \ \ \ \ (a\cdot c,b\cdot d)\equiv (a'\cdot c',b'\cdot d')$$

*Exercise:* Prove the statement above. Answer in the footnote.[^abcd]

[^abcd]: ![](https://hackmd.io/_uploads/r1wAYq5Fj.jpg)

*Exercise:* Think about why in the proof above, one cannot replace "$\cdot$" by "$+$".

But, of course, we know (from our pre-understanding of fractions) that we can add fractions. 

*Homework:* Prove that addition of rational numbers is independent of choice of representatives of equivalence classes.

Answer in the footnote.[^ad+bc]

[^ad+bc]: ![](https://hackmd.io/_uploads/r1JaFqcYj.jpg)

*To summarize*, whatever $\equiv$ and whatever the operation $\diamond$, to show that the operation $\diamond$ can be extended to equivalence classes one needs to show that $\diamond$ is independent of choice of representative, that is, 

$$\frac {t\equiv t' \ \ \ \ s \equiv s'} {t\diamond s \equiv t'\diamond s'}$$

Thus, we not only formalized arithmetic on rational numbers, we also learned a general method of defining mathematical objects as equivalence classes and how to compute with such equivalence classes.



### 5) Excursion into History

- Dedekind's [Was sind und was sollen die Zahlen?](http://www.opera-platonis.de/dedekind/Dedekind_Was_sind_2.pdf) introduces the natural numbers (in a naive set theory that we know today can easily be completely formalized). [^dedekind]
- The history of equivalence relations is discussed in Section 3 of Asghari's [Equivalence: an attempt at a history of the idea](https://link.springer.com/article/10.1007/s11229-018-1674-2) ...
- The SEP:
    - [The Modern History of Computing](https://plato.stanford.edu/entries/computing-history/)  
    - [Dedekind](https://plato.stanford.edu/entries/dedekind-foundations/) and [The Early Development of Set Theory](https://plato.stanford.edu/entries/settheory-early/)
    - [Russell's Paradox](https://plato.stanford.edu/entries/russell-paradox/) and [Self-Reference](https://plato.stanford.edu/entries/self-reference/)


... < more to come here > ...

[^dedekind]: On page 379 one finds of [this edition](https://gdz.sub.uni-goettingen.de/id/PPN23569441X).

    ![](https://i.imgur.com/j5oQtJw.png)

    We see that Dedekind does recursion on the second argument, uses $1$ as its base case instead of $0$, and writes $'$ for successor. Multiplication is treated similarly on page 382.


### 6) ... < more to come here > ...


## Epilogue

I want to come back to the question whether the formalization of mathematics was successful at breaking the circle of explanations. My short answer: Yes, from an engineering point of view. No, from a mathematical/logical point of view. No, from a philosophical point of view. 

From an engineering point of view, the success of software tools that are able to do mathematics shows that the circle of explanations can be broken down to simple operations on strings that can be performed on any computer.

From a mathematical/logical point of view, Goedel's incompleteness theorem shows that there can be no mathematical proof that the formalization of mathematics breaks the circle of explanations successfully. [^goedel]

[^goedel]: One should discuss whether the theorems of Goedel and Gentzen can be understood as a *philosophical* argument in favour of the success of breaking the circle of explanations.

From a philosophical point of view, we need to view mathematics as a human activity. In this view, breaking the circle of explanations appears to be  a trick. For example, when we defined equality of fractions in order to define the rational numbers, we found the formal definition 
$$(a,b)\equiv (c,d) \ \  \textrm{ if } \ \ a\cdot d=b\cdot c$$

only by using our informal pre-understanding of fractions which told us that
$$\frac a b = \frac c d \ \ \ \Longleftrightarrow \ \ \ \  a\cdot d=b\cdot c$$

Mathematicians and software engineers may be  happy with this trick that Wittgenstein called throwing ["away the ladder after he has climbed up it"](https://people.umass.edu/klement/tlp/tlp-hyperlinked.html#p6.54GER), but as Wittgenstein himself admitted, this is not a philosphical interesting attitude: ["Whereof one cannot speak, thereof one must be silent"](https://people.umass.edu/klement/tlp/tlp-hyperlinked.html#p7GER). [^wittgenstein]

[^wittgenstein]: There are several hyperlinkded online editions of the Tractatus that visualize its tree structure: [Pierre Bellon](https://pbellon.github.io/tractatus-tree/#/), [hhfpatrick](https://tractatus.xyz/). I found these links via the [University of Iowa Tractatus Map](http://tractatus.lib.uiowa.edu/) which also have a [beautiful map of the Tractatus](http://tractatus.lib.uiowa.edu/map/).


## Appendix: Formal Set Theory

I never taught a course on set theory, so I cannot confidently make recommendations of what the best textbooks and resources are. I select some that are available online and look reasonable.

To see how a formal develop of set theory looks like try [An Introduction to Set Theory](https://www.math.toronto.edu/weiss/set_theory.pdf) by William Weiss. Maybe start with the essence, the 11 axioms on page 117.

After that, a shorter and more gentle introduction is [Introduction to Set Theory](https://math.berkeley.edu/~seanm/ZF_notes.pdf) by Sean Murphy (contains some typos but seems to strike a good balance between formal development and explanation).

Further explanations and background are in [Wikipedia](https://en.wikipedia.org/wiki/Set_theory) and at the [SEP](https://plato.stanford.edu/entries/set-theory/).
