---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Information Diffusion and Heterogeneity"
summary: "Understanding the role of diffusion of knowledge, information, and ideas for the growth of firms and economies"
tags: []
categories: []
date: 2020-09-16T0:04:00

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
At the core of most of my research are (1) models of heterogeneity in knowledge/ideas/information; and (2) frictions and sources of diffusion that prevent convergence towards homogeneity - and the aggregate implications.

Some of the questions I have tackled from this perspective include how does:

1. innovation and technology diffusion interact to endogenously determine the shape of productivity distribution and generate aggregate growth?
2. an industry evolve as information diffuses to grow the network of connections between firms and consumers?
3. heterogeneity of information lead to market power in product and financial markets that are not fully Walrasian?

## Background

Over the last few decades, Macroeconomics has made enormous progress on being able to understand the role of heterogeneity of state (e.g., wealth, income, productivity), but is only starting to make significant progress on heterogeneity of information.  Part of the issue is that our computational methods become tractable precisely because Walrasian markets make any sort of information fully revealing - thereby radically decreasing the complexity and dimensionality of the problem.

While there are tricks that I and others have used to deal with these issues in specific cases, we need new computational and theoretical methods to tackle this problem without compromising essential economics.  In addition, since many of these problems involve an agent learning and forecasting, we need to expand our set of tools for "within-model" inference.  Consequently, I am exploring tools from [scientific machine learning and high dimensional methods]({{< ref "/project/ML-high-dim/index.md" >}}), inspired by computer science, statistics, and computational sciences literature.  My plan is to move towards applications with [implications for real financial frictions]({{< ref "/project/financial-frictions/index.md" >}}) arising from "within-model" inference.
