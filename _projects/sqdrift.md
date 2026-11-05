---
layout: page
title: Randomized Krylov Quantum Diagonalization
description: randomized time-evolution circuits that make sample-based quantum diagonalization practical for large molecules
img: assets/img/projects/sqdrift-circuits.png
importance: 2
category: Quantum Computing for Chemistry
related_publications: false
---

collaborators: IBM Research, TCS Research, Prof. Phani Motamarri

_Ongoing work._

[Sample-based quantum diagonalization]({{ '/projects/sqd-iron-sulfur/' | relative_url }}) is only as good as the configurations the quantum computer provides. SqDRIFT generates them from time-evolution circuits under the molecular Hamiltonian, built by randomly sampling Hamiltonian terms (the qDRIFT method). Because these circuits approximate a Krylov space of the Hamiltonian, the method inherits convergence guarantees that heuristic circuit ansätze lack. For large active spaces, however, faithful time evolution is far too deep for today's processors.

This project aims to make SqDRIFT practical for large, strongly correlated molecules on current hardware: sampling the terms that matter most for the state at hand, keeping the circuits shallow, choosing the evolution times, and feeding the best configurations from the classical diagonalization back into later rounds of sampling. We test it on [4Fe-4S] on IBM Heron processors and, in simulation, on the iron-molybdenum cofactor (FeMoco) at 152 qubits.

<div style="max-width: 720px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/sqdrift-circuits.png" title="Randomized circuits" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Three randomly drawn SqDRIFT circuits for [4Fe-4S] (72 spin orbitals, one per horizontal line). Each starts from a reference configuration (filled circles: occupied orbitals) and applies a short sequence of excitation terms sampled from the Hamiltonian.
</div>
