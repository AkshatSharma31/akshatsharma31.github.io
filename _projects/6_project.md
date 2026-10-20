---
layout: page
title: Information-Theoretic Analysis of Molecular Dynamics
description: Analyzing lysozyme conformational dynamics using backbone RMSD, Ramachandran distributions, Rényi entropy, and probability-simplex representations.
img: assets/img/lysozyme_md.png
importance: 2
category: Computational & Theoretical Work
---

### Project Overview

This project investigates the conformational dynamics of hen egg-white lysozyme through a combination of atomistic molecular dynamics (MD) simulation and information-theoretic analysis. A 1-nanosecond production trajectory was generated in an explicit, neutralized solvent environment using GROMACS, providing a time-dependent dataset for examining protein structural fluctuations and coarse-grained conformational distributions.

The analysis combines conventional structural observables with an entropy-based description of backbone conformational sampling. Backbone root-mean-square deviation (RMSD) was used to characterize structural evolution, while Ramachandran dihedral angles were classified into three predefined regions to construct empirical probability distributions. These distributions were subsequently analyzed using Rényi entropies and represented geometrically on a two-dimensional probability simplex.

### Methodology

**1. Molecular Dynamics Simulation**

The hen egg-white lysozyme structure (PDB ID: 1AKI) was simulated using GROMACS 2023.3 under an Ubuntu Linux environment. The system employed the Amber99SB force field and SPC/E water model, with chloride ions added to neutralize the system. Following energy minimization, the system underwent 100 ps of NVT equilibration and 100 ps of NPT equilibration at a reference temperature of 300 K and pressure of 1 bar. An unrestrained 1 ns production simulation was then performed using a 2 fs integration timestep.

**2. Structural Stability Analysis**

Backbone RMSD was calculated relative to the reference structure to characterize conformational deviations throughout the production trajectory. A cumulative running average was compared with a reference average calculated from the final 20% of the trajectory. This comparison was used to assess temporal stabilization of the selected observable, rather than to establish equilibrium or ergodicity.

**3. Ramachandran-Based Coarse-Graining**

Backbone Φ and ψ dihedral angles were extracted from the trajectory and assigned to three predefined categories: an alpha-helix-associated region, a beta-sheet-associated region, and a residual category containing all remaining observations. The resulting empirical probability vector

\mathbf{p}=(p_1,p_2,p_3),\quad \sum_{i=1}^{3}p_i=1,

provides a compact representation of the sampled backbone-angle distribution.

**4. Information-Theoretic Analysis**

We calculated the Rényi entropy of order q from the empirical probability distributions, with Shannon entropy obtained in the limit \(q\to1\). The study examined the descriptor

Φ(q)=H_1+2(q-1)Hq-(2q-1)H2q,

for selected values of q. We used its temporal variation to characterize changes in the coarse-grained conformational distribution, without assuming that a plateau represents global entropy or complexity maximization.

**5. Probability-Simplex Visualization**

The three-state probability vectors were mapped onto a two-dimensional simplex, allowing changes in the relative populations of the predefined conformational categories to be visualized over time. The resulting path represents the evolution of empirical probability distributions across analysis windows, rather than the trajectory of an individual molecular configuration through the full conformational phase space.

### Key Findings

- **Temporal stabilization:** Backbone RMSD and its running average exhibit comparatively smaller changes during the later portions of the simulated trajectory.
- **Nonuniform conformational sampling:** The Ramachandran distribution shows concentrated populations in commonly sampled backbone-angle regions, particularly alpha-helix-associated conformations.
- **Entropy-based characterization:** The descriptor Φ(q) varies over the trajectory, with comparatively smaller changes in later analysis windows.
- **Probability-simplex representation:** The three-state probability distributions provide a compact geometric visualization of temporal changes in coarse-grained backbone conformations.
- **Methodological integration:** The workflow connects atomistic MD trajectory analysis with empirical probability distributions and information-theoretic descriptors.

### Computational Tools

- **GROMACS 2023.3:** Molecular dynamics simulation and trajectory analysis.
- **Amber99SB and SPC/E:** Protein force field and explicit solvent model.
- **Python, NumPy and Matplotlib:** Probability analysis, Rényi entropy calculations, and visualization.
- **RMSD and Ramachandran analysis:** Conventional structural observables for examining conformational evolution.
- **Probability-simplex mapping:** Geometric representation of coarse-grained empirical distributions.

### Significance and Future Directions

This project establishes a computational workflow for combining molecular dynamics with information-theoretic characterization of protein conformational sampling. By translating backbone dihedral-angle observations into probability distributions, it provides a compact way to track how coarse-grained structural populations change during a simulation.

The current results are best interpreted as a proof of concept. The 1 ns trajectory and three-state classification do not establish ergodicity, equilibrium sampling, or global complexity maximization. Future work will focus on longer simulations, independent trajectory replicas, statistical uncertainty and autocorrelation analysis, sensitivity to classification boundaries, and finer-grained or continuous representations of backbone conformations.
