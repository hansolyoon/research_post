---
layout: post
title: Formal Verification, Casually Explained
category: jekyll 
description: Formal Verification, Casually Explained
---

### **What do we mean by software correctness?**
"We have a list of things we want the software to do, and use logic to prove the software does these things."

We call our list of things we want the software to do a *specification*. A program is only corret (or incorrect) relative to its specification; if the program is correct relative to its specification, we say it *implements* or *refines* the specification.

#### **How do we know the specification itself is correct?**
1. Write an even higher-level specification and prove our original spec implements the higher-level spec (recursively do this. s many times as you want)
2. Admit our specification is inherently not perfect.

#### Formal verification
The goal of formal verification: We want very strong guarantees our software is correct. Why? Because correct software provides greater utility than incorrect software.

How do we ensure the correctness of conventional software? Code review, automated testing, and real-world use. But it is easy to see these provide significantly weaker guarantees of correctness.

For formal verification, we need only three weak assumptions for our program to be guaranteed correct:
- Our top-level specification accurately corresponds to our idea.
- If our implementation proof contains errors, they are caught by our verifier program.
- If an event occurs in the real world, its effect on our program is captured by our model.

--------
Source: https://medium.com/@ahelwer/formal-verification-casually-explained-3fb4fef2e69a
