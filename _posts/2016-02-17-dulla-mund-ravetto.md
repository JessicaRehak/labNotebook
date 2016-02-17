---
layout: post
categories: paper
title: Dulla, Mund, Ravetto, 2008
---

## The quasi-static method revisited

Authors:

* Sandra Dulla
* Ernest H. Mund
* Piero Ravetto

### Notes:

#### History

* Henry/Curlee (1958) found the quasistatic method (QSM)
* Yasinsky/Henry 1965 showed that adiabatic approach gave better
  results on loosely coupled two group diffusion descriptions
* Ott/Madell (1969) showed that overall errors could be greatly
  reduced by not ignoring the non-linear coupling between amplitude
  and shape. Created the IQM.

#### Algorithmic structure of IQM

1. PK parameters are evaluated through time interval Dt, assuming
   shape function has _not_ been modified. Then, amplitude eq may be
   solved through timesteps dt < Dt
2. Approximate time derivative by backwards difference. (IQM)
3. Evaluate the normalization condition.
4. Update the value of amplitude T
5. Iterate until convergence criterion for normalization condition
   error is met.

#### PCQM Method

* Uses the basic transport equations and PK equations
* Shape is a "convenient tool" to get the amplitude from the solution
  of the basic equations but isn't an _unknown_
* 
