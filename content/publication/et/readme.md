+++
title = "Erosion Thickness Readme"
date = "2022-06-14"
draft = false

# hide this page from listing anywhere but still
# allow it to be relref from other pages
[_build]
  list = 'never'
  publishResources = true
  render = 'always'

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["medial-axis"]

# Project summary to display on homepage.
summary = ""

# Optional image to display on homepage.
image_preview = ""

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = true

# Does the project detail page use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++
## Pipeline
************************
{{<figure alt="fig-pipeline" src="/img/et-pipeline.png" title="Figure 1. Pipeline for generating a hybrid skeleton (with surfaces & curves) from the given medial axis.">}}

Given the medial axis mesh (`.ply`) and the radius field defined on it (`.r`), we can use our GUI program to generate a hybrid skeleton (`.ply`), with surfaces (triangular faces) and curves (polygonal lines) controlled by thresholding the $ET_2$ and $ET_1$ measures separately.


## Preparing input
************************
One way to obtain medial axis and radius files for a triangular surface mesh is using our [VoxelCore]({{<ref "publication/voxelcore/overview/index.md">}}) method.

