---
layout: post
title: Runtime Monitoring for Safety-Critical Embedded Systems
category: jekyll 
description: PhD Dissertation of Aaron Kane, CMU, 2015
---

### Runtime Monitoring for Safety-CriticalEmbedded Systems

**Runtime Verification(RV)** is a lightweight technique to verify that certain properties hold over execution traces. Most existing RV methods utilize some form of system or code instrumentation and thus ~are not designed to monitor potentially black-box COTS components.~ But this paper present runtime monitoring framework for monitoring CPS with black-box components.

Traditionally, three main techniques are used for system verification:
- Theorem proving,
- model checking,
- and testing
**Theorem proving and model checking** are formal methods and has problem of the state space explosion problem which affects the scalability.
**Testing** scales better but it is infeasible for high-reliability systems.
**RV** can provide a formal analysis while avoiding many of the pitfalls that traditional model-based methods have such as state space explosion and model abstractions because RV scales with the trace rather than the system model. RV essentially provides the scalability of testing with the stronger assurances of formal methods giving up coverage like other formal methods. RV is implemented in the form of *monitors*.

RV is a ~supplementary technique~ to other common methods. RV can check that system satisfies a *proven* formal model's assumptions and abstractions at runtime. Because of unanticipated operating conditions, maintenance errors, runtime faults, malicious attacks, and other sources, a system faults can arise after checking by formal methods.

#### System Requirements
Requirements elicitation is one of the most difficult aspects of safety critical system design. What we can do is to translate from traditional informal system requirements to formal logic-based requirements.

#### Safety-Critical Systems
*Embedded systems* are systems which include a computer but are not used for general purpose computing. *Safaty critical systems* are systems whose failure can result in loss of life, significant property damage, or damage to the environment.

For the system specification, informal specification language like natual language, can lead to incorrect requirements and has ambiguities inherent. On the contrary, formal specification have many benefits including being unambiguous and checkable for syntactic correctness. But it is complex and error-prone, so many specification patterns have been proposed.

#### System Verification
**Verification** is the process of ensuring that the system adheres to its design specification. RV provides verification about the actual system rather than a model of the system. 

#### Runtime Verification
RV can be performed *online* or *offline* from recorded log files. A correctness property specified in a formal logic, mostly LTL, is translated into a monitor. 
- Safety properties: informally, "something bad does not happen"
- Liveness: "a good thing eventually happens" (bounded liveness properties are essentially safety properties)

--------
### Ideas:

--------
### Questions:
- It says most RV are not designed to monitor black-box CPS. Then how does DryVR handle black-box CPS? [DryVR](https://dryvr-02.readthedocs.io/en/latest/status.html)
- RV does not use model abstractions?
- If RV detects current violations, is it useful? It seems that it would be very easy with a simple program. From my understanding, only predictive RV is useful.
- What is three-valued or four-valued variants in LTL?

--------
### Interesting references
- 

--------
Source: https://users.ece.cmu.edu/~koopman/thesis/kane.pdf
