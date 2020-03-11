Predictive Run-Time Verificationof Discrete-Time Reachability Propertiesin Black-Box Systems Using Trace-LevelAbstraction and Statistical Learning

#### *Prevent*
- Prevent is a predictive RV framework, in which the monitor is able to predict the future exptensions of an execution, using a model inferred from the random sampling executions of the system. The monitor maintains a table of the states of the prediction model, with the probability of the extensions from each state that satisfy a safety property.
- The monitor finitely extends the prefix based on a *prediction model* that is trained on the set of *independent and identically distributed(iid)* sample traces.

- The size of the prediction model directly influence the monitor's memory usage and computational performance, so achieving a small prediction model is key in predictive RV.

- In RV, a monitor checks the current execution, that is a finite prefix of an infinite path, against a given property, typically expressed in LTL, that represents a set of acceptable infinite paths.

#### Running example
- Suppose checking the reachability property *eventually the outcome of the die is either "1" or "6", at runtime, based on the symbols in the defined observation space.

#### Novelty
- Their apporach is novel in terms of applying learning and abstraction to predictive RV, and using HMM to handle non-determinism at the trace level.

---------
### Questions
- How does Prevent infer models?
- k-gapped pair model
- transient probability

---------
### Ideas
- In predictive RV, keep think about the probability. Will it be collide? Will it violate safety properties? With what probability?
- In UAV work, I tried to project future *positions* of a UAV *with* a model, while this work project future *states* of a system *without* an explicit model. Try *prevent* for a UAV.