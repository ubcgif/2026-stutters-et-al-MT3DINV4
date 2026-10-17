# Techniques for Improving MT Forward Simulations with Octree Meshes

Rylan Stutters<sup>1</sup>,
Wouter Deleersnyder<sup>1</sup>,
Santiago Soler<sup>1</sup>,
and Lindsey Heagy<sup>1</sup>

<sup>1</sup>University of British Columbia <br>

| | Information |
|---:|:----|
| Workshop | [MT3DINV4](https://mt3dinv4.mtnet.info/Home.html) |
| Task 1 | Forwad Modelling of a Sphere in a Half-Space |
| Abstract (PDF) | [Abstract in repo][abstract-pdf] |
| Presentation (PDF) | [PDF in repo][presentation-pdf] |

[abstract-pdf]: https://github.com/ubcgif/2026-stutters-et-al-MT3DINV4/blob/main/abstract/rstutters_MT3DINV4_abstract.pdf
[presentation-pdf]: https://github.com/ubcgif/2026-stutters-et-al-MT3DINV4/blob/main/abstract/presentation/rstutters_MT3DINV4_task1.pdf


## Abstract

Mesh refinement drives a tradeoff between accuracy and computational costs for Magnetotelluric forward modelling. We conduct simulations in the SimPEG framework to investigate this tradeoff and evaluate various Octree mesh refinement schemes against the analytic solution for a conductive sphere in a resistive halfspace. We also present volume averaging techniques to reduce inaccuracies associated with representing the sphere using discretized cells.
 
Two refinement scheme parameters are studied: refinement around the sphere and refinement around the receivers. Comparison to the analytic solution and computation time are used as figures of merit as these parameters are independently varied. The percent residuals of the simulated impedances follow a linear relationship as refinement is varied.
 
Volume averaging techniques are applied to the model by assigning conductivities based on the fraction of a cell which is enclosed within the sphere. Methods favouring lower conductivities such as harmonic averaging were found to be more effective than methods favouring higher conductivities, such as geometric averaging. Using the method of harmonic averaging, the percent residuals above the sphere can be reduced by more than a factor of two. The submitted results leverage this technique to produce a model with impedance residuals under $1\%$ for low frequencies (up to 1 Hz) and under $5\%$ for the mid to high frequencies (up to 1 kHz), all while using less than half the computation time and memory required for an equivalently performing mesh built from the standard cutoff procedure.
 