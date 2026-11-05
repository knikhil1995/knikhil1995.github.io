---
layout: page
title: Quantum Diagonalization of Iron-Sulfur Clusters
description: sample-based quantum diagonalization for strongly correlated iron-sulfur clusters on IBM quantum processors
img: assets/img/projects/sqd-heavy-hex.png
importance: 1
category: Quantum Computing for Chemistry
related_publications: false
---

collaborators: IBM Research, TCS Research, Prof. Phani Motamarri

_Ongoing work._

Iron-sulfur clusters such as [2Fe-2S], [4Fe-4S] and the iron-molybdenum cofactor (FeMoco) of nitrogenase are textbook examples of strongly correlated molecules: many nearly degenerate electronic configurations matter at once, and even the best classical methods struggle to describe them accurately. Sample-based quantum diagonalization (SQD) uses a quantum computer to sample configurations from a correlated quantum state, and a classical computer to diagonalize the Hamiltonian in the subspace those samples span.

This project improves each stage of that pipeline with one question in mind: what does it take for quantum samples to match, and eventually go beyond, the best classical selected configuration interaction methods? We work on

- circuits built from physically motivated starting points and mapped efficiently onto IBM's heavy-hex qubit layout;
- recovering useful configurations from noisy hardware samples;
- getting more accuracy out of the sampled configurations on the classical side;
- classical baselines at the same subspace size, so that the contribution of the quantum computer is measured fairly.

We test these ideas on [4Fe-4S] (54 electrons in 36 orbitals, 72 qubits) on IBM Heron processors. Two companion projects feed into this pipeline: [randomized Krylov circuits (SqDRIFT)]({{ '/projects/sqdrift/' | relative_url }}) for generating configurations, and a faster [selected-CI eigensolver]({{ '/projects/sbd-eigensolver/' | relative_url }}) for the classical diagonalization.

<div style="max-width: 640px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/sqd-heavy-hex.png" title="Circuit layout on IBM Heron" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Qubits of a 156-qubit IBM Heron processor used by a [4Fe-4S] circuit. Spin-up and spin-down orbitals sit on two chains; the interactions between them act on the couplers (green) where the chains meet.
</div>
