---
title: "Erosion Thickness on Medial Axes of 3D Shapes"
date: "2018-05-09"

draft: false
authors: ["Yajie Yan", "Kyle Sykes", "Erin Chambers", "David Letscher", "Tao Ju"]
publication: "ACM Transactions on Graphics (Proc. SIGGRAPH 2016)"
publication_short: ""

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags: ["medial-axis"]

# Optional external URL for project (replaces project detail page).
external_link: ""

# Does the project detail page use math formatting?
math: true

# Does the project detail page use source code highlighting?
highlight: true

# Featured image
image:
  caption: ""
  focal_point: "Center"
  preview_only: true
  placement: 

summary: "An efficient global significance measure on Medial Axes to differentiate major structures from noises"

---

{{<figure alt="" src="/et_sig16/et_teaser.png" title="Figure 1. The medial axis of a bumpy dolphin shape contains numerous noisy branches (left). Our measure properly highlights the important subset of the medial axis (middle). Guided by the measure, a skeleton is generated that features both surfaces and curves capturing planar and tubular parts of the shape.">}}

### Abstract
While playing a fundamental role in shape understanding, the medial axis is known to be sensitive to small boundary perturbations. Methods for pruning the medial axis are usually guided by some measure of significance. The majority of significance measures over the medial axes of 3D shapes are locally defined and hence unable to capture the scale of features. We introduce a global significance measure that generalizes in 3D the classical Erosion Thickness (ET) measure over the medial axes of 2D shapes. We give precise definition of ET in 3D, analyze its properties, and present an efficient approximation algorithm with bounded error on a piecewise linear medial axis. Experiments showed that ET outperforms local measures in differentiating small boundary noise from prominent shape features, and it is significantly faster to compute than existing global measures. We demonstrate the utility of ET in extracting clean, shape-revealing and topology-preserving skeletons of 3D shapes.

### Gallery

{{<figure alt="" src="/et_sig16/gallery.png" title="Figure 2. Gallery of 12 shapes organized by columns. The surface, ET, curve-only skeleton and hybrid skeleton are shown for each shape by rows. See the supplementary material for complete results.">}}

### Downloads

+ Paper: [`author version`](#)
+ Supplementary: 
    - {{%staticref "et_sig16/et_sup.pdf"%}} `proof` {{%/staticref%}},
    - [`gallery(html)`]({{<ref "et_gallery.md">}})
+ Example meshes: {{%staticref "et_sig16/data.zip"%}} `data` {{%/staticref%}}
+ Tool:
{{%staticref "et_sig16/et.v2.zip"%}} `exe` {{%/staticref%}},
[`readme`]({{<relref "readme.md">}})