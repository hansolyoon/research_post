Probabilistic Black-Box Reachability Checking

- Unlike testing, model checking cannot be applied in a black-box setting. To overome thsi limitation Peled et al. introduced black-box checking, a combination of testing, model inference and model checking.
- The technique requires systems to be fully deterministic. For stochastic systems, statistical techniques are available. However, they cannot be applied to systems with non-deterministic choices. 
- This paper present a black-box checking technique for stochastic systems that allows both, non-deterministic and probabilistic behavior.

- Rather than inferring DFA, author assume that systems can be modelled by Markov decision processes (to handle non-deterministic behavior).

---------
### Questions
- probabilistic model checking
- Model inference tool ALERGIA?
- Reachability analyzer PRISM?
- statistical model checking

---------
### Ideas
- Does RV requires a system model? If yes, can we make a black-box RV? Even further, black-box predictive RV?
- For UAV, first guess of probability of future position would be 360 deg and everywhere. But we can update our info about vel, dv, omega, domega...more generally, states and changing rate of states, using Bayesian estimation. Then we can do predictive monitoring with probability. The only difference from IROS paper is that we don't have a system model.