---
layout: page
title: Eigensolvers with Approximate Products
description: a preconditioned eigensolver for selected configuration interaction that does most of its work with cheap, approximate Hamiltonian products
img: assets/img/projects/sbd-eigensolver.png
importance: 4
category: Computational Method Development
related_publications: false
---

collaborators: Prof. Phani Motamarri

_Ongoing work._

Selected configuration interaction (selected CI) methods describe strongly correlated molecules by choosing a subset of the most important electronic configurations and finding the lowest energy of the Hamiltonian in the space they span. The configurations can be chosen by classical heuristics or sampled on a quantum computer, as in sample-based quantum diagonalization; either way, for the molecules of interest the subspace holds tens of millions of determinants or more. The diagonalization, dominated by repeated Hamiltonian-vector products on GPUs, then becomes the main cost.

This project develops an inverse-free preconditioned Krylov eigensolver for these subspace problems, implemented in the GPU diagonalization library [SBD](https://github.com/r-ccs-cms/sbd). In the spirit of our [R-ChFSI eigensolver]({{ '/projects/rchfsi/' | relative_url }}), most of the work is done with an inexpensive approximation to the Hamiltonian, while a few exact products keep the final energy at full accuracy. On the largest subspaces we have tested, from small molecules to iron-sulfur clusters, the solver reaches the same accuracy about twice as fast as the Davidson method used by default.

<div style="max-width: 720px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/sbd-eigensolver.png" title="Exact and approximate Hamiltonian" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Magnitudes of the Hamiltonian matrix elements of N<sub>2</sub> (8 electrons in 8 orbitals) between determinants, exact (left) and with its small couplings removed (right). The eigensolver does most of its work with the cheaper approximate operator.
</div>
