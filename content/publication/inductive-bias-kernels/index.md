---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Solving Models of Economic Dynamics with Ridgeless Kernel Regressions"
authors:
- Mahdi Ebrahimi Kahou
- Jesse Perla
- Geoff Pleiss
date: 2025-10-02T10:21:19-07:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2025-10-02T10:21:19-07:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: '**arXiv Working Paper**'
publication_short: ""

abstract: "This paper proposes a ridgeless kernel method for solving infinite-horizon, deterministic, continuous-time models in economic dynamics, formulated as systems of differential-algebraic equations with asymptotic boundary conditions (e.g., transversality).  Traditional shooting methods enforce the asymptotic boundary conditions by targeting a known steady state---which is numerically unstable, hard to tune, and unable to address cases with steady-state multiplicity.
Instead, our approach solves the underdetermined problem without imposing the asymptotic boundary condition, using regularization to select the unique solution fulfilling transversality among admissible trajectories.  In particular, ridgeless kernel methods recover this path by selecting the minimum norm solution, coinciding with the non-explosive trajectory.
We provide theoretical guarantees showing that kernel solutions satisfy asymptotic boundary conditions without imposing them directly, and we establish a consistency result ensuring convergence within the solution concept of differential-algebraic equations. Finally, we illustrate the method in canonical models and demonstrate its ability to handle problems with multiple steady states."

summary: "This paper proposes a ridgeless kernel method for solving models in economic dynamics, formulated as systems of differential-algebraic equations with asymptotic boundary conditions."

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
