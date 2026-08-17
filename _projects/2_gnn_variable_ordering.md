---
layout: page
title: graph neural networks for variable ordering
description: better representations for cylindrical algebraic decomposition — and a hard look at the benchmark data
importance: 2
category: research
related_publications: true
---

Quantifier elimination via cylindrical algebraic decomposition is exquisitely sensitive to the order in which variables are eliminated. A good ordering finishes in seconds; a bad one on the same problem can run for hours or exhaust memory. Choosing that ordering is a natural target for machine learning, and several models have been proposed for it.

## Representations

Prior work largely encoded problems as flat feature vectors — degree counts, occurrence statistics, and similar summaries — which discard the structure of the polynomial system. This project explored **graph neural network representations** instead, encoding the problem so that the relationships between variables and polynomials survive into the model.

## The data problem

The more consequential finding was about the datasets rather than the models. The benchmark corpora used to train and evaluate variable-ordering models turned out to contain significant pollution — redundancies and artefacts that let models score well for reasons unrelated to the actual task. Any comparison run on the uncleaned data flatters itself. A meaningful part of the work was identifying and resolving this so that model comparisons mean something.

## Outcome

Presented at **ICMS 2024** and published in the proceedings as *Exploring Alternative Machine Learning Models for Variable Ordering in Cylindrical Algebraic Decomposition* ([DOI](https://doi.org/10.1007/978-3-031-64529-7_20)), with James Davenport.
