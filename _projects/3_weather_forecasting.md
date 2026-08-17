---
layout: page
title: forecasting from noisy, incomplete weather data
description: Bayesian imputation and Transformer time-series models, applied to campus energy scheduling
importance: 3
category: research
---

A research placement at the **University of Exeter**, working on the practical problem that real environmental datasets are neither clean nor complete: sensors drop out, readings drift, and whole spans of history are simply missing.

## Imputation

Rather than discarding incomplete records or filling gaps with means, this work implemented **advanced Bayesian models** for imputation, so that the uncertainty introduced by missing data is carried forward into the prediction rather than quietly assumed away.

## Forecasting

For the forecasting stage I adapted the **Transformer architecture** to time-series data, reaching accuracy competitive with state-of-the-art models on the same benchmarks.

## Application

The models were put to work on a concrete scheduling problem: predicting building energy consumption and using those predictions to optimise lecture timetables against energy cost. Results were presented at a departmental symposium.
