---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Recent Criticisms of Julia"
subtitle: ""
summary: "I agree with the general sentiment of much of the criticism, but it doesn't impact most use-cases of economists"
tags: []
categories: []
date: 2022-05-31T07:13:10-07:00
lastmod: 2022-05-31T07:13:10-07:00
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
There has been some posts from a developer on [why he no longer recommends Julia](https://yuri.is/not-julia/) and [longer discussions](https://discourse.julialang.org/t/discussion-on-why-i-no-longer-recommend-julia-by-yuri-vishnevsky/81151) addressing his specific concerns.

My comments here should be narrowly applied to people writing code for economics research and not necessarily extrapolated to teaching or industry use, which have different tradeoffs.  Keep in mind the author says
> For many years I used the Julia programming language for transforming, cleaning, analyzing, and visualizing data, doing statistics, and performing simulations.

That statement is very important, and I would say that Julia does not compare favorably to alternatives there.  Something like R might be a better fit---or maybe a combination of R with Julia generating the simulations in files.

My take on how his comments apply to economic researchers solving models (i.e, not just teaching or cleaning data/visualizing/etc) are:
1. I agree with the sentiment of a lot of these criticisms although they don't affect economists in the same way as the authors use cases.
2. Economists should not misinterpret these and think that typical code they write is more likely to have problems with Julia than other languages.  It won't unless you are doing something especially advanced.  You may have bugs in your JMP, but they are very likely to be your own bugs!  In fact, julia has excellent [unit testing](https://julia.quantecon.org/software_engineering/testing.html) so with some discipline it might even be better than matlab/etc.
3. There are a lot of bugs in a lot of packages in Julia.  This is likely true of a random draw of a Python package as well, but the difference is that the core Python ecosystem packages are going to have far better testing.  Be cautious.
4. If you are using a particular package called [OffsetArrays.jl](https://github.com/JuliaArrays/OffsetArrays.jl) then you should be careful calling out to arbitrary packages.  But you probably haven't, and likely never should.
5. He also comments on issues on ML frameworks (e.g., reverse-mode auto-differentiation packages) of Julia.  There has been a sequence of hype and then lack of coordinated investment for years in the Julia community.  The people maintaining the existing frameworks are doing their best, but they are fighting "technical debt" since the existing packages don't seem designed to survive as long as they have.  This is a serious and a major impediment to some use-cases for Julia.  But that doesn't necessarily mean the Python frameworks are always preferable since they only cover a limited number of use-cases of AD.
6. His main points on how Julia's ground-up foundations on [generic programming](https://julia.quantecon.org/more_julia/generic_programming.html) make it especially difficult for integration testing of complicated packages are probably true.  But if you try not to get too fancy, it won't bite you.

## Do Not Choose a Single Programming Language

I do not think everyone should quickly move all of their code to Julia or Python or any other language.  For teaching, Julia is useful because it introduces different styles of programming to students and can help students learn [better algorithms](https://julia.quantecon.org/tools_and_techniques/numerical_linear_algebra.html) and how [source control](https://julia.quantecon.org/software_engineering/version_control.html) and [testing](https://julia.quantecon.org/software_engineering/testing.html) can lead to more reproducible research.  Afterwards, even if they use Python, Matlab, or R it will be with a broader experience.

For research: In all cases, you should ask what the alternative is for a particular use-case and what packages/algorithms exist.  You always want to use the best algorithms possible with the least amount of work/code on your part (subject to feasibility constraints with coauthors/RAs).

Purely as code, self-contained matlab/fortran/numba is almost always inferior to Julia in my mind, although not always worth the trouble to switch.  But hopefully we are not writing everything ourselves!  With packages it all depends:  Julia's differential equations frameworks in [SciML](https://sciml.ai/) are better than any other language, Python's deep learning frameworks dominates Julia in most cases.  R's statistics packages dominate Python and Julia for standard statistics/classic-ML.  Bayesian models in Stan are a lot easier than Julia or Python as long as the model fits in that framework.  I am even a big defender of Stata for applied-micro.  We should use the best language/ecosystem for the job, and Julia isn't always the best.
   

Is it ever the best language/ecosystem? At this point, while I have found many things in Julia frustrating, it is still the most elegant way to write many of the numerical algorithms that economists require, and in some cases has the best ecosystem out there.  With the exception of deep-learning, the only real alternative to me is just sticking with Matlab/Fortran/Python or whatever you are currently using, and waiting it out until you have a good reason to switch for a particular use-case.  If there is a package or algorithm you need which exists in Julia or Python, then that is a good enough reason.  Get into the mindset that you will use multiple languages.

The most important direct issue for me right now is for straightforward ML/auto-differentiation algorithms that don't require too much customization.  In those cases, I recommend using Python frameworks such as Pytorch for the foreseeable future.  If you are doing non-standard things or major customization of AD is required, then Julia might be the best option---but enter with your eyes open.  That said, getting fancy with JAX isn't especially easy either.

My feelings on this could change, and if deep learning ends up radically changing how we solve economic models (and it might, see [Exploiting Symmetry in High-Dimensional Dynamic Programming](https://www.jesseperla.com/publication/symmetry-dynamic-programming/symmetry-dynamic-programming.pdf), which is using Pytorch) then Julia's scope may narrow significantly.


A few more details on the specific concerns brought up in that document.

## AbstractArrays, OffsetArrays, and "Correctness"

Let me narrowly explain the issue and then give some broader thoughts.
- Julia is more generic than any other mainstream language, which is both its curse and its advantage.  See [introduction to types](https://julia.quantecon.org/getting_started_julia/introduction_to_types.html) and [generic programming](https://julia.quantecon.org/more_julia/generic_programming.html) for more details on what ``generic'' means.  Even something as simple as array indexing can be generalized.
- In particular, while you may think of Julia as having one-based indexing like Matlab, Mathematica, and most Fortran, it doesn't really have to.  So they wrote a package called [OffsetArrays.jl](https://github.com/JuliaArrays/OffsetArrays.jl) for people to have Fortran-style choice in indexing.  In principle, then, Julia could have zero-based or anything else.
- The problem is that while this works perfectly fine in most cases, if you pass these arrays to arbitrary packages, they may have been written to assume one-based indexing that is standard in Julia.  There are ways to write the code generically, and while many packages have done so, it is probably not worth it in many cases.
- For economists this should have no impact in practice.  The solution is simple: OffsetArrays is so niche and unnecessary that you don't need to use it, and if you do then don't call arbitrary packages with those arrays.

The broader point he is making, though, is an important one.  Julia does not enforce generic interfaces so there are far more places where integration testing is necessary to combine completely arbitrary packages than any other language.  This is a software engineering concern that has an impact on advanced usage and may be part of what is preventing Julia from fulfilling its full potential, but won't affect normal usage.  But it does mean you should be cautious combining multiple fancy packages together.

## Safety of Julia and How it Interacts with "Correctness"
Don't misunderstand the comments about the `@inbounds` macro.  It is part of a general point on the limitations of generic interfaces which are not strictly enforced, although I am not sure enforcing interfaces would have fixed this particular problem.
- This is narrowly an issue with the `OffsetArrays` and how it interacts with packages that assumed arrays start counting at one.  If you don't use that package, then don't worry about it.
- For the most part, with the exception of Rust and maybe Fortran, Julia is safer than all feasible alternatives  The least safe of all is C/C++ and hence Python indirectly since it is just a thin wrapper around C code in many cases.
- Furthermore, you can just run julia with `--check-bounds=yes` to disable these optimizations---as people always do in unit testing.

So I also wouldn't worry about this.  The issues with `@inbounds` discussed are an important point, but they are a question of generic programming language design rather than something that directly impacts typical users.  The alternatives in my mind (e.g., [Haskell typeclasses](https://www.haskell.org/tutorial/classes.html) and [C++ Concepts](https://en.wikipedia.org/wiki/Concepts_(C%2B%2B)) which applies to static generic programming) are enormous undertakings, so assume that nothing significant will change anytime soon---if ever.  These sorts of things require software-engineering discipline for package writers more than anything else.

## General Bugginess of Julia Packages and Code?
Is Julia and its ecosystem especially buggy and with poor code quality?  It can be (Zygote vs. Pytorch which has a huge team of professional developers), but:
- While many of the issues he is bringing up are legitimate bugs, they are often weird corner cases.  For example, using the [prod function to take the product of 32bit integers in a tuple](https://github.com/JuliaLang/julia/issues/39183) was not an issue if you have them in an vector or used the default integer type.  Similarly, he points out corner cases like histograms not working properly [if every single value is an identical Float64](https://github.com/JuliaStats/StatsBase.jl/issues/616).
- But I think the basic point he is bringing up is probably correct, just that it probably won't effect normal usage since these corner cases tend to occur with combining different generic types (e.g. his point about [alias not being checked with copyto! and UpperTriangular matrices](https://github.com/JuliaLang/julia/issues/39460).

I wouldn't run a self-driving car on Julia, but I would't worry too much about core Julia bugs for solving a dynamic programming problem.  Even if Julia's compiler is more likely to have a bug than a python interpreter, unless you are pushing the boundaries of generic programming they will be orders of magnitude less rare than your own bugs.

The broader issue of code quality of packages in Julia is important to keep in mind.  Be careful which packages you use and rely on.  This caution should apply to Python users as well since there are even more poorly-written packages there.  The difference is that the basic ones like numpy/etc. are pretty stable by this point.  Counting packages gives a distorted view of the ecosystem in both cases because most people use only a handful iof packages.

## Community and a Lisp curse

The author points out that
> The Julia community is full of capable and talented people who are generous with their time, work, and expertise.

Which is certainly the case.  I tend to agree with the author that the broader community/leadership does not always emphasize simple cases which lead to intuitively correct results with the same weights I would give it (e.g., [scoping](https://docs.julialang.org/en/v1/manual/variables-and-scoping/#On-Soft-Scope) being more important to get right than arbitrary-indexing of arrays).

Given the amount of code written by researchers, you need to be especially careful in how you choose packages.  This also applies to Python, but can sometimes be less of an issue since single frameworks such as Pytorch tend to combine more into one framework---and with significant software engineering resources.  In part this monolithic package approach is out of necessity since Python frameworks don't interoperate at all, and the C/C++ code behind them is tough to write.  Furthermore, since Python isn't generic and the frameworks can't easily coexist, there is very little "integration testing" required between packages, which helps lower the "testing surface".

I see plenty of evidence of the [Lisp Curse](http://www.winestockwebdesign.com/Essays/Lisp_Curse.html) in Julia.  This whole  [OffsetArrays.jl](https://github.com/JuliaArrays/OffsetArrays.jl)  debacle especially smells of this mindset.  Why not just admit Julia has one-based indexing like matlab, fortran, mathematica, R, and every other language emphasizing scientific computing?  Just because you **can** make a package for arbitrary indexing of arrays in Julia doesn't mean you **should**.

Making any serious package in Python is a big undertaking because you can end up writing much of it in C/C++ to get high performance.  With Julia you can whip up a half-functional AD system with good performance with a days work as soon as you understand the math and the basics of dynamic dispatching.  It is amazing, but that power can lead to people making all sorts of new projects with idiosyncratic tastes for features instead of contributing to existing ones.  In some cases that diversity is a good thing, but in others it is a disaster for users since they may not have a well-maintained baseline they can trust.

As for excess experimentation spreading resources thin in the community, I think it happens but it may be more similar to other languages than people realize.  Even though python packages can have massive numbers of users and lots of people submitting bugs, you will often find that the bulk of the code was written by only a handful of people.  An increasing number of maintainers sometimes only happens after things mature and stabilize.  The key problem is to ensure we take the right Julia packages over the finish-line to reach that maturity.

One thing that can help is to consolidate into common interfaces so that experimentation can happen in the background on algorithms rather than interfaces.  This is the SciML strategy (e.g., for example, [Optimization.jl](https://github.com/SciML/Optimization.jl) is a front-end which lets people swap out various backend algorithms, [AbstractDifferentiation.jl](https://github.com/JuliaDiff/AbstractDifferentiation.jl) can be used by those sorts of packages to swap out their gradient choices, etc.  For a user, this can be seamless and make it easy to try out all sorts of algorithms.