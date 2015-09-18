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
    - Why do we need to carry out work like this? ( limited experimental anaylysis available )
  - Large NWs needed to remove the finite size effects of doping and stress.
  - Ion implantation used as a standard method for doping semiconductors.
  - This is a completely novel simulation (*ab-initio* has been done on the smaller scales **AND** large scale with classical molecular dynamics)
  
## Methodology
  - O(*N*) DFT
  - XL-BOMD ( cite papers Niklasson and Arita )
  - PAOs (and testing L-range? Not sure if this should go here or the later section "Basic plan")
  
## Basic plan
( This is in part covered by Dave's notes RE the timeline )
  - What will we do? 
  - How will we do it? 
  - Contingency plans
  
## Why do we need to use ARCHER?

Given the approximate sizes of the jobs highlighted in the technical assessment (~16,000 cores or ~10% of total cores), ARCHER really is the only machine large enough to perform these sorts of calculations within the UK. In addition to this, the environment, libraries etc, provided on ARCHER will allow us to tune and run CONQUEST to its fullest potential. Since the proposed calculations will be amoung the largest ever done, certainly for *ab-initio* molecular dynamics, the high speed interconnects on ARCHER are a requisite to achieve the scaling required for such massive calculations.
