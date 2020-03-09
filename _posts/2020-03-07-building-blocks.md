---
layout: post
title: Building Blocks for Theoretical Computer Science
category: jekyll 
use_math: true
description: Learning formal mathematics
---

#### Lecture info:
- Title: Building Blocks for Theoretical Computer Science (V 1.3)
- Margaret M. Fleck
- Jan 2013

----------

### Formal Mathematics
- It is used to. create theoretical designs for algorithms and prove that they work correctly.
- This is especially important for methods that are used frequently and/or in applications where we don't want to failure.

### Math review
#### Some sets
- A number is positive if it is greater than zero. If you wish to exlcude negative values, but include zero, you must use the term "non-negative."
- Infinity is not a number in standard mathematics.
- It is important to state the types of variables explicitly like $x \in \mathbb{R}$ or $y \notin \mathbb{z}$.

#### Pairs of reals
- The set of all pairs of reals is written $\mathbb{R}^2$. 

#### Exponentials and logs
- Logarithms appear in CS as the running times of particularly fast algorithms.
- Outside of computer science, the default base for logarithms is usually $e$, because this makes a number of continuous mathematical formulas work nicely (just as base 2 makes many computer science formula work nicely).

#### Stirings
A *bit string* is a string consisting of the characters 0 and 1. If A is a set of characters, then $A^\*$ is the set of all (finite-length) strings containing only characters from A. For example, if A contains all lower-case alphabetic characters, then $A^\*$ contains strings like e, onion, and kkkkmmmmmbb. It also contains the empty string $\epsilon$.

### Logic
#### A bit about style
- Writng mathematics requires two things. You need to get the logical flow of ideas correct. And you also need to express yourself in standard style.
- Two systems of logic are commonly used in mathematics: propositional logic and predicate logic.

#### Propositions
- A *proposition* is a statement which is true or false (but never both!).
- Propositions are a helpful but too rigid to represent most of the interesting bits of mathematics.

#### Logical Equivalence
- $p \equiv q$
- De Morgan's Laws

#### Predicates
- Predicate logic allows variables and predicates that take variables as input.
- A predicate is a statement that becomes true or false if you substitute in values for its variables. 
- The main use of predicates is to make general statements about what happens when you substitute a variety for the variables.
- Is "For all $x$, $2x \geq x$" true or false? It depends on what values x can have. In order to decide whether a statement involving *quantifiers* is true, you need to know what types of values are allowed for each variable.
- Good style requires that you state the type of the variable explicitly when you introduce it, e.g. "For all natural numbers $x$, $2x \geq x$."

#### Quantifiers
- The general idea of a quantifier is that it expresses how many of the values in the domain make the claim true. In normal English, for example, "a few", "many", or "most."
- Mathematics uses only three quantifiers.
	- universal quantifier: "for all"
	- existential quantifier: "there exists"
	- unique existence
- We don't write "such that" when the quantifier is in shorthand. For example, $	\exists y \in \mathbb{R}, y = 2^{1/2}$. (In normal English, "there exists a real number y such that (s.t.) y=...")

#### Binding and scope
- $\forall x \in \mathbb{R}, x^2 + 3 \geq 0$, the universal quantifier binds the variable x.
- The "bound" variable in a quantification is only defined for a limited time, called the "scope" of the binding.
- If variable hasn't been bound by a quantifier, it is called "free."

### Proof
"An integer n is even if there is an integer m such that n=2m."
= "An integer n is even if it has the form 2m, where m is an integer."

#### Proving a universal statement
- We use a key definition of what we want to prove.
- We start from the known information and moved gradually towards the information that needed to be proved (in logical order).

#### Proving existential statements
- It is enough to exhibit some specific concrete object, of our choosing, with the required properties. The proof can be very simple (very short).
- Don't prove an existential claim using a general argument about why there must exist numbers with these properties. Use specific, concrete example. 

#### Disproving a universal statement
- To disprove a universal claim, we need to prove an existential statement.

#### Disproving an existential statement
- The negation of an existential claim is a universal one.

|             | prove            | disprove                 |
|-------------|------------------|--------------------------|
| universal   | general argument | specific counter-example |
| existential | specific example | general argument         |


