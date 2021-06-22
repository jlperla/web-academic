---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Exploiting Symmetry in High-Dimensional Dynamic Programming"
authors:
- Jesus Fernandez-Villaverde
- Mahdi Ebrahimi Kahou
- Jesse Perla
- Arnav Sood 
date: 2021-06-21T10:21:19-07:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-09-18T10:21:19-07:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: '**Working Paper**'
publication_short: ""

abstract: "We propose a new method for solving high-dimensional dynamic programming problems and recursive competitive equilibria with a large (but finite) number of heterogeneous agents using deep learning. The curse of dimensionality is avoided due to four complementary techniques (1) exploiting symmetry in the approximate law of motion and the value function; (2) constructing a concentration of measure to calculate high-dimensional expectations using a single Monte Carlo draw from the distribution of idiosyncratic shocks; (3) sampling methods to ensure the model fits along manifolds of interest; and (4) selecting the most generalizable over-parameterized deep learning approximation without calculating the stationary distribution or applying a transversality condition. As an application, we solve a global solution of a multi-arm version of the classic Lucas and Prescott (1971) model of investment under uncertainty. First, we compare the solution against a linear-quadratic Gaussian version for validation and benchmarking. Next, we solve nonlinear versions with aggregate shocks. Finally, we describe how our approach applies to a large class of models in economics."

# Summary. An optional shortened abstract.
summary: "We provide a new method for solving high-dimensional dynamic programming problems, and recursive competitive equilibria with a large (but finite) number of heterogenous agents. "

tags: []
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf:
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

projects: ["ML-high-dim"]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
