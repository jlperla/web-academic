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

**Prerequisites**: One of ECON 301, ECON 304, ECON 308 and one of ECON 302, ECON 305, ECON 309 and one of ECON 325, ECON 327, STAT 200, STAT 201, STAT 203, COMM 291 and MATH 221 and one of ECON 323, CPSC 110, CPSC 107, CPSC 103, MATH 210, COMM 337

To summarize: beyond the intermediate micro and macro courses required for 4th year economics electives, students are expected to have an understanding of probability from their econometrics or statistics courses, basic programming experience with Python, Matlab, or similar languages (i.e., Stata and introductory R are insufficient), and a class in the fundamentals of matrices and linear algebra (which is itself a prerequisite for ECON 323).  Students who learning programming through functional (e.g., a Lisp) or compiled imperative languages (e.g., C or Fortran) should also be able to keep up with the programming requirements.
## Course Overview

This is an introductory course in the computational tools used in macroeconomics.

Models in macroeconomics and financial economics are constructed from a core set of tools which provide a model of individual decisions while still maintaining an internal consistency between the decisions of many individuals in an economy.  Some of the common features of these models include
1. __dynamic and forward looking decisions__: If I consume less today, I can save more for tomorrow;
2. __randomness and uncertainty about the future__: If reject a job offer, I am not sure when the next offer will occur;
3. __prices and resources reflecting the collective decisions of other agents__: The wage I am offered depends on the number of similar workers I am competing with, the intensity which the unemployed search for jobs, and the demand for my skills from firms;
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

While the coding is intended to stay at as basic level as possible at first, students are expected to be reasonably proficient in Matlab, Python, Julia, and similar languages.  After the first few weeks the lectures will tend to focus on teaching the theory where code implementations done largely in the assignments.  At that point, additional coding will be done with a flipped lecture to ensure that students can slowly practice the material, leaving more time for macroeconomic theory.

All materials will be provided on http://canvas.ubc.ca and the open-source materials are on GitHub.  Students are expected to have a laptop for in-class exploration and exams.

## Assignments and Assessment
The only way to learn how to apply programming to economic problems is practice. To aid in this, a significant portion of the grade will be the six problem sets.

The midterm and final will be in class and combine both theory and computations, with the exam submitted via a Jupyter notebook.

The weighting in the grade is:
- 6 Problem sets: 30% (total)
- Midterm exam: 30%
- Final exam: 40%

The problem sets will start off short and easy to help those with less programming experience, and then build in complexity.

## Computational Infrastructure and Programming Language
While students will have experience with another programming language such as Python or Matlab from their prerequisities, this course will be taught using [Julia](https://julialang.org/).  Beyond being an excellent language for technical computing for macroeconomics, Julia provides a new set of programming principles that will broaden the student's knowledge of computing.  This will help them students by both providing a better differentiated resume, broader skills, and more opportunities to work as a research assistant for researchers requiring significant computational expertise.

Students can install a Julia installation on their laptop by following [these instructions](https://julia.quantecon.org/getting_started_julia/getting_started.html).  While one can use Julia entirely from Jupyter notebook, we will also install VS Code and introduce basic github/vscode usage as well.

## Course Outline (by Week)
Note: a few of the linked lectures are currently in python, and a port is under way.
### Week 1: Introduction to Julia and programming for economics (LO1)

   - Topics include: [Getting Started](https://julia.quantecon.org/getting_started_julia/getting_started.html) and [Julia Essentials](https://julia.quantecon.org/getting_started_julia/julia_essentials.html)
   - At the end of the week students will have reviewed the basic setup of the Julia programming language and related it similar functionality in to Python or Matlab

### Week 2: Linear algebra and basic scientific computing (LO1)
   - Topics include [Arrays and Related Types](https://julia.quantecon.org/getting_started_julia/fundamental_types.html) and related topics in implementing [Linear Algebra](https://julia.quantecon.org/tools_and_techniques/linear_algebra.html).  In addition, students will review [Optimizers and Solvers](https://julia.quantecon.org/more_julia/optimization_solver_packages.html).  Interested students can review bonus material in [Generic Programming](https://julia.quantecon.org/getting_started_julia/introduction_to_types.html) but it wouldn't be required or tested.
   - At the end of the week students will feel comfortable: working with matrices, vectors, and arrays; solving linear systems and calculating eigenvalues; optimizing unconstrained and constrained functions; and solving systems of equations.
### Week 3: Geometric Series and Stochastic Processes (LO2)
- Topics include [Geometric Series](https://julia.quantecon.org/tools_and_techniques/geom_series.html) [Dynamics in One Dimension](https://python.quantecon.org/scalar_dynam.html)
- At the end of the week students will understand how to calculate present discounted values, work with keynesian money-multipliers, and simulating random processes.
- **Problem Set 1 Due** - basic loops, linear algebra, and optimization problems.
### Week 4: Dynamics of Wealth and Distributions (LO2)
- Topics include [AR1 Processes](https://python.quantecon.org/ar1_processes.html) and [Wealth Distribution Dynamics](https://python.quantecon.org/wealth_dynamics.html)
- At the end of the week students will better understand ergodic distributions, measures of inequality, and simulating the dynamics of the wealth distribution.
### Week 5: Linear State Space Models Part (LO3)
- Topics include [Linear State Space Models](https://julia.quantecon.org/tools_and_techniques/linear_models.html)
- At the end of this week students will understand how to describe processes such as asset pricing and consumption smoothing as linear-state space models, simulate them, and calculate present-discounted values.
- **Problem Set 2 Due** - calculating present discounted values and simulating univariate asset pricing models, simulating and calculating dynamics of the wealth distribution.
### Week 6: Permanent Income Model (LO3)
- Topics include [The Permanent Income Model](https://julia.quantecon.org/dynamic_programming/perm_income.html)
- At the end of the week students will understand how to implement the classic consumption-savings model with linear-quadratic preferences in the LSS framework of the previous lecture, and to simulate permanent and transitory shocks to income.
### Week 7: Markov Chains (LO4)
- Topics include [Finite Markov Chains](https://julia.quantecon.org/tools_and_techniques/finite_markov.html)
- At the end of the week students will understand how to describe discrete-state stochastic processes as markov chains and simulate models of unemployment for a worker.
- **Problem Set 3 Due** - solving and simulating multivariate asset pricing problems in a LSS setup and exploring the permanent income model.
### Week 8: Models of Unemployment (LO4)
- Topics include the [Lake Model of Employment and Unemployment](https://julia.quantecon.org/multi_agent_models/lake_model.html)
- At the end of the week students will build on the previous tools of markov chains to look at a aggregated models of employment and unemployment in the economy.
- **Midterm in class**
### Week 9: Rational Expectations and Firm Equilibria (LO5)
- Topics include [Rational Expectations Equilibrium](https://julia.quantecon.org/multi_agent_models/rational_expectations.html)
- At the end of the week students will understand the core big K, little k insight for implementing price-taking agents and implement a model of firm dynamics.
### Week 10: Asset Pricing (LO5)
- Topics include [Asset Pricing with Finite State Models](https://julia.quantecon.org/multi_agent_models/markov_asset.html)
- At the end of the week students will understand pricing assets with payouts following the markov-chains of the previous lectures.
- **Problem Set 4 Due** - firm dynamic simulations and more on dynamics of markov chains.
### Week 11: Lucas Trees (LO5)
- Topics include [Asset Pricing with Finite State Models](https://julia.quantecon.org/multi_agent_models/markov_asset.html) and some of [The Lucas Asset Pricing Model](https://julia.quantecon.org/multi_agent_models/lucas_model.html)
- At the end of the week students will understand how to price assets with continuous rather than discrete payoffs.
### Week 12: Recursive Equilibria and the McCall Search Model (LO6)
- Topics include [The McCall Search Model](https://julia.quantecon.org/dynamic_programming/mccall_model.html)
- At the end of the week students will be able to define and solve basic models of labor market search.
- **Problem Set 5 Due** - asset pricing examples and a labor market search.
### Week 13: Cake Eating Problem (LO6)
- Topics include [Introduction to Optimal Savings](https://python.quantecon.org/cake_eating_problem.html) and [Numerical Methods for Solving the Cake Eating Problem](https://python.quantecon.org/cake_eating_numerical.html)
- At the end of the week students will be able to implement simple value-function iteration to solve a dynamic programming problem with a continuous set of decisions.
### Week 14: Cass Koopmans/Neoclassical Growth (LO7)
- Topics include [Cass Koopmans Planning Problem](https://python.quantecon.org/cass_koopmans_1.html)
- At the end of the week students will be able to solve for the transition dynamics of the planning problem for the Cass Koopmans/neoclassical growth model.
### Week 15: Optimal Growth Model (LO7)
- Topics include [Stochastic Optimal Growth Model](https://julia.quantecon.org/dynamic_programming/optgrowth.html)
- At the end of the week students will be able to solve growth models with a single type of good and stochastic productivity.
- **Problem Set 6 Due** - solving stochastic dynamic programming and simulating  transition dynamics of growth models.
- **Final Exam** - according to calendar schedule
- 
## Policies

**Missed Exam Policy:** You are responsible for ensuring that you take these exams as scheduled; no make-up exams will be given.
- Missing a midterm for ANY acceptable reason will result in its weight being automatically transferred to the final exam.
- The final exam date will be announced by Student Services about half-way through the term.
- There is no make-up final. Travel plans and/or cheap tickets are not a reason to miss the final. If you have a medical	or other compelling reason why you cannot take the final exam at its scheduled time you must follow the formal process and get an Academic Concession from your Faculty Advising Office (see below)

**Policy for Academic Concessions:**
Sometimes, things happen during the course of a semester that can affect your ability to succeed.  There are three main categories:
- Medical – i.e. you got sick and missed class or a chronic illness got worse
- Compassionate – i.e. a friend or close relative had something bad happen to them, or something bad happened to you.
- Conflicting Responsibilities – i.e. something happened in your personal life which is affecting your ability to do the work, like childcare falling through
You can read more about specific examples and the whole policy at:
http://www.calendar.ubc.ca/vancouver/index.cfm?tree=3,48,0,0

In all of these cases, UBC’s policy is to allow you to request an academic concession.  My policy is that all requests for academic concession on exams should be handled through your faculty Advising office (unless your office advises otherwise).  This is so that we can centrally track requests for concession and ensure they are fairly administered; it also helps protect your privacy.  You can find the procedure here, for Arts:

https://students.arts.ubc.ca/advising/academic-performance/help-academic-concession/

If you need a concession, you should immediately speak to Advising, who will follow-up with me to handle the academic side of things.  In-term concessions, which handle things like missed assignments or deadlines, are handled usually by extending the deadline or adjusting the final grading of the course (e.g. omitting an assessment).  Alternative forms of assessment may also be used if suitable and recommended by Advising.
•	Concessions need to be made in a timely fashion, which I will define as “within 2 weeks of the missed assessment” unless this is not reasonable.
You are also welcome to speak to me regarding your issue; I’m here to support you and help you get through things and be successful.  If you’re not sure if it’s something you should/could get a concession for, I can also give you a quick sense of what Advising will likely suggest if you’re unable to make an appointment immediately. 


**Academic Integrity**
It is the policy of the VSE to report all violations of UBC’s standards for academic
honesty to the office of the Dean of Arts. A detailed description of academic integrity,
including the University’s policies and procedures, may be found in the UBC Calendar:
Student Conduct and Discipline. In addition to the violations stated on that page (for
example, plagiarism), the VSE rules state that any student who hires a tutor/editor to help
with any portion of their work will be given an automatic grade of zero on their submitted
work. Any student found to have violated the university rules on academic misconduct
will receive a grade of zero on the relevant work. Further penalties, may be levied by the
President's Advisory Committee on Student Discipline. Those further penalties could
include a notation on your transcript indicating that you have committed an academic
offence, failure of the course, and/or suspension from the university.

**Academic Accommodation for Students with Disabilities**
The University of British Columbia recognizes its moral and legal duty to provide
academic accommodation. The University must remove barriers and provide
opportunities to students with a disability, enabling them to access university services,
programs, and facilities and to be welcomed as participating members of the University
community. The University’s goal is to ensure fair and consistent treatment of all
students, including students with a disability, in accordance with their distinct needs and
in a manner consistent with academic principles. The University will provide academic
accommodation to students with disabilities in accordance with the British Columbia
Human Rights Code, R.S.B.C. 1996, c. 210 and the Canadian Charter of Rights and
Freedoms, Part I of the Constitution Act, 1982, being Schedule B to the Canada Act 1982
(U.K.), 1982, c. 11. Provision of academic accommodation shall not lower the academic
standards of the University. Academic accommodation shall not remove the need for
evaluation and the need to meet essential learning outcomes. Students with a disability
who wish to have an academic accommodation should contact Centre for Accessibility
without delay (see UBC Policy 73).

**Conflicting Responsibilities**
UBC recognizes that students may occasionally have conflicting responsibilities that
affect their ability to attend class or examinations. These may include: representing the
University, the province or the country in a competition or performance; serving in the
Canadian military; or observing a religious rite. They may also include a change in a
student’s situation that unexpectedly requires that student to work or take responsibility
for the care of a family member, if these were not pre-existing situations at the start of
term.

Students with conflicting responsibilities have a duty to arrange their course schedules to
avoid, as much as possible, any conflicts with course requirements. As soon as
conflicting responsibilities arise, students must notify either their instructor(s) or their
Faculty Advising Office (e.g. Arts Academic Advising), and can request academic
concession. Instructors may not be able to comply with all such requests if the academic
standards and integrity of the course or program would be compromised.

Varsity student-athletes should discuss any anticipated and unavoidable regular-season
absences with the instructor at the start of term and provide notice of playoff or
championship absences in writing as soon as dates are confirmed.
Religious observance may preclude attending classes or examinations at certain times. In
accordance with the UBC Policy on Religious Holidays, students who wish to be
accommodated for religious reasons must notify their instructors in writing at least two
weeks in advance. Instructors provide opportunity for such students to make up work or
examinations missed without penalty.


**Policies and Resources to Support Student Success**
UBC provides resources to support student learning and to maintain healthy lifestyles but
recognizes that sometimes crises arise and so there are additional resources to access
including those for survivors of sexual violence. UBC values respect for the person and
ideas of all members of the academic community. Harassment and discrimination are not
tolerated nor is suppression of academic freedom. UBC provides appropriate
accommodation for students with disabilities and for religious and cultural observances.
UBC values academic honesty and students are expected to acknowledge the ideas
generated by others and to uphold the highest academic standards in all their actions.
Details of the policies and how to access support are available here
https://senate.ubc.ca/policies-resources-support-student-success.

**Statement regarding academic freedom**
During this pandemic, the shift to online learning has greatly altered teaching and studying at UBC, including changes to health and safety considerations. Keep in mind that some UBC courses might cover topics that are censored or considered illegal by non-Canadian governments. This may include, but is not limited to, human rights, representative government, defamation, obscenity, gender or sexuality, and historical or current geopolitical controversies. If you are a student living abroad, you will be subject to the laws of your local jurisdiction, and your local authorities might limit your access to course material or take punitive action against you. UBC is strongly committed to academic freedom, but has no control over foreign authorities (please visit http://www.calendar.ubc.ca/vancouver/index.cfm?tree=3,33,86,0 for an articulation of the values of the University conveyed in the Senate Statement on Academic Freedom). Thus, we recognize that students will have legitimate reason to exercise caution in studying certain subjects. If you have concerns regarding your personal situation, consider postponing taking a course with manifest risks, until you are back on campus or reach out to your academic advisor to find substitute courses. For further information and support, please visit: http://academic.ubc.ca/support-resources/freedom-expression  
