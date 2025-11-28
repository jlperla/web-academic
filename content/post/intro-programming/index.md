---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Advice on Learning Python"
subtitle: ""
summary: ""
tags: []
categories: []
date: 2025-11-20T07:13:10-07:00
lastmod: 2025-11-20T07:13:10-07:00
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
I am often asked (1) is it worth learning to code well, given how useful AIs are now; (2) are advanced undergrad/grad CS/Stats/Datascience courses a good way to learn to "code" better; and (3) if not, what resources do you suggest?

My short answers are: (1) yes; (2) no; and (3) if learning with projects or lecture notes isn't enough, then some online courses will help provide some accountability.

## Is it Worth Learning to Code Well?
Yes.  Even if you need to use an AI you need to be able to tell when it is making mistakes, and guide it towards a solution.  You may also be in a position where being able to write without an AI is essential (e.g., coding interviews).

Finally, for most classes in CS/datascience/etc. past the introductory level there is an expectation that you can write code at a fast pace and debug it effectively.  Without sufficient practice you would find it difficult to keep up with the pace of those classes.

And to be clear, in most undergrad and datascience courses R is taught as a set of statistical packages, and is not a programming language in the same sense.

## Are Graduate Computer Science/Stats/Datascience Courses a Good Way to Learn to "Code" Better?
No.  Those courses are intended to teach you about the "science" of computer science or statistics.  They expect you to already be fluent in coding.  This is true for most undergrad courses in CS as well (many students would know how to "code" in high school and can skip the first CS course).

## What Resources Do You Suggest?
If you are an undergrad, then there is an advantage in taking introductory courses with the CS department.  For example, UBC has **CPSC 103: Introduction to Systematic Program Design** which is an outstanding and accessible introduction intended for non-majors.  If you have never programmed before then do not worry, the course will be accessible.  After taking those types of courses, you may find you can get better at coding by just working hard on final projects of economics field courses.

Otherwise, learning by carefully going through sets of lectures carefully (e.g., [QuantEcon](https://quantecon.org/lectures/) has some good intro classes in Python) works for some people, but others find it difficult to stay motivated without some external accountability.  My personal feeling is that the more money it costs, the less likely it will be appropriate for academically oriented undergrads or masters students.

There are many online courses with various prices and technical levels.  Coursera Michigan has a [Python for Everybody](https://www.coursera.org/specializations/python) set of courses which are very popular.  However, I find that these are expensive (the auditing isn't as useful) and far too introductory for most econ students.  More generally, Coursera seems to be focused on professional development, and less on academic learning.  edX has more academic style courses, but there is also a lot of variation.

### Harvard's CS50 Courses
The best one I have found is also free.  Harvard and edX have put in an enormous amount of effort into the [HarvardX: CS50's Introduction to Programming with Python](https://cs50.harvard.edu/python/) which is attached to their [edX course](https://www.edx.org/learn/python/harvard-university-cs50-s-introduction-to-programming-with-python).  It is intended for non-CS majors and is very accessible (even for teenagers) but goes at a good pace.  A few other notable advantages:

- Unlike some "audit" for other courses, you get the full experience for free.  You submit assignments, problem sets, for auto-grading.
- You can get a [certificate of completion](https://cs50.harvard.edu/python/certificate/) for free when auditing the course if you submit the problem sets and final project.
- There is also a professional certificate for a fee (which would be on the official edX site), but it is unclear if that is worth the trouble.  Perhaps employers would value it, but most academics would not care about the "official" professional certificate vs. the free audit certificate.
- They have built up an [online VS Code environment](https://cs50.dev) with Microsoft that allows you to do all of your coding in a browser, submit problem sets and projects, etc. without any local installation issues.

See [how to take this course](https://cs50.harvard.edu/python/#how-to-take-this-course) for details on signing up for the appropriate course to audit without paying edX.

Other courses include:

- [HarvardX: CS50’s Introduction to Artificial Intelligence with Python](https://cs50.harvard.edu/ai/) looks great as a follow-up to the python course if you want to continue learning more advanced topics.  
- [HarvardX: CS50's Introduction to Computer Science](https://cs50.harvard.edu/x/) which is meant a a first course accessible for CS majors and non-majors, but covers a lot of material quickly.  See that page for links to the appropriate edX courses and certifications, but as with the Python course you can audit it for free, get access to all of the materials, and submit assignments for auto-grading by registering on edX.
