---
title: 'Voxel Cores: Efficient, robust, and provably good approximation of 3D medial axes'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Yajie Yan
  - David Letcher
  - Tao Ju

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2018-08'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: "Voxel Cores: Efficient, robust, and provably good approximation of 3D medial axes"
publication_short: VoxelCores

abstract: We present a novel algorithm for computing the medial axes of 3D shapes. We make the observation that the medial axis of a voxel shape can be simply yet faithfully approximated by the interior Voronoi diagram of the boundary vertices, which we call the voxel core. We further show that voxel cores can approximate the medial axes of any smooth shape with homotopy equivalence and geometric convergence. These insights motivate an algorithm that is simple, efficient, numerically stable, and equipped with theoretical guarantees. Compared with existing voxel-based methods, our method inherits their simplicity but is more scalable and can process significantly larger inputs. Compared with sampling-based methods that offer similar theoretical guarantees, our method produces visually comparable results but more robustly captures the topology of the input shape.

# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: []

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: ""
  focal_point: ""
  preview_only: true
  placement: 

header:
  image: ""
  placement: 1
  caption: ""

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---