---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "ECON 4XX: Computational and Quantitative Macroeconomics"
subtitle: ""
summary: ""
tags: []
categories: []
date: 2022-04-00T07:13:10-07:00
lastmod: 2022-04-09T07:13:10-07:00
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
projects: ["datascience-computational"]
---

This is a newly proposed course which will be taught as **ECON 407 in Spring 2023**  as a pilot.  See additional **strongly recommended** prerequisites in addition to ECON407 requirements.

## Calendar Description:
**ECON 4XX: Computational and Quantitative Macroeconomics**

(3 credits course) Computational tools used in macroeconomics and financial economics including applications to unemployment, inequality, asset pricing, and economic growth

**Prerequisites**: One of ECON 301, ECON 304, ECON 308 and one of ECON 302, ECON 305, ECON 309 and one of ECON 323, CPSC 107, CPSC 110 and one of ECON 325, ECON 327, STAT 200 and MATH 221


To summarize: beyond the intermediate micro and macro courses required for 4th year economics electives, students are expected to have an understanding of probability from their econometrics or statistics courses, basic programming experience with Python, Matlab, or similar languages (i.e., Stata and introductory R are insufficient), and a class in the fundamentals of matrices and linear algebra (which is itself a prerequisite for ECON 323).  Students who learning programming through functional (e.g., a Lisp) or compiled imperative languages (e.g., C or Fortran) should also be able to keep up with the programming requirements.
## Course Overview

This is an introductory course in the computational tools used in macroeconomics.

Models in macroeconomics and financial economics are constructed from a core set of tools which provide a model of individual decisions while still maintaining an internal consistency between the decisions of many individuals in an economy.  Some of the common features of these models include
1. __dynamic and forward looking decisions__: If I consume less today, I can save more for tomorrow;
2. __randomness and uncertainty about the future__: If reject a job offer, I am not sure when the next offer will occur;
3. __prices and resources reflect the collective decisions of other agents__: The wage I am offered depends on the number of similar workers I am competing with, the intensity which the unemployed search for jobs, and the demand for my skills from firms;
4. __social learning from other agents' with information aggregated through prices__: If many others consider a particular equity or bond asset a good buy, then I can infer this by the price of the asset itself; and
5. __distributions and heterogeneity in the economy itself influences decisions and prices__: If the distribution of income is askew and there are many poor agents living hand-to-mouth, government policy such as sending out stimulus cheques has a different effect on inflation and customer welfare than if every person had similar incomes.

A difficulty inherent to macroeconomics is that often model features must hold at the same time, which makes it difficult to do counter-factual experiments with ``partial-equilibrium''---i.e., changing one price or element of the model in isolation---because of the interconnection of decisions, prices, and distributions.   However, by writing formal models in mathematics, you can conduct policy experiments and interpret the data while still ensuring self-consistency.  Using precise mathematical language will (1) uncover unanticipated consequences implicit in your assumptions; (2) keep everyone honest; (3) provide a framework to investigate changes in assumptions; (4) provide a framework to nest models and add enough "reality" to do quantitative analysis.

The downside is that while this set of mathematical tools provides a rich set of economic theories that can be explored and tested against the data, the inherent difficulty of dynamic models means that we may usually need to solve them approximately and on a computer.

This course will explore these sorts of theoretical models in conjunction with the computational tools to solve and simulate them.  We will learn using the Julia programming language - a modern language for scientific and technical computing which will also help teach a new, high-performance programming language to compliment their existing background in Python or Matlab from other courses.

## Learning Outcomes

By the end of the course, students will be able to
1. program your tools from linear algebra, probability, and optimization in the Julia programming language (LO1)
2. simulate and analyze stochastic processes and understand the evolution of the wealth distribution (LO2)
3. describe economic dynamics as a linear state space model and solve them numerically (LO3)
4. implement and analyze markov chains, and apply them to models of unemployment and asset pricing (LO4)
5. learn the role of general equilibrium and prices in aggregating information and reflecting the real economy (LO5)
6. define economic problems recursively, such labor market search and consumption savings models, and solve them numerically (LO6)
7. define and implement dynamic models of growth (LO7)

## Textbook and Materials
The core textbook is the online, open-source textbook [Quantitative Economics with Julia](https://julia.quantecon.org/) by Jesse Perla, Thomas J. Sargent and John Stachurski.  This set of lecture is quantitative economics and programming in economics, building on key open-source libraries. While it has both graduate-level and undergraduate-level material, in cases where material in the course is too advanced, we will choose a subset and adapt lecture materials to be appropriate for the level.

The textbook includes both theory and code, and a set of [Jupyter notebooks](https://github.com/QuantEcon/lecture-julia.notebooks).   

## Course Format
The course will meet for two 1.5 hours lectures per week for an in-class lecture. While there will not be a formal "lab", the instructor may go through coding examples in class. A teaching assistant will be available to help with the class size of approximately 50 students.

While the coding is intended to stay at as basic level as possible at first, students are expected to be reasonably proficient in Matlab, Python, and similar languages.  After the first few weeks the lectures will tend to focus on teaching the theory where code implementations done largely in the assignments.  At that point, additional coding will be done with a flipped lecture to ensure that students can slowly practice the material, leaving more time for macroeconomic theory.

All materials will be provided on http://canvas.ubc.ca and the open-source materials are on GitHub.  Students are expected to have a laptop for in-class exploration and quizzes.

## Assignments and Assessment

TBD

## Course Outline (by Week)
Note: a few of the linked lectures are currently in python, and a port is under way.
### Week 1: Introduction to Julia and programming for economics (LO1)

   - Topics include: [Getting Started](https://julia.quantecon.org/getting_started_julia/getting_started.html) and [Julia Essentials](https://julia.quantecon.org/getting_started_julia/julia_essentials.html)
   <!-- - At the end of the week students will have reviewed the basic setup of the Julia programming language and related it similar functionality in to Python or Matlab -->

### Week 2: Linear algebra and basic scientific computing (LO1)
   - Topics include [Arrays and Related Types](https://julia.quantecon.org/getting_started_julia/fundamental_types.html) and related topics in implementing [Linear Algebra](https://julia.quantecon.org/tools_and_techniques/linear_algebra.html).  In addition, students will review [Optimizers and Solvers](https://julia.quantecon.org/more_julia/optimization_solver_packages.html).  Interested students will be given bonus material in [Generic Programming](https://julia.quantecon.org/getting_started_julia/introduction_to_types.html)
   <!-- - At the end of the week students will feel comfortable: working with matrices, vectors, and arrays; solving linear systems and calculating eigenvalues; optimizing unconstrained and constrained functions; and solving systems of equations 
   - **Problem Set 1 Posted** - Basic loops, linear algebra, and optimization -->
### Week 3: Geometric Series and Stochastic Processes (LO2)
- https://julia.quantecon.org/tools_and_techniques/geom_series.html
- https://python.quantecon.org/scalar_dynam.html
- Simulating random processes and visualizing CLT and ergodic distributions

### Week 4: Dynamics of Wealth and Distributions (LO2)
- https://python.quantecon.org/ar1_processes.html
- https://python.quantecon.org/wealth_dynamics.html

### Week 5: Linear State Space Models Part (LO3)
- https://julia.quantecon.org/tools_and_techniques/linear_models.html

### Week 6: Permanent Income Model (LO3)
- https://julia.quantecon.org/dynamic_programming/perm_income.html

### Week 7: Markov Chains (LO4)
- https://julia.quantecon.org/tools_and_techniques/finite_markov.html
### Week 8: Models of Unemployment (LO4)
- Apply markov chains to https://julia.quantecon.org/multi_agent_models/lake_model.html
### Week 9: Rational Expectations and Firm Equilibria (LO5)
- https://julia.quantecon.org/multi_agent_models/rational_expectations.html
### Week 10: Asset Pricing (LO5)
- https://julia.quantecon.org/multi_agent_models/markov_asset.html
### Week 11: Lucas Trees (LO5)
- https://julia.quantecon.org/multi_agent_models/lucas_model.html
### Week 12: Recursive Equilibria and the McCall Search Model (LO6)
- https://julia.quantecon.org/dynamic_programming/mccall_model.html
### Week 13: Cake Eating Problem (LO6)
- https://python.quantecon.org/cake_eating_problem.html
- https://python.quantecon.org/cake_eating_numerical.html
### Week 14: Cass Koopmans/Neoclassical Growth (LO7)
- https://python.quantecon.org/cass_koopmans_1.html
- https://python.quantecon.org/cass_koopmans_2.html
### Week 15: Optimal Growth Model (LO7)
- https://julia.quantecon.org/dynamic_programming/optgrowth.html