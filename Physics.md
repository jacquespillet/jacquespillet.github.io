###Physics simulation

Here I showcase some physics simulation I've been playing with in the past years.

##Smoothed particle hydrodynamics

Implementation of SPH, all on the GPU with compute shaders in Unity.

Next step will be to render it properly, I'm thinking implementing [this paper](https://www.cc.gatech.edu/~turk/my_papers/sph_surfaces.pdf)

<img src="Images/Gifs/SPH_0.gif"/>
<img src="Images/Gifs/SPH_1.gif"/>
<img src="Images/Gifs/SPH_2.gif"/>

##Bullets

I've integrated [Bullet physics engine](https://github.com/bulletphysics/bullet3) in my [toy engine](Engine.md).

Here are a few features that I implemented :

<img src="Images/Gifs/Bullets_Cubes.gif"/>

<img src="Images/Gifs/stairs.gif"/>

<img src="Images/Gifs/soft.gif"/>


###Others

I've started to implement [position based dynamics](https://matthias-research.github.io/pages/publications/posBasedDyn.pdf) in Unity on the GPU.

<img src="Images/Gifs/PBD_0.gif"/>
<img src="Images/Gifs/PBD_1.gif"/>


I've also played a bit with implementing rigid body dynamics on the GPU  using [this paper](https://developer.nvidia.com/gpugems/gpugems3/part-v-physics-simulation/chapter-29-real-time-rigid-body-simulation-gpus)

<img src="Images/Gifs/Harada.gif"/>
