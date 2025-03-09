---
layout: page
title: Non-Collinear Magnetism and SOC
description: a scalable finite-element framework for ab-initio modelling of Non-Collinear Magnetism and Spin-Orbit Coupling in pseudopotential DFT
img: assets/img/ncsoceqns.png
importance: 2
category: Computational Method Development
related_publications: true
---

collaborators: Dr. Phani Motamarri

{% cite kodali2024finiteelementmethodsnoncollinearmagnetism %}

Spin-orbit coupling is a fundamental and complex relativistic effect that plays a crucial role in a wide range of experimental phenomena, including magnetic anisotropy, phosphorescence, and spin-orbit torque. This effect is important in various active research areas, such as spintronics, low-dimensional materials, topological insulators, materials for quantum computing. The utilization of pseudopotential DFT has been shown to be effective in predicting various material properties when extended to account for non-collinear magnetism and spin-orbit coupling. To this end, we have derived a real-space formulation for non-collinear magnetism with spin-orbit coupling using ONCV (Optimised Norm Conserving Vanderbilt) pseudopotentials and developed an efficient, scalable finite-element-based methodology, tailored for both multinode CPU and GPU architectures. The proposed method utilizes the FE cell-matrix approach to evaluate the matrix multi-vector products encountered during the iterative solution of the Kohn-Sham eigenproblem to increase the arithmetic intensity of the underlying computations. We further intend to develop hardware-aware strategies to accelerate further the underlying iterative eigensolver used to solve the FE discretized Kohn-Sham eigenproblem by employing a matrix-free approach to compute these matrix multi-vector products. Furthermore, we aim to derive and implement a generalized force approach for evaluating atomic forces and unit-cell stresses in a unified computational framework for geometry optimization involving non-collinear magnetism with spin-orbit coupling.
