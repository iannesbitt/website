---
title: Thwaites SPH
banner: assets/banners/thwaites_sph.png
date: 2021-10-08
tags: post
template: posts.html
---
<br>

<iframe width="560" height="315" src="https://www.youtube.com/embed/1pQJw1G1IuQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This is an unpublished model I made for the final project of a fluid dynamics class during the second year of my Master's degree. While I have not had the chance to turn it into something more substantive, I am very proud of it and think it's really interesting, and I still occasionally say to myself "oh yeah, I should get around to publishing that at some point."

The goal of the project was to understand the dynamic physical forces that act on Thwaites Glacier, West Antarctica, and contribute to the behavior of the floating and grounded portions of the ice sheet. Thwaites sits at the margin of one of the largest and most vulnerable major ice sheets in the world, the West Antarctic Ice Sheet (WAIS), much of which drains via Thwaites. Thwaites itself is understood to be a major keyhole to the WAIS; i.e. a collapse of Thwaites glacier could lead to a subsequent collapse of the entire WAIS, an ice body that contains approximately 3.3 meters' worth of global sea level. The significance of the forces captured in this model are immense and are not yet well understood. 

In simple terms, the melting of icebergs and floating ice at the ends of glaciers—and West Antarctic glaciers in particular—is not well understood and must be studied more in order for glaciologists to determine the extent to which glaciers are likely to retreat. This is especially true for glaciers that are suspected to contribute to sea level rise as climate change continues to impact the people and infrastructure that occupy our coastlines.

The model features 5 moving "paddles" which simulate the movement of katabatic winds that flow from the center of Antarctica to its edges. These very cold, dense winds have the effect of mixing the water offshore of the floating ice shelves and glacier termini. The end state of the model shows that mixing in effect with light blue, low salinity meltwater occupying the surface ocean and the darker shaded water molecules beneath it. Mixing is not the only force acting on the sea water however, as several other water masses of varying temperature and salinity are constantly in motion around the continent. A secondary effect of the mixing caused by the katabatic winds is that it may allow warm, salty Antarctic deep water to slowly make its way to the glacier terminus. This would be an important effect to study for any mass balance study of Thwaites or other vulnerable Antarctic glaciers.

The model was built with [DualSPHysics](https://github.com/DualSPHysics/DualSPHysics), a free and (mostly) open-source software that models free-surface flow phenomena and calculate forces acting on a per-particle basis, where Eulerian and continuum models struggle. Smoothed-partical hydrodynamic (SPH) numerical models are constructed of particles, rather than meshes, which allows for computation of fluid interaction without the need to recompute mesh extent at each time step. Each particle has a bell curve-like "smoothing kernel" which defines the strength of its interaction with neighboring particles. Because so many interactions can happen over the course of a model run, DualSPHysics uses the graphics processing software [CUDA](https://developer.nvidia.com/cuda-zone) to interface with graphics processing unit (GPU) computing power. Since GPUs contain many smaller cores whereas central processing units (CPUs) contain a few more powerful ones, GPUs can calculate interactions between many particles much more efficiently.

The code to run this model can be found [here](https://github.com/iannesbitt/CaseThwaitesSPH).
