# Case for suppport

Stuff that needs a doing:

## Introduction ( 1 paragraph )
  - Why NWs?
  - Why doping ( w.r.t. ion implantation )?
  - Why use O(*N*) DFT?
  - What are we doing?
  
## Novelty & Timeliness
  - Reference experimental work ( esp. Fukata-san )
    - How new is this field? ( doped NWs )
Whilst the Si-Ge heterostructures have been studied since the mid-70s, it is only in the last 13 years that growth of radial heterostructures (i.e. core-shell) has been possible due to advances in the experimental techniques. Core-shell NWs have several advantages over the other possible heterostructures: (i) better confinement of carriers due to sharp interfaces, (ii) carrier mobilities in Ge are higher than in Si. These make 
    - Why do we need to carry out work like this? ( limited experimental anaylysis available )
  - Large NWs needed to remove the finite size effects of doping and stress.
  - Ion implantation used as a standard method for doping semiconductors.
  - This is a completely novel simulation (*ab-initio* has been done on the smaller scales **AND** large scale with classical molecular dynamics)
  
## Methodology
  - O(*N*) DFT
The computational modelling will be based on linear scaling density functional theory (O(*N*) DFT), specifically, using the CONQUEST code. Linear scaling implies that the resources required to do calculations will scale linearly with system size, evidence for which will be given in the resource management section. DFT has been enormously successful in characterising materials and has already been used successfully to model Si/Ge NWs electronic structure. Our code uses many different basis set types, however for this project we will use pseudo atomic orbitals derived from pseudopotentials (here PBE functionals). The success of DFT, and the experience of the PI, will form the platform for the project. The PI has extensive experience with DFT modelling with CONQUEST, since he is the lead developer, though other codes such as VASP and QuantumEspresso will be used as a benchmark tool for testing purposes.
  - XL-BOMD ( cite papers Niklasson and Arita )
Molecular dynamics routines are often prone to energy-drift over extended periods of time due to the lack of time reversibily. This problem was initially addressed by Niklasson *et al*. However, because of time reversibility the propagation of the electronic degrees of freedom is also lossless. Small numerical errors or inaccurate initial boundary conditions will never disappear but propagate throughout the simulation. Exact time reversibility is therefore a potential problem for long-time simulations under “noisy” conditions since numerical errors can accumulate to large fluctuations. Exact time reversibility in the propagation of the electronic degrees of freedom may then lead to a substantial loss of accuracy, and in the worst case, to divergence. Using a revised scheme of extented Lagrange Born-Oppenheimer molecular dynamics, through the introduction of an external dissipative force term acting on the electronic degrees of freedom, error accumilation has been removed.
  - PAOs (and testing L-range? Not sure if this should go here or the later section "Basic plan")
In order to ensure rapid calculations we have chosen to use pseudo-atomic orbitals (PAOs) as our basis set. These are numerically tabulated radial solutions to the Schrodinger equation using pseudopotentials, where each angular momentum channel is given *n* functions, where *n* = 1,2,3... and refers to the size of the basis set, i.e. single zeta = 1 etc. To use these functions, and indeed to find the solutions to the Schrodinger equation, we multiply these by the appropriate spherical harmonic. Each of these radial functions needs to be hand tuned to ensure we get accurate forces and band eigenvalues. To do this we usually benchmark against VASP for using approriate test systems, e.g. bulk/surfaces of Si/Ge and doped bulk/surfaces of Si/Ge. During this benchmarking process we converge the L-matrix range which converges the total energy in a similar fashion to the way the plane-wave cutoff converges a VASP calculation. At this point in time we already have a good set of PAOs for the system for single zeta polarisation up to tripple zeta triple polarisation, although we will need to test these for suitability in the proposed calculations. 
  
## Basic plan
( This is in part covered by Dave's notes RE the timeline )
  - What will we do? 
  - How will we do it? 
  - Contingency plans
  
## Why do we need to use ARCHER?

Given the approximate sizes of the jobs highlighted in the technical assessment (~16,000 cores or ~10% of total cores), ARCHER really is the only machine large enough to perform these sorts of calculations within the UK. In addition to this, the environment, libraries etc, provided on ARCHER will allow us to tune and run CONQUEST to its fullest potential. Since the proposed calculations will be amoung the largest ever done, certainly for *ab-initio* molecular dynamics, the high speed interconnects on ARCHER are a requisite to achieve the scaling required for such massive calculations.


A S Torralba et al 2008 J. Phys.: Condens. Matter 20 294206
