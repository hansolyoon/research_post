Combining Model Checking and Runtime Verification for Safe Robotics

- Validating the end-to-end correctness of robotics system consists of two parts:
	- a high-level programming language for implementing and systematically testing the reactive robotics software via model checking
	- a signal temporal logic based online monitoring system to ensure that the assumptions about the low-level controllers used during model checking hold at runtime

#### Key features
1. The event-driven programming language P for implementing and model checking high-level robotic logics; P analysis assumes a discrete abstraction of the continuous robot dynamics
2. A combination of STL and regression methods to infer the parameters under which the assumptions made in (1) are satisfied;
3. An online monitoring based approach to ensure that the specification defined in (2) are not violated by the robot at runtime.

---------
### Questions
- What is a programming lanugage called P?
- Drona; tool for simulating autonomous drones

---------
### Ideas
- Need to read carefully this paper again.

---------
### Interesting references
- https://drona-org.github.io/Drona/