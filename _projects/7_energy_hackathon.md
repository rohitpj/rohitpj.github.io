---
layout: page
title: predicting site energy demand and solar yield
description: k-means clustering and XGBoost, built under time pressure — top 10% globally
importance: 7
category: engineering
---

An entry to a **global SLB hackathon**, forecasting two coupled quantities across a set of production sites: how much power each site would *consume*, and how much solar energy it would *generate*.

Sites differ enough that a single global model underfits them, but there are too few sites to justify a bespoke model each. The approach was to **cluster sites with k-means** first, so that sites with similar demand and generation profiles were modelled together, then fit **XGBoost** regressors on the resulting groups.

The entry placed in the **top 10% globally**.
