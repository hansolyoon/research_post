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
- It is used to create theoretical designs for algorithms and prove that they work correctly.
- This is especially important for methods that are used frequently and/or in applications where we don't want to failure.

### Math review
#### Some sets
- A number is positive if it is greater than zero. If you wish to exlcude negative values, but include zero, you must use the term "non-negative."
- Infinity is not a number in standard mathematics.
- It is important to state the types of variables explicitly like $x \in \mathbb{R}$ or $y \notin \mathbb{Z}$.

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

#### Direct proof
- At the end of our proof, put "which is what we needed to show," a box (after a dot), or Q.E.D. It helps tell the reader that we're done with the proof.

#### Proof by cases
- When the given information allows two or more separate possibilities, it is often best to use a technique called "proof by cases." ($x > 6 or x < -6$)
- In this case, you must be sure that all your cases, taken together, cover all the possibilities.

#### Proof by contrapositive
- If the original claim was $\forall x, P(x) \rightarrow Q(x)$ then its contrapositive is $\forall x, \neg Q(x) \rightarrow \neg P(x)$.
- It is safe to state "We'll prove the contrapositive of this statement. That is, ..."

### Number Theory
- Number theory is a branch of mathematics concerned with the behavior of *integers.* (cryptography, randomization, prime number)

#### Factors and multiples
If b = an for some integer n, a is called a factor or divisor of b. b is called a multiple of a. (a | b)

#### Prime numbers
- an integer $q \geq 2$ is prime if the only positive factors of q are q and 1. An integer $q \geq 2$ is composite if it is not prime.
- Numbers smaller than 2 are neither prime nor composite.

#### The division algorithm
- The division algorithm: For any integers a and b, where b is positive, there are unique integers q (the quotient) and r (the remainder) s.t. a = bq+r and $0 \leq r < b$.
- The remainder is required to be non-negative. So -10 divided by 7 has the remainder 4, because (-10) = 7(-2)+4. This is the standard convention in mathematics.

#### Euclidean algorithm

#### Pseudocode
- Pseudocode is an abstracted type of programming language, used to highlight the important structure of an algorithm and communicate between researchers who may not use the same programming language. 
- Details required only for a compiler are omitted.
- Many small details are not standardized but it's usually easy for a humban to figure out what the author must have intended.

#### Congruence mod k
- Many applications of number theory, particularly in CS, use modular arithmetic. The formal mathematical definitions of modular arithmetic are based on. he notion of congruence.
- If k is any positive integer, two integers a and b are congruent mod k if k | (a-b). For example, $3 \equiv 10$ (mod 7).

#### Equivalence classes
- The equivalence class of x (written [x]) is the set of all integers congruent to x mod k. Or, equivalently, the set of integers that have remainder x when divided by k.

### Sets
- Definition: A set is an unordered collection of objects.
- The items in the set are called its elements or members. $x \in A$ means that x is a member of the set A.
- Three basic way to define a set:
	- describe its contents in mathematical English, e.g. "the integers between 3 and 7, inclusive."
	- list all its members, e.g. {3, 4, 5, 6, 7}
	- use so-called set builder notation, e.g. {$x \in \mathbb{Z} | 3 \leq x \leq 7}
- Set builder notation has two parts separated with a vertical bar or a colon. It is often read "such that."
- The general term for an ordered sequence of k numbers is a k-tuple. Tuples are very different from sets, in that the order of values in a tuple matters and duplicate elements don't magically collapse. So (1, 2, 3, 4) $\neq$ (1, 2, 3) and (1, 2, 2, 3) $\neq$ (2, 2, 1, 3). Therefore, make sure to enclose the elements of a set in curly brackets and carefully distinguish curly brackets (set) from parentheses (ordered pair).
- A tuple must contain at least two elements. In formal mathematics, a 1-dimensional value x is just written as x, not as (x).
- By contrast, {57} is not the same as 57 in set. A set can also contain nothing at all, and such set is called the empty set or the null set.

#### Cardinality, inclusion
- If A is a finite set, then |A| is the number of objects in A. It is called cardinality of A.
- A is a subset of B (written A $\subseteq B$), $\forall x, x \in A \rightarrow x \in B$.
- If two sets can be different, A is a proper subset of B. $A \subset B$.

#### Vacuous truth
- Empty set is a subset of any set A.
- $\forall n, P(n) \rightarrow Q(n)$ is true when $P(n)$ is false even though $Q(n)$ is weird statement.
- These seems to be counter-intuitive. Such claims are *vacuously* true.

#### Set operations
- Given two sets A and B, the intersection of A and B ($A \cap B$) is the set containing all objects that are in both A and B.
- If the intersection of two sets A and B is the empty set, i.e. the two sets have no elements in common, then A and B are said to be disjoint.
- The union of sets A and B ($A \cup B$)
- The set difference of A and B (A-B) contains all the objects that are in A but not in B.
- The complement of a set A($\overline{\rm A$) contains all objects that are not in A.
- Cartesian product (A X B) = {$(x, y)|x \in A and y \in B}. Order matters for Cartesian products.

#### Size of set union
- Inclusion-Exclusion Principle: $|A \cup B| = |A| + |B| - |A \cap B|

### Relations
- A relation R on a set A is a subset of A X A, i.e. R is a set of ordered pairs of elements from A. If R contains the pair (x,y), we say that x is related to y, or xRy in shorthand.

#### Properties of relations: reflexive
- Reflexive: every element is related to itself. (R is reflexive if xRx for all x $\in$ A)
- Irreflexive: no element is related to itself. (R is irreflexive if xR/x for all x $\in$ A). But irreflexive is not the negation of reflexive. The negation of reflexive would be "there is an x $\in$ A, xR/x"
- Neither reflexive nor irreflexive: some elements are related to themselves but some aren't.

#### Types of relations
- symmetric and antisymmetric
- transitive
- partial order: relation that is reflexive, antisymmetric, and transitive
- linear order(total order)
- stric partial order: irreflexive, antisymmetric, and transitive
- equivalence relation: reflexive, symmetric, and transtiive

### Functions and onto


