---
layout: page
title: Polymorphism & Phase Transformations
description: Quantitative evaluation of the solid-state crystallization kinetics, lattice metrics, and phase profiles of active pharmaceutical ingredients.
importance: 2
img: assets/img
category: Experimental Materials & Synthesis
---

### Project Overview
Conducted under the supervision of Prof. Soumyajit Roy at IISER Kolkata, this project explores the thermodynamic landscapes, crystallization kinetics, and polymorphic stability profiles of active pharmaceutical ingredients (APIs). Using Paracetamol and Ibuprofen as model systems, the research evaluates how thermal conditions, solvent-antisolvent dielectric choices, and local concentrations dictate unit cell geometry and phase transitions.

---

### Core Technical Milestones

#### 1. Isolation & Stabilization of Elusive Polymorphs
* **Paracetamol Phase Polymorphism:** Successfully evaluated transitions between the highly stable Form I, the metastable Form II, and the transient/unstable Form III.
* **Form II Isolation Protocol:** Synthesized the elusive Orthorhombic Form II from the Monoclinic Form I precursor. Form I (40 mg) was thermally converted to a molten state at its melting threshold of $169^\circ\text{C}$, insulated via aluminum foil wrap, and slowly quenched to $25^\circ\text{C}$ to form an intermediate amorphous glassy matrix. 
* **Controlled Recrystallization:** Dissolved the glassy mass into $1\text{ mL}$ of ethanol on a glass slide under a constant thermal pan delivery at $40^\circ\text{C}$ until saturation, triggering the spontaneous nucleation of characteristic needle-like Orthorhombic structures.

#### 2. Advanced Powder-XRD Analytics & Lattice Metrics
* **Peak Assignment & Spacing Extraction:** Evaluated a comprehensive matrix of experimental lines (Samples 8 through 38) against standard database reference files (CCDC Mercury PXRD profiles) to map intensity against 2-theta ($2\theta$) angles, assigning Miller indices ($h, k, l$) to discrete diffractive reflections.
* **Phase Discrimination Criteria:** Form I was diagnostic for intense, selective diffractive peaks at $2\theta = 23.48^\circ$ and $24.37^\circ$, whereas Form II formation was validated by a singular diagnostic marker reflection at $2\theta = 24.03^\circ$.
* **Crystallographic Mathematical Models:** Quantified interplanar lattice spacings ($d$) to map lattice strain profiles using the following structural geometric criteria:
  * **Monoclinic Lattice Condition:** ($\alpha \neq b \neq c, \alpha = \beta = 90^\circ \neq \gamma$) resolved via:
    $$\frac{1}{d^2} = \frac{1}{\sin^2\beta} \left( \frac{h^2}{a^2} + \frac{k^2\sin^2\beta}{b^2} + \frac{l^2}{c^2} - \frac{2hl\cos\beta}{ac} \right) \quad \text{}$$
  * **Orthorhombic Lattice Condition:** ($\alpha \neq b \neq c, \alpha = \beta = \gamma = 90^\circ$) calculated via:
    $$\frac{1}{d^2} = \frac{h^2}{a^2} + \frac{k^2}{b^2} + \frac{l^2}{c^2} \quad \text{}$$

#### 3. Colloidal Solution Profiling & Nucleation Pathways
* **Ibuprofen Solvation Assays:** Profiled how variation in local super-saturation affects crystallization pathways by establishing binary solutions of Ibuprofen in DMSO, followed by anti-solvent induction via Millipore water.
* **Concentration & Temperature Grids:** Mapped multiple variable environments (e.g., Sample 8 at $24\%$ concentration with $240\text{ mg}$ drug per $1\text{ mL}$ DMSO added to $1000\mu\text{L}$ water at $27^\circ\text{C}$; alongside Sample 11 at $8\%$ concentration executed across a thermal split of $17^\circ\text{C}$ and $27^\circ\text{C}$ using $200\mu\text{L}$ water).
* **Nucleation Diagnostics:** Followed sample homogeneity through sonication routines and used incident laser light scattering to determine Tyndall effects, confirming successful confinement into localized, highly active colloidal phases prior to isolation via vacuum drying and subsequent PXRD assignment.
