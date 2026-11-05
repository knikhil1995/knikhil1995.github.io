---
layout: page
title: Matrix-Free Algorithms
description: hardware-aware kernels for higher-order finite-element matrix-multivector products on CPUs and GPUs
img: assets/img/CPUEO.jpg
importance: 7
category: Computational Method Development
related_publications: true
---

collaborators: Gourab Panigrahi, Debashis Panda, Prof. Phani Motamarri

{% cite panigrahi_fast_2023 %}

Hardware-aware algorithms for higher-order finite-element (FE) discretized matrix-vector products evaluate the action of an operator on the fly, reducing arithmetic and data-access costs compared to assembling sparse matrices. These matrix-free approaches exploit the tensor-product structure of the FE basis to evaluate integrals without constructing cell-level matrices. Existing implementations, however, are designed for operating on a single vector and are not well suited to the matrix-multivector products that dominate subspace-iteration eigensolvers.

We developed matrix-free algorithms for FE-discretized matrix-multivector products on multi-node CPU and GPU architectures. Batched evaluation with hardware-tailored batch sizes improves data locality and exposes more parallelism. On CPUs we use even-odd decomposition, SIMD vectorization and overlapping of computation with communication; on GPUs we overlap compute with data movement and reduce memory traffic through shared memory, constant memory and kernel fusion.

The implementation outperforms the baseline cell-matrix approach on both single- and multi-node CPU and GPU systems, for operator actions as well as for a model eigenproblem solved with Chebyshev-filtered subspace iteration, the eigensolver at the heart of [DFT-FE](https://github.com/dftfeDevelopers/dftfe) and of our [R-ChFSI]({{ '/projects/rchfsi/' | relative_url }}) work.
