---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Machine Learning and High Dimensional Economics"
summary: "Tools and applications from computer science/statistics/math for modeling heterogeneity, information diffusion, and high-dimensional learning."
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
My interest in [information diffusion]({{< ref "/project/information-diffusion/index.md" >}}) and [computational economics ]({{< ref "/project/datascience-computational/index.md" >}}) led to me examining better ways to deal with high-dimensions in macroeconomics taking inspiration from the computer science, statistics, and computational sciences literature.

The broad goals of this research agenda are to:
   - attack the curse of dimensionality in macroeconomics by **combining** the economic model with machine learning techniques (an analogy is the "Physics Informed Neural Networks", see [SciML](https://sciml.ai/)) for much more.
   - build models to tie together models of statical learning from the agent's perspective given non-trivial heterogeneity (i.e. using the "learning" models from the CS/Statistics literature **inside of** of the agent's problem, where the state may have high degrees of heterogeneity).  The main applications are models of [learning and inference in finance]({{< ref "/project/financial-frictions/index.md" >}}).
   - chase especially useful spillovers that may come along the way (e.g. high-dimensional fixed-effects and sojourns into Bayesian methods)

For macroeconomics, the analogy to "Physics Informed Neural Networks" and related scientific machine learning techniques is especially important, because it is a hybrid approach - using the flexible non-parametric features of neural networks/deep learning with constraints and models that come out of economics.

Watch this excellent keynote from [Karen Willcox](https://kiwi.oden.utexas.edu/) 
{{< youtube Bk4PJnjuPps >}}.    