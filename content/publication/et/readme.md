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
## Workflow
************************

ET GUI program contains three tabs: `file`, `visualization`, and `skeletonization`. A general work flow starts from importing input files, computes ET, MC, and skeletons under `skeletonization`, and interactive visualization through controls in both visualization and skeleton tabs.


0. **Preparing input**: One way to obtain medial axis and radius files for a triangular surface mesh is using our [VoxelCore]({{<ref "publication/voxelcore/overview/index.md">}}) method


1. **Import input files**: The medial axis mesh file (`.ply`) and the `.r` file that defines distance to the shape surface are required. A shape mesh (`.obj`) can be optionally provided for visualization purpose. Click button `load` to load and render the meshes, which enables the visualization sections for surface and MA (highlighted in orange). In this example, MA and R were computed by VoxelCore for the shape of bunny. VoxelCore also generates a voxelized shape which is used here for surface visualization. 
{{<figure alt="input_MA_and_R" src="/img/et-MA-R.png" title="Providing input files to ET program. MA colored by radius field is visualized.">}}

2. **Computing skeletons**: Next, go to `Skeletonization` and click `precompute` to computes all the measures used for generation of skeletons. Once finished, sliders are enabled to set thresholds for $ET_M$ and $ET_C$ to keep a subset of surfaces and curves above the thresholds. Click `create` to visualize the subsets. Finally, create `export` to write the resulting skeleton to a `.skel` file. In the figure two sample skeletons are shown with their thresholding values shown in the UI.
{{<figure alt="sample_skels" src="/img/et-sample-skels.png" title="Two sample skeletons and their corresponding thresholds.">}}

1. **Measures visualization**: All measures have been computed at this point, and can be rendered using controls in `Visualization`. Below we show two example measures, i.e. $ET_M$ and $ET_C$ on MA and MC respectively. These can be changed in the dropdown list of MA and MC visualizaion sections.
{{<figure alt="sample_measures" src="/img/et-sample-measures.png" title="MA and MC are colored by $ET_M$ and $ET_C$ respectively.">}}