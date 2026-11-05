---
layout: page
title: Vacancies in Fe<sub>3</sub>GeTe<sub>2</sub>
description: Fe-vacancy-driven noncollinear magnetism in a van der Waals ferromagnet monolayer
img: assets/img/projects/fgt-monolayer.png
importance: 1
category: Novel Applications
related_publications: false
---

collaborators: Prof. Biplab Sanyal (Uppsala University), Prof. Phani Motamarri

_Manuscript in preparation._

Fe<sub>3</sub>GeTe<sub>2</sub> is a layered van der Waals ferromagnet that remains magnetic down to a single layer, making it a leading candidate for two-dimensional spintronics. Its magnetic properties are known to be sensitive to Fe deficiency, but a microscopic picture of how individual vacancies reshape the local magnetism has been missing. Answering this question requires large supercells together with a fully relativistic, noncollinear treatment of magnetism, a combination that has been computationally out of reach.

Using the [noncollinear finite-element DFT]({{ '/projects/2_project/' | relative_url }}) and [GPU algorithms]({{ '/projects/exascale-dft/' | relative_url }}) developed during my Ph.D., we carry out large-scale, fully relativistic noncollinear DFT calculations of Fe vacancies in monolayer Fe<sub>3</sub>GeTe<sub>2</sub>. We examine:

- which of the two inequivalent Fe sublattices vacancies prefer to form on;
- how a vacancy reconstructs the magnetic moments of the surrounding Fe atoms and how far this disturbance extends;
- the vacancy-induced canting of the spins away from the collinear ferromagnetic order;
- how pairs of vacancies interact with each other.

These calculations connect the composition sensitivity of Fe<sub>3-x</sub>GeTe<sub>2</sub> to a microscopic picture of defect formation and local magnetic order, and provide a reference for future studies of supported layers and heterostructures.

<div style="max-width: 380px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/fgt-monolayer.png" title="Fe3GeTe2 monolayer" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Side and top views of a single Fe<sub>3</sub>GeTe<sub>2</sub> monolayer (Fe: red, Ge: blue, Te: green).
</div>
