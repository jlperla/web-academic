---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "How Inductive Bias in Machine Learning Aligns with Optimality in Economic Dynamics"
authors:
- Mahdi Ebrahimi Kahou
- Jesse Perla
- James Yu
- Geoff Pleiss
date: 2024-08-12T10:21:19-07:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2024-08-12T10:21:19-07:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: '**arXiv Working Paper**'
publication_short: ""

abstract: "This paper examines the alignment of inductive biases in machine learning
  (ML) with structural models of economic dynamics.  Unlike dynamical systems
  found in physical and life sciences, economics models are often specified by
  differential equations with a mixture of easy-to-enforce initial conditions
  and hard-to-enforce infinite horizon boundary conditions (e.g. transversality and no-ponzi-scheme
  conditions).  Traditional methods for enforcing these constraints are
  computationally expensive and unstable.  We investigate algorithms where those
  infinite horizon constraints are ignored, simply training unregularized kernel machines
  and neural networks to obey the differential equations.  Despite the inherent
  underspecification of this approach, our findings reveal that the inductive
  biases of these ML models innately enforce the infinite-horizon conditions
  necessary for the well-posedness.  We theoretically demonstrate that
  (approximate or  exact) min-norm ML solutions to interpolation problems are
  sufficient conditions for these infinite-horizon boundary conditions in a wide class of problems.  We then provide
  empirical evidence that deep learning and ridgeless kernel methods are not
  only theoretically sound with respect to economic assumptions, but may even
  dominate classic algorithms in low to medium dimensions.  More importantly,
  these results give confidence that, despite solving seemingly ill-posed
  problems, there are reasons to trust the plethora of black-box ML
  algorithms used by economists to solve previously intractable,
  high-dimensional dynamical systems---paving the way for future work on
  estimation of inverse problems with embedded optimal control problems."

summary: "This paper shows how kernel based methods can automatically fulfill long-run boundary conditions for dynamic economic models, and provide an alternative to classical methods - even in low dimensions."

tags: []
categories: []
featured: true

# Custom links (optional).
# links:
#   - name: Slides
#     url: 'symmetry_dynamic_programming_presentation.pdf'    

url_pdf: https://arxiv.org/pdf/2406.01898
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
  caption: "Solution to Optimal Advertising Model with Matern Kernels"
  focal_point: "Left"
  preview_only: false

projects: ["ML-high-dim"]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
