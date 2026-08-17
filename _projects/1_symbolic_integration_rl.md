---
layout: page
title: learned rule ordering for symbolic integration
description: replacing SymPy's hand-written integration heuristics with a policy learned by reinforcement learning
importance: 1
category: research
related_publications: true
---

Computer algebra systems integrate expressions by repeatedly applying transformation rules. Which rule to try next is, in most systems, decided by a hand-written heuristic ordering — a fixed priority list assembled over years by the maintainers. The ordering works, but it is static, opaque, and tuned to the problems its authors happened to have in front of them.

This project replaces that ordering in **SymPy** with a learned policy.

## Approach

The core difficulty is supervision. There is no ground-truth dataset of "the optimal rule to apply to this integrand" — constructing one would mean solving the search problem you are trying to learn in the first place. So instead of learning from labels, the policy is trained against the integrator itself: the integration process is treated as an environment, rule choices as actions, and successful termination (and its cost) as reward. Transformer models over the expression tree provide the state representation.

This sidesteps both of the usual crutches — no hand-tuned heuristics, and no pre-labelled dataset.

## Outcome

Presented at **SCML 2026** (Conference on Symbolic Computation and Machine Learning), and submitted to the *Journal of Symbolic Computation*. Joint work with Rashid Barket and Matthew England.
