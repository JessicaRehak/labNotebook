---
layout: post
categories: paper
title: Ott Meneley 1969
---

## Accuracy of the Quasistatic Treatment of Spatial Reactor Kinetics - 1969

Authors:

* K. O. Ott (Perdue)
* D. A. Meneley (Argonne)

### Codes:

`QX-1`: quasistatic treatment of excursions

### Notes:

General problem: solution of the time-dependent multigroup diffusion
  equation

#### Modal/Nodal Method:

* Modal-method: "expansion of the time-dependent neutron flux into a
  series of time-independent modes or nodes with time-dependent
  coefficients."
* Sometimes coefficients are also dependent on energy.
* Nodal: Functions are only applied over nonoverlapping regions, index
  means the region, uses "coupling coefficients" for interaction
  between regions.

#### Factorization

* Factorization of total flux into amplitude and shape
* Another separation condition is required for t>0.
* Many can be used, only real requirement is that the shape function
  is positive and bounded for all points in space, energy, and time.
* Henry's condition fulfills those requires and allows transition to
  point kinetics formulation.
* Any weighting function can be used.
* Want strong coupling in only one direction for rapid convergence.
* Chosen splitting: space-energy shape of shape function depends only
  weakly on the amplitude function.
* Once reduced to the point kinetics equation form, the integral
  quantities (reactivity, beta, etc) must be averaged with the
  time-dependent shape function.
* Makes things more complicated, until you assume that the
  time-dependence of the shape function is of "lesser importance" than
  the time-dependence of the amplitude function.

##### Improved Quasistatic Approximation

* Replaces the derivative of the shape function by a backwards
  difference of the first order.
* Shape function is slowly varying: can apply first-order difference
  over a much larger deltaT than would be possible for the amplitude
  function
* Delayed source term is calculated directly from the flux history

##### Quasistatic Approximation

The time derivative is neglected entirely.

##### Adiabatic Approximation

* Does not distinguish the shape of the delayed neutron source from
  prompt.
* Ignores both time derivatives, uses eigenvalue to get stationary
  expression for the shape function.
* Ignores a lot of the coupling.
* Removal and source still depend on the total flux.

##### Adiabatic Approx. with Precomputed Shape Functions

* Ignores coupling of removal and source with total flux.
* Diff. eq. for amplitude and shape are completely independent, can
  pre-calculate time-dependent shape functions.
* Calculate shape functions for the time-dependent situation,
  calculate integral quantities, used as inputs to point kinetics to
  get amplitude function.
* "Point kinetics method"

#### Comparison of Quasistatic with others

* Quasistatic diverges from exact solution due to neglecting the shape
  function derivative, this can be improved via the IQM
* Adiabatic: significant errors without any real reduction in
  complexity.



#### Comparison methodology

* Accuracy of QSM is investigated by comparison with direct numerical
  solutions calculated by `WIGLE`
* Used two-energy-group slab systems
* Simulated excursions in a large water-cooled thermal rx and a fast
  reactor, three regions (I,II,III), center region has higher buckling
  to obtain a relatively flat initial flux"
* Transients modeled as linear increase in region I
* One-group delayed neutrons (beta 0.0084, lambda 0.08/sec)

#### Quasistatic Errors

* By ignoring the time derivative term, it is ignoring the finite
  transition time between the two different neutron population shapes.
* Implies you can estimate the error expressing it in terms of this
  "retardation"
* Error is only dependent on inserted reactivity and the degree of
  coupling.
* Errors can only be compared over the same flux rise.

### Conclusion/Summary

* Asymmetric insertions were applied to very loosely coupled systems.
* Errors in fast reactors excursions are <5%
* Errors in thermal reactors <80%
* QSM is sufficient for fast reactors, but not thermal reactors due to
  the slow flux-shape adaptation.
