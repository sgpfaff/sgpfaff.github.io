---
layout: page
title: Stellar Shell Formation
description: An investigation of how stellar shell formation is impacted by the presence of an oscillating central potential.
img: assets/img/prof.gif
importance: 1
category: undergraduate
permalink: /shells/
related_publications:

toc:
    sidebar: left
---

---
## **Detailed Overview**

With Dr. Tomer Yavetz at the Institute for Advanced Study, I investigate the influence of an oscillating central potential in the host galaxy on the formation of stellar shells. That's a lot of jargon, so I will break down each part in the following sections.
</br>

### Oscillating Central Potentials
Let's start with a the following simplified model of a galaxy.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic1.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

The circle in the middle with the squiggly line represents the visible matter of the galaxy. This is what you think of when you think of galaxies: spiral arms, a bar, stars, gas, etc. The dotted line surrounding the visible matter represents the [dark matter halo](https://en.wikipedia.org/wiki/Dark_matter_halo). Dark matter halos are known to exist from [rotation curve](https://en.wikipedia.org/wiki/Galaxy_rotation_curve) data. This diagram is not to scale, as in reality the dark matter halo is significantly larger than the visible part of the galaxy.

The conventional practice in galaxy research (disregarding unique cases such as spiral arms, bars, and subhalos) treats the potential and density of galaxies as static in time. In other words, the density of the galaxy only depends on *where* you are in the galaxy, not *when* you observe it. 

However, many theories predict that the central region of many galaxies have temporal density oscillations at small radii. Let's update the model we had before, adding a red circle for the region with oscillating density. For our purposes, we are only concerned with the dark matter halo, so I have removed the visible matter from the diagram.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic2.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

This effect is predicted for a halo of Fuzzy Dark Matter, an theorized ultralight form of dark matter that abides by quantum mechanics at galactic scales. We may see similar behavior with a rotating bar as well.

A [Navarro-Frenk-White (NFW) density profile](https://en.wikipedia.org/wiki/Navarro–Frenk–White_profile) is used for the outer region, since this density profile converges with Cold Dark Matter (the more conventionally used dark matter model) and observations at large radii. For the core density profile (the one that is fluctuating), we use a profile that is cusped (the reason why this is important is to resolve the [core cusp problem](https://en.wikipedia.org/wiki/Cuspy_halo_problem)). The core density is dependent on a scale radius, $$r_c$$, which varies to introduce temporal density oscillations in the central region.

$$
\rho(r, t) =
 \left\{
\begin{array}{ll}
    \rho_{CORE}(r,t), & r \leq r_{intersect}\\
    \rho_{NFW}(r), & r \geq r_{intersect} \\
\end{array}
\right.
=
 \left\{
\begin{array}{ll}
    \frac{0.019(m_a/10^{-22}eV)^{-2}(r_c(t)/kpc)^{-4}}{[1+0.091(\frac{r}{r_c(t)})^2]^8}, & r \leq r_{osc}\\
    \frac{\rho_0}{\frac{r}{R_s}(1+\frac{r}{R_s})^2}, & r \geq r_{osc} \\
\end{array}
\right.
$$

where 

$$r_c(t) = r_{c,0} sin(\frac{2 \pi t}{T_{osc}})$$. 

$$T_{osc}$$ is the period of density oscillation, which becomes an important parameter in interpreting our results. One way to visualize this density oscillation is to animate the density-radius plot over time. 

--> insert animation

Another way to visualize the evolution of the density is to make a color map with radius on the y-axis, time on the y-axis, and the color representing density.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/tables.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

Each vertical strip represents a snapshot of the relationship between radius and density at a specific time, while horizontal strips reveal how density changes over time at a specific radius.

Agreeing with intuition, the dynamical effect of this oscillating central potential on some structure in this galaxy is maximized when you are closer to the region of oscillation. Conveniently, very unique structure forms (in a static potential) when you merge a small galaxy with a larger galaxy on a trajectory that comes close to the center: stellar shells.
</br>

### Stellar Shells
Before moving forward, let's get some intuition for stellar shell formation and morphology. To start, consider the following setup: a dwarf galaxy (blue) merging with the dark matter halo of an elliptical galaxy on a radial trajectory (dashed blue). We refer to the smaller galaxy in this situation as the ***progenitor*** and the larger galaxy as the ***host***.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic3.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

The progenitor contains stars with different energies and angular momenta, both quantities that do not change through time with a static potential. The energy governs how long it takes a star to go from one apocenter (point of maximum radius in an orbit) to another, $$T_{orbit}$$, and the radius of apocenter. 
</br>

### Putting it all together
So, what happens to this static shell morphology when you introduce an oscillating central potential during its formation?
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic4.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div></br></br>
---
## **Brief Overview**
</br>

### Introduction
Stellar shells are concentric layers of stars encircling some galaxies. These shells are formed when a smaller progenitor galaxy merges with a larger host galaxy, a scenario most frequently observed in nature when the progenitor follows a highly eccentric orbit around the host galaxy [1].
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/shell_irl.jpg" title="Figure 1" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<div class="caption">
    **Figure 1.** Hubble image of the galaxy ESO 381-12, containing several stellar shells. Credit: NASA, ESA, P. Goudfrooij (STScI)
</div>

With Dr. Tomer Yavetz at the Institute for Advanced Study, I investigate the influence of an oscillating central potential in the host galaxy on the formation of stellar shells. The physical motivation for this investigation lies in the predicted behavior of galaxies with Fuzzy Dark Matter (FDM) halos. 

FDM is a proposed form of dark matter that is composed of ultralight scalar axions, with a de Broglie wavelength on the scale of approximately a kpc. Central oscillations in the seen in FDM simulations due to wave-like interference patterns [2].
</br>

### Methods
The host galaxy's potential was generated by creating a spherically symmetric density profile with a sinusoidally oscillating core and an NFW envelope [3] and solving the Poisson Equation, simplified for spherical symmetry.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/tables.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<div class="caption">
    **Figure 2.** Dynamic relationship between density, potential, and acceleration with respect to both time and radius. Each vertical strip represents a snapshot of these parameters at a specific time, while horizontal strips reveal how these properties change over time at a radius.
</div>

We conducted a test particle simulation using leapfrog integration, interpolating acceleration from the above table. The progenitor, with a mass $m_{prog} = 1.1 \times 10^4 M_{\odot}$, was populated with test particles normally distributed around its center. The host galaxy has a mass of $m_{host} = 1.1 \times 10^8 M_{\odot}$ [4].
</br>

### Results
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/T_convg.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<div class="caption">
    **Figure 3.** The top and bottom figures depict the 2D spatial distribution of test particle shells with differing central potential oscillation periods at 𝑡 = 15.24 𝑇!"#$%. Oscillation periods and the simulation time are represented in terms of the radial period of the progenitor base orbit, 𝑇!"#$% = 2.5 𝐺𝑦𝑟. The periods vary from significantly shorter periods than the time required to traverse the central region to substantially longer periods.
</div>

* As expected, the effect of the central potential oscillation is negligible in cases where the oscillation period is much greater or much less than the time for the progenitor to cross the central region (top left and bottom right cells of Figure 3). The shells formed in this regime are nearly identical to the typical shells formed in a static potential.

* Amplitude convergence tests show that the shells in the oscillating potential expand and contract around the static case (QR Code 2).
* Figure 3 shows that the oscillating central potential translates to varying the energy in the system, impacting the typical shell structure. In certain cases, this process leads to the formation of additional structure (new over densities, such as in the $T / T_{orbit}$ = 0.04 case) or a total destruction of structure (such as in the $T / T_{orbit}$ = 0.28 case).
</br>

### Conclusions
* One likely explanation for the changes to the typical shell structure is a resonance between the potential oscillation periods and the time to traverse the central region.
* An immediate next step is to use a realistic FDM potential produced from a full scale FDM simulation to see if the disruption is replicated.
* Stellar shell formation in an oscillating potential may also have implications outside of FDM, such as with other physical situations like a rotating bar.
* One future avenue is to identify observable signatures of an oscillating central region.
* An observable signature of this phenomenon could provide compelling evidence for FDM as a primary DM candidate.
* The next generation of telescopes, such as the Vera C. Rubin Observatory/LSST [5] and the Nancy Grace Roman Space Telescope [6], may allow us to probe shells around not only large galaxies, but also dwarf galaxies.
</br>

### References
[1]  Hendel, D., & Johnston, K. V. 2015, MNRAS, 454, 
      2472, doi: 10.1093/mnras/stv2035

[2]  Schive, H.-Y., Chiueh, T., & Broadhurst, T. 2014, 
      Nature Physics, 10, 496, doi: 10.1038/nphys2996

[3]  Yavetz, T. D., Li, X., & Hui, L. 2022, Phys. Rev. D, 
      105, 023512, doi: 10.1103/PhysRevD.105.023512
[4]  Price-Whelan, A. M., Johnston, K. V., Valluri, M., 
      et al. 2016, MNRAS, 455, 1079, 
      doi: 10.1093/mnras/stvv2383

[5]  Ivezi ́c, ˇZ., Kahn, S. M., Tyson, J. A., et al. 2019, ApJ, 
      873, 111, doi: 10.3847/1538-4357/ab042c

[6]  Akeson, R., Armus, L., Bachelet, E., et al. 2019, 
      The Wide Field Infrared Survey Telescope: 100 
      Hubbles for the 2020s. https://arxiv.org/abs/
      1902.05569.org
























