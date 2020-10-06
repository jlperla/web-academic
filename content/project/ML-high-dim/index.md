---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Machine Learning and High Dimensional Economics"
summary: "Tools and applications from computer science/statistics/math for modeling heterogeneity, information diffusion, and high-dimensional learning"
tags: []
categories: []
date: 2020-09-16T0:03:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
My interest in [information diffusion]({{< ref "/project/information-diffusion/index.md" >}}) and [computational economics ]({{< ref "/project/datascience-computational/index.md" >}}) led me to examine better ways to deal with high-dimensionality in macroeconomics taking inspiration from computer science, statistics, and computational sciences literature.

The broad goals of this research agenda are to:

   - attack the curse of dimensionality in macroeconomics by **combining** economic models with new machine learning techniques.
   - tie together models of statical learning from the agent's perspective given non-trivial heterogeneity (i.e., using "learning" models from computer science/statistics literature **inside of** the agent's problem, where the state may have high degrees of heterogeneity).  The main applications are models of [learning and inference in finance]({{< ref "/project/financial-frictions/index.md" >}}).
   - chase especially useful spillovers that may come along the way (e.g., high-dimensional fixed-effects and sojourns into Bayesian methods).

For macroeconomics, this hybrid approach is especially important: we need to use the flexible non-parametric features of neural networks/deep learning with constraints and models that come out of economics. As an analogy, consider "Physics Informed Neural Networks" and [scientific machine learning](https://sciml.ai/).

For more background, watch this excellent keynote from [Karen Willcox](https://kiwi.oden.utexas.edu/)
{{< youtube Bk4PJnjuPps >}}.

I am on the Advisory Committee of the NumFOCUS supported [SciML](https://sciml.ai/) organization created to unify the packages for scientific machine learning.
