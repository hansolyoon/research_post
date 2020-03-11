Some Thoughts on Runtime Verification

- Model checking was initially used in verification to contrast it with deductive (proof theoretic) methods of reasoning.
	- In LTL, a given sequence w is a model of a temporal logic formula $\phi$ if w satisfies $\phi$. Thus verification by model checking means to check whether all possible runs are models of $\phi$. 
	- In CTL, what is checked is whether the whole transition system (Kripke structure in modal logic parlance), viewed as a generator of a branching structure, is a model of the formula.

### Various interpretations of runtime verification
#### Runtime Verification as Simulation Plus Formal Specification
- According to the automata-theoretic approach to verification, exhaustive verfication corresponds to an *inclusion* problem between two formal languages: the set of behaviors produced by the system and the set of behaviors defined by the property. For checking a single behavior, the problem simplifies into a *membership* problem.
- In the context of digital hardware, monitoring is called *dynamic* verification against *assertions* while the term *static* or *formal* verification is used for model checking. Motivated initially by analog and mixed-signal circuits, we extended the idea to continuous and hybrid systems by introducing STL.

#### Runtime as More Real
- Another interpretation of runtime is literally, *while a program is running.* This means that in contrast with the abstract automaton model, we deal here with something closer to the implementation.


---------
### Questions
- symbolic model checking is BDD?
- symbolic model checking: set-based breadth-first simulation
	- symbolic means that logical formulae are used to describe the set of reachable states at successive time points.
- statistical model checking: just renamed term of simulation?	
- What is the difference between "Runtime Verification as Simulation Plus Formal Specification" and "model checking"?
- What is the exact meaning of 'monitoring', and what is differenfe between 'runtime verification' and 'runtime monitoring'?

---------
### Ideas
- 
