---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Differentiable State-Space Models and Hamiltonian Monte Carlo Estimation"
summary: 'We propose a methodology to take dynamic stochastic general equilibrium (DSGE) models to the data based on the combination of differentiable state-space models and the Hamiltonian Monte Carlo (HMC) sampler.'
authors:
- David Childers
- Jesus Fernandez-Villaverde
- Jesse Perla
- Christopher Rackauckas
- Peifan Wu 
date:  '2022-10-06'
doi: ""
lastmod: 2022-10-06T10:21:19-07:00
featured: true
draft: false

# Schedule page publish date (NOT publication's date).
publishDate: 2022-10-06T10:21:19-07:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types:
- 9
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: 'First and second order estimation of HMC vs. RWMH'
  focal_point: 'Left'
  preview_only: false

# Publication name and optional abbreviated publication name.
publication: '**NBER Working Paper**'
publication_short: ""

abstract: We propose a methodology to take dynamic stochastic general equilibrium (DSGE) models to the data based on the combination of differentiable state-space models and the Hamiltonian Monte Carlo (HMC) sampler. First, we introduce a method for implicit automatic differentiation of perturbation solutions of DSGE models with respect to the model's parameters. We can use the resulting output for various tasks requiring gradients, such as building an HMC sampler, to estimate first- and second-order approximations of DSGE models. The availability of derivatives also enables a general filter-free method to estimate nonlinear, non-Gaussian DSGE models by sampling the joint likelihood of parameters and latent states. We show that the gradient-based joint likelihood sampling approach is superior in efficiency and robustness to standard Metropolis-Hastings samplers by estimating a canonical real business cycle model, a real small open economy model, and a medium-scale New Keynesian DSGE model.

# Summary. An optional shortened abstract.
summary: "We propose a methodology to take dynamic stochastic general equilibrium (DSGE) models to the data based on the combination of differentiable state-space models and the Hamiltonian Monte Carlo (HMC) sampler."

tags: []
categories: []
featured: false

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

projects: ["ML-high-dim"]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
