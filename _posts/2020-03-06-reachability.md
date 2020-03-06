---
layout: post
title: Reachability
category: jekyll 
use_math: true
description: Reachability is the task of figuring out what states a dynamical system could possibly reach.
---

#### Lecture info:
- Title: Cognitive Robotics
- Instructor: Prof. Brian Charles Williams
- As Taught In: Spring 2016
- MIT Course Number: 16.412J / 6.834J

----------

### Reachability 

> Reachability (or computing reach sets) is the task of figuring out what states a dynamical system could possibly reach.

> "Figuring out where our system could possible end up"

 Reachability analysis is primarily used for verification among various applications like planning, control, and monitoring of systems. Generally, we test for intersection between the reachable set and a set of bad states.

 *How to represent reachable sets?* 

 $R(X_0, t)$: the reach set at time t is the set of states x for which there exists a sequence of control inputs $u_0, ... u_{t-1}$ that would take us from a state $x_0 \in X_0$ to state x
 -> $R(X_0, s+t) = R(R(X_0,s),t)$

 In a Finite state machine, we could represent reach sets as finite sets.
 In a continuous system, a reach set will be a region of the state space, so we need a symbolic representation.

 **Two canonical representations:**
 - **Vertices**: polytope = convex hull
 - **Inequalities**: polytope = union set of solutions to inequalities

 **Closure**: If $P$ is a convex polytope, the $AP={Ax:x\in P}$ is also a convex polytope. Therefore a system defined by $x_{i+1}=Ax_i$, or linear system defined by $x_hat = Ax(s)+u(s)$, if we start with a convex set of $X_0$, then the $R(x_0, t)$ will also be convex. However, even if the reach set is convex, the reachable set $R(X_0, t)$ is not necessarily convex, but it will be a union of the convex polytopes.

 **"Flow tubes" or "funnels"**: a certain area of state space where a dynamic system and some control rules guarantee that you will eventually reach.

--------
### Questions:
- What are the differences between flow tubes and funnel? Only funnel considers uncertainty?

--------
### Interesting references
- Bradley and Zhao, 1993; Frazzoli, 2001 - Flow tubes 
- Hoffman and Williams, 2006 - Flow tubes with temporal constraints
- Tobenkin, Manchester, and Tedrake, 2011; Majumdar and Tedrake, 2012 - Funnels
- Anirudha Majumdar and Russ Tedrake, Robust Online Motion Planning with Regions of Finite Time Invariance
- Bhatia, A. and Frazzoli E., Incremental Search Methods for Reachability Analysis of Continuous and Hybrid Systems
- Hoffman A., Williams B., Exploiting Spatial and Temporal Flexibility for Plan Execution of Hybrid, Under-actuated Systems
- G. Bledt, A. Majumdar, A. J. Barry, R. Tedrake, UAV Trajectory Planning and Optimization for High Speed Flight with Uncertainties Using Computer Vision Through Forest, Presented at the MIT summer research program poster session.

--------
Source: https://ocw.mit.edu/courses/aeronautics-and-astronautics/16-412j-cognitive-robotics-spring-2016/lecture-notes/MIT16_412JS16_L18.pdf

