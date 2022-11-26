---
title: "Voxel Cores: Efficient, robust, and provably good approximation of 3D
  medial axes"
date: "2018-07-30"
draft: false
authors:
  - Yajie Yan
  - David Letscher
  - Tao Ju
publication: "ACM Transactions on Graphics (Proc. SIGGRAPH 2018)"
publication_short: ""
tags:
  - medial-axis
summary: "Medial Axes of voxel shapes with provably good geometry and guaranteed topology properties"
external_link: ""
math: true
highlight: true
featured: false

image:
  caption: ""
  focal_point: ""
  preview_only: true
  placement: 

header:
  image: ""
  caption: ""

---

{{<figure alt="flowchart of algorithm" src="/img/vc-flowchart.png" title="Figure 1. Breakdown of algorithm. Given a triangular mesh, we first convert it into a voxel shape, then extract the voxel core which is colored by the lambda measure, and finally output a pruned voxel core. The voxelization step is omitted if the input is already a voxel shape.">}}

## Abstract
We present a novel algorithm for computing the medial axes of 3D shapes. We make the observation that the medial axis of a voxel shape can be simply yet faithfully approximated by the interior Voronoi diagram of the boundary vertices, which we call the voxel core. We further show that voxel cores can approximate the medial axes of any smooth shape with homotopy equivalence and geometric convergence. These insights motivate an algorithm that is simple, efficient, numerically stable, and equipped with theoretical guarantees. Compared with existing voxel-based methods, our method inherits their simplicity but is more scalable and can process significantly larger inputs. Compared with sampling-based methods that offer similar theoretical guarantees, our method produces visually comparable results but more robustly captures the topology of the input shape.

## Algorithm

The input 3D shape to our algorithm can be a voxel representation (binarized volume), or a triangular mesh representing the surface of the shape. Then our algorithm generates the voxel core which approximates the medial axis of the shape. Both in theory and in practice, we are able to show voxel core captures the topology and is within provable proximity of the true medial axis of a voxel shape. Although for meshes such guarantees only hold theoretically, in practice we still observe a high success rate in delivering these promises. Below we show a flow chart that visualizes each step of our algorithm.

1. First, we voxelize the input triangular mesh (a) to obtain a voxel shape (b). Of course this step is omitted if the input is already a voxel shape.

2. We then extract the voxel core by computing the Voronoi diagram of the boundary voxel vertices interior to the voxel shape \(c\). In the figure the voxel core is colored by the lambda measure using a heat color scheme, with blue being low and red being high.

3. Finally we output the subset of the voxel core whose lambda value is below the user provided threshold (d) as the medial axis of the input shape. 

## Generating skeletons

The output of this project, i.e. Voxel cores can be futher simplified using [Erosion Thickness]({{<relref "publication/et/overview/index.md">}}). The output will be a skeleton featuring both curves and surfaces that capture tubular and planar regions of the shape.

## Downloads

- Paper: {{%staticref "vc_sig18/voxelma.pdf"%}} `pdf (author version)` {{%/staticref%}}
- Supplementary: {{%staticref "vc_sig18/voxelma_sup.pdf"%}} `pdf` {{%/staticref%}}
- {{%staticref "ma_data/bunny_from_voxelcore.zip"%}} `Data` {{%/staticref%}}
- Tool: {{%staticref "vc_sig18/voxelcore.zip"%}} `exe` {{%/staticref%}}, [`readme`]({{<relref "readme.md">}})

We provide the executable which implements the method. Please see the [`readme`]({{<relref "readme.md">}}) for details about using the tool.
