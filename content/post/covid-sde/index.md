---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Modeling Shocks in COVID 19"
subtitle: "An Introduction to Stochastic Differential Equations"
summary: ""
authors: []
tags: []
categories: []
date: 2020-09-13T22:06:40-07:00
lastmod: 2020-09-13T22:06:40-07:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
In the [Quantitative Economics with Julia](julia.quantecon.org) book, we have added two new lectures.

1. [Modeling COVID 19 with Differential Equations](https://julia.quantecon.org/continuous_time/seir_model.html)
- In this lecture, dynamics are modeled using a standard SEIR (Susceptible-Exposed-Infected-Removed) model of disease spread, represented as a system of ordinary differential equations where the number of agents is large and there are no exogenous stochastic shocks.
2. [Modeling Shocks in COVID 19 with Stochastic Differential Equations](https://julia.quantecon.org/continuous_time/covid_sde.html)
- In this lecture, we extend the model to include shocks to the $R_0$ and the mortality rates.  Stochastic Differential Equations (SDE) coupled with features in [SciML](https://diffeq.sciml.ai/) such as [Parallel Ensembles](https://diffeq.sciml.ai/dev/features/ensemble/#ensemble) provide a rich environment to experiment with non-deterministic models.