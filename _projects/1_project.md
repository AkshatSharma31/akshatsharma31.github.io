---
layout: page
title: Quantum Assembly Index
description: Quantifying molecular complexity through QTAIM electron-density topology, density-weighted graph paths, ring and cage contributions, and molecular symmetry.
img: assets/img/Fig_Final1.png
importance: 2
category: Computational & Theoretical Work
---

### Project Overview

Molecular complexity is commonly quantified using graph-theoretic indices, structural counts, and cheminformatic descriptors. However, these approaches do not directly incorporate the electronic structure and real-space organization of molecules. In this work, I introduce the **Quantum Assembly Index Aρ**, a parameter-free descriptor that quantifies the physical complexity of chemical architectures using the topology of the electron density.

The index combines density-weighted shortest-path organization within molecular topology graphs with ring and cage contributions derived from critical points identified through the Quantum Theory of Atoms in Molecules (QTAIM). Rotational symmetry is incorporated to account for repetitive and symmetry-equivalent structural organization. This formulation connects molecular connectivity with the electronic and topological features of the underlying quantum-mechanical density.

I evaluate Aρ across a chemically diverse benchmark spanning small molecules, pharmaceuticals, biomolecular assemblies, coordination clusters, and extended frameworks. The results demonstrate that molecular size alone is insufficient to characterize complexity: systems with comparable atom counts can exhibit substantially different index values depending on their topology, symmetry, and electronic organization.

### Methodology: Electron-Density Topology

The Quantum Assembly Index is constructed through three principal contributions:

- **Density-Weighted Graph Organization:** Represents atomic nuclei as graph nodes and bond critical point-mediated interactions as edges. Edge costs are derived from the electron density at bond critical points, and all-pairs shortest-path analysis quantifies the organization of the resulting graph.
- **Ring and Cage Contributions:** Incorporates ring critical points through mean bond ellipticity and cage critical points through Laplacian-based weighting normalized by enclosure size.
- **Rotational Symmetry and Topological Corrections:** Combines the contributions through symmetry normalization and a topological correction factor accounting for ring and cage closure.

Electronic structures are obtained using computational quantum-chemistry methods, followed by QTAIM analysis to identify and characterize the relevant critical points. The resulting quantities are integrated into a single dimensionless descriptor of molecular organization.

### Benchmarking and Predictive Performance

I compare Aρ with established cheminformatic descriptors, including Bertz complexity, the Balaban J index, Kier–Hall shape indices, connectivity indices, molecular weight, topological polar surface area, ring counts, and quantitative estimate of drug-likeness (QED).

The principal findings include:

- **Complexity Beyond Molecular Size:** The index distinguishes molecules of comparable size but different structural organization. For example, fullerene C₆₀ has a reported Aρ of 0.188, whereas an adenine–thymine base-pair assembly has a reported value of 15.861.
- **Comparative Classification Performance:** In the manuscript's binary classification benchmark, Aρ achieves a reported ROC-AUC of 0.960, compared with 0.839 for a model combining conventional descriptors.
- **Complementary Structural Information:** Correlation, feature-importance, and ablation analyses investigate the information captured by Aρ beyond conventional molecular representations.
- **Statistical Validation:** The study employs stratified cross-validation, repeated resampling, external holdout evaluation, and label-permutation testing to assess predictive performance and robustness.

### Computational Implementation

The computational workflow integrates electronic-structure calculations, QTAIM topological analysis, graph algorithms, and cheminformatic benchmarking. Molecular geometries are initially optimized using GFN2-xTB, while electron densities are evaluated using r²SCAN-3c or GFN2-xTB for very large systems, as described in the manuscript. QTAIM analysis is performed using Multiwfn, with graph construction and shortest-path calculations implemented using Python tools.

The principal computational limitation is the cost of generating suitable electron densities and performing complete topological analyses. The descriptor calculation itself is comparatively inexpensive once the required topological information is available.

The molecular geometries, computed Aρ values, and computational implementation are publicly available through the accompanying Zenodo repository.

### Significance and Future Directions

The Quantum Assembly Index provides a physically grounded complement to conventional molecular complexity descriptors by incorporating electron-density topology, ring and cage organization, and rotational symmetry. Its potential applications include molecular prioritization, cheminformatic analysis, virtual screening, and the development of machine-learning models informed by quantum-chemical structural features.

Future directions include evaluating the transferability of the descriptor across electronic-structure methods and molecular conformations, extending validation to larger chemical datasets, and developing surrogate models to enable its use in large-scale molecular screening.

**Publication:** [Quantifying the physical complexity of chemical architectures through electron-density topology — ChemRxiv](https://doi.org/10.26434/chemrxiv.15000864/v4)

**Code and data:** [Zenodo — Quantum Assembly Index, v1.0.0](https://doi.org/10.5281/zenodo.20592190)

**Keywords:** Quantum Assembly Index · QTAIM · Electron-Density Topology · Molecular Complexity · Graph Theory · Computational Chemistry · Cheminformatics
