---
layout: page
title: Matrix-Free Algorithms
description: for Higher-Order Finite-Element Discretized Matrix Multivector Products
img: assets/img/CPUEO.jpg
importance: 1
category: Computational Method Development
related_publications: true
---

collaborators: Gourab Panigrahi, Debashis Panda, Dr. Phani Motamarri

{% cite panigrahi_fast_2023 %}

Recent advancements in hardware-aware algorithms for higher-order finite-element (FE) discretized matrix-vector multiplications have shown that on-the-fly matrix-vector products can reduce arithmetic complexity and enhance data access efficiency. These matrix-free approaches exploit the tensor-structured FE polynomial basis for integral evaluations without explicit cell-level matrix construction. While the existing implementations of such algorithms are well-suited for the action of FE-discretized matrices on a single vector, they are not directly applicable to matrix-multivector products involving multiple vectors. To address this limitation, we have proposed a computationally efficient and scalable matrix-free implementation procedure for computing FE-discretized matrix-multivector products on multinode CPU architectures. Our implementation achieves significant speedups of up to 4.4x compared to baseline cell-matrix implementation when utilizing 1024 vectors and FE interpolating polynomial orders ranging from 6 to 8. The observed speedups underscore the potential of our matrix-free implementation to enhance the overall performance of subspace-iteration methods used in solving the Kohn-Sham eigenproblem incorporating non-collinear spin and spin-orbit coupling on multinode CPU and GPU architectures.
