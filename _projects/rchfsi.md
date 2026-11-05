---
layout: page
title: R-ChFSI Eigensolver
description: a residual-based Chebyshev-filtered subspace iteration robust to inexact and low-precision operations
img: assets/img/projects/chebyshev-filter.png
importance: 2
category: Computational Method Development
related_publications: true
---

collaborators: Kartick Ramakrishnan, Prof. Phani Motamarri

{% cite kodali2025residualbasedchebyshevfilteredsubspace %}

Solving the large sparse eigenvalue problem that arises in every self-consistent-field iteration is the dominant cost of a Kohn-Sham DFT calculation. Chebyshev-filtered subspace iteration (ChFSI) is well suited to these repeated eigensolves: a Chebyshev polynomial of the Hamiltonian damps the unwanted part of the spectrum and amplifies the occupied subspace without a full diagonalization. However, standard ChFSI is sensitive to errors in the matrix-vector products it relies on. It can stall when the inverse of the overlap matrix in a generalized eigenproblem is only approximated, or when the filtering is carried out in reduced-precision arithmetic.

We introduced **R-ChFSI**, which recasts the Chebyshev recurrence in terms of residuals rather than direct eigenvector updates. This change damps the errors introduced by inexact products, and we derived convergence guarantees that hold under such approximations. As a result, R-ChFSI can:

- use inexpensive approximate inverses for generalized eigenproblems, where exact factorizations are prohibitively expensive;
- carry out filtering in low-precision arithmetic (FP32/TF32) on modern GPUs while still reaching tight double-precision tolerances;
- tolerate reduced-precision (BF16) inter-process communication in distributed sparse matrix-vector products.

On large finite-element DFT eigenproblems, R-ChFSI reaches residuals orders of magnitude below those of standard ChFSI when approximate inverses are used, and it meets tight target tolerances even in reduced precision, which makes its filtering substantially faster on GPUs than standard double-precision ChFSI. It is the mathematical foundation for the mixed-precision and compressed-communication strategies in our [exascale DFT work]({{ '/projects/exascale-dft/' | relative_url }}), and its idea of doing most of the work with inexpensive, inexact products carries over to our [selected-CI eigensolver]({{ '/projects/sbd-eigensolver/' | relative_url }}).

<div style="max-width: 480px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/chebyshev-filter.png" title="Chebyshev filter" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A Chebyshev polynomial stays bounded over the unwanted part of the spectrum while growing rapidly over the wanted eigenvalues, so applying it to a subspace amplifies the desired eigencomponents.
</div>
