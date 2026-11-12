---
layout: about
title: about
permalink: /
subtitle: <a href='https://sites.google.com/view/matrix-lab'>MATRIX Lab</a>,<br>
  <a href='https://cds.iisc.ac.in'>Department of Computational and Data Sciences</a>,<br>
  <a href='https://iisc.ac.in'>Indian Institute of Science</a>

profile:
  align: right
  image: prof_pic.png
  image_circular: true # crops the image to make it circular
  more_info: >
    <p>310, CDS,</p>
    <p>IISc,</p>
    <p>Bangalore,560012</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am a National Quantum Mission postdoctoral fellow in the [Department of Computational and Data Sciences](https://cds.iisc.ac.in) at the Indian Institute of Science, where I completed my Ph.D. in November 2026 in the [MATRIX Lab](https://sites.google.com/view/matrix-lab) with [Prof. Phani Motamarri](https://sites.google.com/view/matrix-lab/bio-of-the-pi). My research sits at the intersection of computational physics, numerical linear algebra and high-performance computing: I develop fast, systematically convergent methods for simulating electrons in materials and molecules, and make them run efficiently on modern GPU supercomputers.

My Ph.D. work brings fully relativistic density functional theory (DFT), including [noncollinear magnetism and spin-orbit coupling]({{ '/projects/2_project/' | relative_url }}), to a real-space finite-element framework in the open-source [DFT-FE](https://github.com/dftfeDevelopers/dftfe) code. Along the way I designed the [R-ChFSI eigensolver]({{ '/projects/rchfsi/' | relative_url }}), which stays robust when matrix products are computed approximately or in low precision, and used it to enable [mixed-precision, compressed-communication DFT]({{ '/projects/exascale-dft/' | relative_url }}) on exascale machines such as Aurora and Frontier. I also work on [adaptive-coordinate finite elements]({{ '/projects/adaptive-fe/' | relative_url }}) that lower the cost of these calculations, and apply these tools to magnetic quantum materials such as [Fe<sub>3</sub>GeTe<sub>2</sub>]({{ '/projects/fgt-vacancies/' | relative_url }}).

More recently, I have been working on quantum computing for chemistry, using [sample-based quantum diagonalization]({{ '/projects/sqd-iron-sulfur/' | relative_url }}) and [randomized Krylov methods]({{ '/projects/sqdrift/' | relative_url }}) to study strongly correlated molecules such as iron-sulfur clusters on IBM quantum processors, in collaboration with IBM Research and TCS Research. Alongside this, I develop GPU eigensolvers for large problems in both settings: the [HEXA dense eigensolver]({{ '/projects/hexa-eigensolver/' | relative_url }}) for dense subspace problems such as those in large-scale DFT, and a [selected-CI eigensolver]({{ '/projects/sbd-eigensolver/' | relative_url }}) for the subspaces sampled in quantum diagonalization.
