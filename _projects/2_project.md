---
layout: page
title: Non-Collinear Magnetism and SOC
description: a scalable finite-element framework for ab-initio modelling of Non-Collinear Magnetism and Spin-Orbit Coupling in pseudopotential DFT
importance: 2
category: Ongoing work
collaborators: Dr. Phani Motamarri
related_publications: theurich_self-consistent_2001, hamann_optimized_2013, motamarri_configurational_2018

---

Spin-orbit coupling is a fundamental and complex relativistic effect that plays a crucial role in a wide range of experimental phenomena, including magnetic anisotropy, phosphorescence, and spin-orbit torque. This effect is important in various active research areas, such as spintronics, low-dimensional materials, topological insulators, materials for quantum computing. The utilization of pseudopotential DFT has been shown to be effective in predicting various material properties when extended to account for non-collinear magnetism and spin-orbit coupling. To this end, we have derived a real-space formulation for non-collinear magnetism with spin-orbit coupling using ONCV (Optimised Norm Conserving Vanderbilt) pseudopotentials and developed an efficient, scalable finite-element-based methodology, tailored for both multinode CPU and GPU architectures. The proposed method utilizes the FE cell-matrix approach to evaluate the matrix multi-vector products encountered during the iterative solution of the Kohn-Sham eigenproblem to increase the arithmetic intensity of the underlying computations. We further intend to develop hardware-aware strategies to accelerate further the underlying iterative eigensolver used to solve the FE discretized Kohn-Sham eigenproblem by employing a matrix-free approach to compute these matrix multi-vector products. Furthermore, we aim to derive and implement a generalized force approach for evaluating atomic forces and unit-cell stresses in a unified computational framework for geometry optimization involving non-collinear magnetism with spin-orbit coupling.
