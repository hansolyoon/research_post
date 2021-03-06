---
layout: post
title: FaSTrack - Sylvia Herbert
category: jekyll 
description: FaSTrack is a tool that is used in conjunction with any model-based motion planner to provide safety guarantees while planning and executing trajectories in real time.
---

### FaSTrack 

Using the reachability techniques, safe motion planning can be accomplished for decomposable and low dimensional systems. For real life systems like cars, planes, and quad rotors, fast planning is intractable. 
Motion planners like rapidly-exploring random trees (RRT) or model-predictive control (MPC) can plan in real time by using simplified models of system dynamics, which sacrifice guarantees of safety and feasibility.

FaSTrack allows users to implement a fast motion planner for simplified dynamics while maintaining safety by providing a *precomputed* bound on the maximum possible tracking error between the planner and the autonomous system (Plan using the **simplified** model, but precompute a tracking error bound that captures all potential deviations of the trajectory due to model mismatch).

--------
### Ideas:
- Like a quadcopter simulation video in example section, can we infer the position of the obstacle by looking at the direction of the aircraft flying to the known goal region? If possible, we can infer intents without map information. Then we can minimize our reachable set by removing some heading angles that the drone may not go according to the inferred intent.
- In that cases, we may can predict future trajectory of any drones when there is no obstacle and an user does not follow an optimal path by assuming imaginary obstacles. A drone can choose arbitrary paths, but with limited rate of change. The goal is known.

--------
### Questions:

--------
### Interesting references
- Sylvia L. Herbert et al., FaSTrack:  a  Modular  Framework  for  Fast  and Guaranteed  Safe Motion  Planning
- How did she calculate a tracking error?
- How does pursuit-chase game work?

--------
Source: [FaSTrack: Fast and Safe Tracking — Sylvia Herbert](http://sylviaherbert.com/fastrack)
