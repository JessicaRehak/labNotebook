---
layout: post
categories: meeting
title: Bethany Goldblum Colloquiem
---

### Presentation
Scintillator Characterization for Neutron Detection

### Speaker
Bethany L. Goldblum

* Grad school/postdoc/staff at UCB
* Director of the Nuclear Policy Working Group
* Leader of Bay Area neutron group
* Nuclear forensics, structure, data

#### Organic Scintillators

* Work at the 88-in cyclotron
* Use scintillators for fast neutron detection, emit light due to
  elastic scattering -> organic scintilator (uses Carbon)
* Molecules are excited and de-excite to singlet bands via collisions,
  vibrations, etc
* Singlets de-ecite via flouresence
* Spin flip transition may lead to excited _triplet_ state that
  de-excite via phosphoresence on much longer time scales. This is
  hindered by that required spin-flip.
* Of the properties of scintillators, will focus on light conversion,
  and decay time

#### Characterization Techniques

* Can fit decay curves with multi-componant exponentials, fit the data
  really well. No physical basis for this functional form. Would like
  a _physics based_ model.
* Determination of light yield takes a long time, don't indicate any
  error, so you can't tell if they match. Identified the edge of the
  pulse-height distribution to identify the incident neutron energy
  (the neutron can pass at most all of its energy to the proton).
* Different sized cylinders give different answers, 5", 2",
  etc. Values are a little different based on cylinder size.
* A lot of discrepancies: models have issues, not measuring the
  radiation of interest directly (requires the neutrons to create
  protons)

#### Work

* Created a model-independant way of identifying light yield.
* In cave 0 at cyclotron, created an open air beam of neutrons
* Two different deuteron energies, Ed = 16 MeV and 44 MeV. Can tailor
  the spectrum and intensity of the source using diffrent materials
  for the breakup target.
* Moved a scintillator around to identify the size of the beam. 

#### (0.5%) Stilbene Doped Bibenzyl Single-crystal Scintillator

* Intensity of light changes by orders of magnitude over nanoseconds
* Use temporal difference between the two PMTs to recreate the
  original waveform.
* High suppressed triplet-triplet annihilation
* Can model the flourescence rate well
* Used in nTOF diagnostics at NIF
* Created a _physics-based_ method of identifying the light response

#### Light Yield Characteristics

* In the cyclotron, because it is a cycle, you have a contribution in
  each cycle from the previous cycle (slower neutrons). This makes TOF
  measurements difficult.
* Neutrons elastically scatters at scintillators and is detected in
  scattering cells.
* Use the angle and TOF to calculate the energy of the incident
  neutron _and_ the proton energy deposited -> light yield directly.
* Don't know what cyclotron pulse each neutron comes from
* Can use kinematics to use angle and TOF to identify which RF pulse
  it came from, to reduce error -> reject criteria.
* Compare nTOF and kinematically-calculated TOF to get "clean
  determination" of incoming nTOF.
* Can get Light Yield v. Proton Energy: bins are equally spaced in
  _time_ due to resolution of ~4 ns
* Can now compare this to the data. Will use a MC approach to get
  systematic error in y-axis.
* This is a model independent approach, measurement can be made in 48
  hours, reduces systematic bias _and_ can go to very low proton
  energies.
