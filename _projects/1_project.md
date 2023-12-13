---
layout: page
title: Stellar Shell Formation
description: An investigation of how stellar shell formation is impacted by the presence of an oscillating central potential.
img: assets/img/prof.gif
importance: 1
category: undergraduate
permalink: /shells/
related_publications:
bibliography: shells.bib
toc:
    - name: Detailed Overview
        - name: Oscillating Central Potentials
        - name: Stellar Shells
        - name: Putting it all together
    - name: Brief Overview
        - name: Introduction
        - name: Methods
        - name: Results
        - name: Conclusions

---

---
## **Detailed Overview**

With Dr. Tomer Yavetz at the Institute for Advanced Study, I investigate the influence of an oscillating central potential in the host galaxy on the formation of stellar shells. That's a lot of jargon, so I will break down each part in the following sections.
<br>
<br>

### Oscillating Central Potentials
Let's start with a the following simplified model of a galaxy.
<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic1.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

The circle in the middle with the squiggly line represents the visible matter of the galaxy. This is what you think of when you think of galaxies: spiral arms, a bar, stars, gas, etc. The dotted line surrounding the visible matter represents the [dark matter halo](https://en.wikipedia.org/wiki/Dark_matter_halo). Dark matter halos are known to exist from [rotation curve](https://en.wikipedia.org/wiki/Galaxy_rotation_curve) data. This diagram is not to scale, as in reality the dark matter halo is significantly larger than the visible part of the galaxy.

The conventional practice in galaxy research (disregarding unique cases such as spiral arms, bars, and subhalos) treats the potential and density of galaxies as static in time. In other words, the density of the galaxy only depends on *where* you are in the galaxy, not *when* you observe it. 

However, many theories predict that the central region of many galaxies have temporal density oscillations at small radii. For example, this effect is predicted for a dark matter halo of Fuzzy Dark Matter, an theorized ultralight form of dark matter that abides by quantum mechanics at galactic scales. We may see similar behavior with a rotating bar as well.Let's update our model, adding a red circle for the region with oscillating density. For our purposes, we are only concerned with the dark matter halo, so I have removed the visible matter from the diagram.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic2.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>


A [Navarro-Frenk-White (NFW) density profile](https://en.wikipedia.org/wiki/Navarro–Frenk–White_profile) is used for the outer region, since this density profile converges with Cold Dark Matter (the more conventionally used dark matter model) and observations at large radii. For the core density profile (the one that is fluctuating), we use a profile that is cusped (the reason why this is important is to resolve the [core cusp problem](https://en.wikipedia.org/wiki/Cuspy_halo_problem)). 

The core density is dependent on a scale radius, $$r_c(t)$$, which varies sinusoidally, introducing temporal density oscillations in the central region.

<br>
$$
\rho(r, t) =
 \left\{
\begin{array}{ll}
    \rho_{core}(r,t), & r \leq r_{osc}\\
    \rho_{NFW}(r), & r \geq r_{osc} \\
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

$$
r_c(t) = r_{c,0} sin(\frac{2 \pi t}{T_{osc}})
$$. 
<br>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/rho_profile.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>


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
<br>
<br>

### Stellar Shells
Before moving forward, let's get some intuition for stellar shell formation and morphology in a conventional, static potential. Consider the following setup: a dwarf galaxy (blue) merging with the dark matter halo of an elliptical galaxy on a radial trajectory (dashed blue).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic3.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
 We refer to the smaller galaxy in this situation as the ***progenitor*** and the larger galaxy as the ***host***. The progenitor contains stars with different energies and angular momenta, both quantities that do not change through time with a static potential. First, the energy governs what the furthest point of the orbit is (apocenter) and how long it takes a star to go from one apocenter to another, $$T_{orbit}$$. 

Having a distribution of energy means that stars in the progenitor are progressing through there orbits at different speeds and they have different peak radii. As a result, the the progenitor will begin to spread along the radial direction. This is called *radial phase mixing*. Once the mixing has gone on for long enough, some stars may even begin to lap other stars.

To understand this process a bit more, let's look at a graph of radius versus time for all of the stars in a progenitor galaxy. This following animation gives intuition for how a radius versus time plot relates to an orbit in cartesian space.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        {% include video.html path="https://www.youtube.com/embed/RsmxoaW-1ug?si=yqfCFzDFhcKl6PcU" title="Video 1" class="img-fluid rounded z-depth-1" controls=true autoplay=true width="560" height="350"%}
    </div>
</div>

Now, let's give this star some friends and remake the same animation.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        {% include video.html path="https://www.youtube.com/embed/O4corKdCKxI" title="Video 1" class="img-fluid rounded z-depth-1" controls=true autoplay=true width="560" height="315"%}
    </div>
</div>

By looking at the density of particles on any verticle strip, you can understand how the stars are distributed by radius. Looking at the vertical strip on the far right cooresponds to the radius of all particles at the current moment. Looking at the vertical strip on the far right of the following snapshot, notice that there are two overdensities, labeled **1** and **2**. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/phasemixing.png" title="Figure 2" class="img-fluid rounded z-depth-1 zoomable=true"%}
    </div>
</div>

These two overdensities correspond to the two ***shells*** that exist at this time. Now trace the overdensities backwards in time. As you can see, they form at a lower radius and move outwards. However, the moving shells, which are boxed in red, aren't formed of a single group of stars slowly moving outward, rather it is new stars progressively reaching apocenter. As a result, we see each shell fade in and fade out as all of the stars eventually pass through. We can also see the shells overlapping, which is what I referred to as the stars "lapping" each other earlier.

The stars bunch up at apocenter because this is the point where they are moving slowest, meaning that they are more likely to be there since this is a highly elliptical orbit. This is analogous to how a block oscillating on a spring moves slowest when it is at its maximum displacement. Considering the stars move slowest at apocenter in this situation, you have a better chance of finding stars at apocenter, which is why we see the bunches of stars at apocenter.
 
Now that we have looked into what the effect of a spread of energy is, let's consider angular momentum. The angular momentum of a star essentially expresses how much tangential velocity (scaled by its radius) a star has. Since there is a small spread of initial radii in the progenitor, the spread of angular momentum basically informs us how much the stars will spread in the azimuthal direction. This is called *azimuthal phase mixing*. 

Another way to visualize the distribution of energy and angular momentum by coloring each star based on its energy and angular momentum.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        {% include video.html path="https://www.youtube.com/embed/c2iGJToknXs?si=zZaGcYTjjmNU6Nuo" title="Video 1" class="img-fluid rounded z-depth-1" controls=true autoplay=true width="560" height="315"%}
    </div>
</div>

As you can see in the animation, energy varies in the radial direction and the angular momentum varies along the azimuthal direction.

Combining these these two forms of mixing produces a *shell* structure. 
<div class="row">
    <div class="col-sm mt-3 mt-md-0 text-center">
        {% include figure.html path="assets/img/shell_irl.jpg" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
Stellar shells are relatively common, present in about 20% of elliptical and lenticular galaxies. This makes them great candidates to look for observational evidence of an oscillating potential if their structure is impacted.
<br>

### Putting it all together
Now that we have set up an oscillating density profile and understand the mechanics of stellar shells, we are ready to tackle the main question: what happens to this static shell morphology when you introduce an oscillating central potential during its formation?


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/galgraphic4.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

As expected, the shell structure converges to the static case when the amplitude of the oscillations is very small, as shown in the following animation.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        {% include video.html path="https://www.youtube.com/embed/u8uTOZX388c?si=AMELbwlSpGdCexGf" title="Video 1" class="img-fluid rounded z-depth-1" controls=true autoplay=true width="560" height="315"%}
    </div>
</div>

We find that the results of such an encounter are highly sensitive to the relationship between the two periods we have discussed: the orbit radial period, $$T_{orbit}$$, and the oscillation period, $$T_{core}$$. We find that when $$T_{core} >> T_{orbit}$$ and $$T_{core} << T_{orbit}$$ the structure converges to the standard static potential morphology. When $$T_{core} ~ T_{orbit}$$, structure is either entirely destroyed or new structure may be created. These results are shown in the following video, where the top left and the bottom right cells are the cases where $$T_{core} << T_{orbit}$$ and $$T_{core} >> T_{orbit}$$ respectively.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        {% include video.html path="https://www.youtube.com/embed/KV_E998ff2k?si=3jyiSDs50IYMDNHY" title="Video 1" class="img-fluid rounded z-depth-1" controls=true autoplay=true width="560" height="315"%}
    </div>
</div>

The resulting effect when $$T_{core} ~ T_{orbit}$$ is dependent on the resonance between the two oscillations. The resonance between these two frequencies is important because the central density oscillations adds and removes energy from stars, depending on when they pass through the center. This effect can be seen by plotting the total energy for each particle as a function of time, which is constant when there is a static potential.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/osc_static_H.png" title="Figure 1" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

There are several points in the plot where the lines converge after they pass through the central region, meaning that their energies converged. At other points, their energies spread out after passing by the oscillating region. From this, we can see how energy is being added and removed from stars in the system differently, creating unique patterns of convergence and divergence.

The oscillating shell has produced several rare but observed structures, such as rings and one armed spirals. There have also been cases where some particles get bound to the center and others are ejected. The simulations have also produced compression waves of stars being ejected from the central region. 
<br>
<br>

---

## **Brief Overview**
<br>

### Introduction
Stellar shells are concentric layers of stars encircling some galaxies. These shells are formed when a smaller progenitor galaxy merges with a larger host galaxy, a scenario most frequently observed in nature when the progenitor follows a highly eccentric orbit around the host galaxy <d-cite key=Hendel_2015></d-cite>.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/shell_irl.jpg" title="Figure 1" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<div class="caption">
    **Figure 1.** Hubble image of the galaxy ESO 381-12, containing several stellar shells. Credit: NASA, ESA, P. Goudfrooij (STScI)
</div>

With Dr. Tomer Yavetz at the Institute for Advanced Study, I investigate the influence of an oscillating central potential in the host galaxy on the formation of stellar shells. The physical motivation for this investigation lies in the predicted behavior of galaxies with Fuzzy Dark Matter (FDM) halos. 

FDM is a proposed form of dark matter that is composed of ultralight scalar axions, with a de Broglie wavelength on the scale of approximately a kpc. Central oscillations in the seen in FDM simulations due to wave-like interference patterns <d-cite key=Schive_2014></d-cite>.
<br>
<br>

### Methods
The host galaxy's potential was generated by creating a spherically symmetric density profile with a sinusoidally oscillating core and an NFW envelope <d-cite key=Yavetz_2022></d-cite> and solving the Poisson Equation, simplified for spherical symmetry.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/tables.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<div class="caption">
    **Figure 2.** Dynamic relationship between density, potential, and acceleration with respect to both time and radius. Each vertical strip represents a snapshot of these parameters at a specific time, while horizontal strips reveal how these properties change over time at a radius.
</div>

We conducted a test particle simulation using leapfrog integration, interpolating acceleration from the above table. The progenitor, with a mass $$m_{prog} = 1.1 \times 10^4 M_{\odot}$$, was populated with test particles normally distributed around its center. The host galaxy has a mass of $$m_{host} = 1.1 \times 10^8 M_{\odot}$$ <d-cite key=2016MNRAS.455.1079P></d-cite>.
<br>
<br>

### Results
<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/T_convg.png" title="Figure 2" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<div class="caption">
    **Figure 3.** The top and bottom figures depict the 2D spatial distribution of test particle shells with differing central potential oscillation periods at 𝑡 = 15.24 $T_{orbit}$. Oscillation periods and the simulation time are represented in terms of the radial period of the progenitor base orbit, $T_{orbit}$ = 2.5 𝐺𝑦𝑟. The periods vary from significantly shorter periods than the time required to traverse the central region to substantially longer periods.
</div>

* As expected, the effect of the central potential oscillation is negligible in cases where the oscillation period is much greater or much less than the time for the progenitor to cross the central region (top left and bottom right cells of Figure 3). The shells formed in this regime are nearly identical to the typical shells formed in a static potential.

* Amplitude convergence tests show that the shells in the oscillating potential expand and contract around the static case (QR Code 2).
* Figure 3 shows that the oscillating central potential translates to varying the energy in the system, impacting the typical shell structure. In certain cases, this process leads to the formation of additional structure (new over densities, such as in the $$T / T_{orbit}$$ = 0.04 case) or a total destruction of structure (such as in the $$T / T_{orbit}$$ = 0.28 case).
<br>
<br>

### Conclusions
* One likely explanation for the changes to the typical shell structure is a resonance between the potential oscillation periods and the time to traverse the central region.
* An immediate next step is to use a realistic FDM potential produced from a full scale FDM simulation to see if the disruption is replicated.
* Stellar shell formation in an oscillating potential may also have implications outside of FDM, such as with other physical situations like a rotating bar.
* One future avenue is to identify observable signatures of an oscillating central region.
* An observable signature of this phenomenon could provide compelling evidence for FDM as a primary DM candidate.
* The next generation of telescopes, such as the Vera C. Rubin Observatory/LSST <d-cite key=2019ApJ...873..111I></d-cite> and the Nancy Grace Roman Space Telescope <d-cite key=2019arXiv190205569A></d-cite>, may allow us to probe shells around not only large galaxies, but also dwarf galaxies.
<br>
<br>






















