---
layout: page
title: scheduling optimisation for rig operations
description: adapting Kuhn–Munkres and Murty's algorithms, and partitioning graphs to scale past them
importance: 5
category: engineering
---

Rig operations are an assignment problem with awkward extra structure. The classical tools fit the clean version of the problem well — the **Kuhn–Munkres** algorithm solves optimal assignment, and **Murty's algorithm** enumerates the *k*-best assignments when you need alternatives rather than a single answer — but real rig scheduling does not arrive in that shape.

## Adapting the classical algorithms

I modified both algorithms to accommodate the constraints that the standard formulations don't express, so that the optimality guarantees survive contact with the actual scheduling requirements.

## Partitioning to scale

More complex rig operations pushed past what the modified algorithms could handle directly. To reach those, I developed **novel graph partitioning algorithms** that decompose an operation into subproblems tractable for the assignment solvers, letting the pipeline process a class of operations it previously could not.

Built during my year at **SLB Cambridge Research**.
