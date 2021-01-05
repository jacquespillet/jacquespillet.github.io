### Toy Engine

In order to gain some expertise on real time rendering techniques and algorithms, as a hobby project I developped this thing.
Not sure how to call it as it's has no true purpose.
I guess playground is the word.

The interface is built with Qt, and the rendering part is done with openGL.

I kind of stopped its development these days because of time constraints.

I'm considering adding support for a vulkan back end when I have some time.

In terms of actual algorithms and techniques, I also have tons of ideas of stuff I want to add.

I also started developping an offline path tracer as part of the software.

The source code is in that repo :
https://github.com/jacquespillet/KikooRenderer


Here are some of the features illustrated with screen grabs.

## Overall Interface

![Interface](Images/Kikoo/Interface.png)

Shot of the interface of the software. The structure of the software is very much influenced by Unity's. 
It is all based on an "Entity Component System" pattern.


Left panel is a scene graph visualisation
Right panel shows the selected object parameters and components.
Bottom panel is a debugging console

## Bloom post process

![Bloom Post process](Images/Kikoo/Bloom.png)

Quite a simple implementation, lots of room for improvement.

## Depth of field post process

![Dof0](Images/Kikoo/Dof3.png)

Example of a depth of field with a rather large focus distance.

## Fast approximate Anti aliasing Post process

![DUDV](Images/Kikoo/NoFxaa.png)
![DUDV](Images/Kikoo/Fxaa.png)

[Clever algorithm](https://en.wikipedia.org/wiki/Fast_approximate_anti-aliasing) that applies some image processing techniques to reduce jaggered edges due to aliasing.

## Cubemap reflections

![Cubemap](Images/Kikoo/Cubemap.png)

## Directional Flow

![DirFlow_0](Images/Kikoo/DirFlow_0.png)

Implementation of the great tutorial by [Catlike Coding](https://catlikecoding.com/unity/tutorials/flow/directional-flow/).

## Water Plane

![DUDV](Images/Kikoo/DUDV_0.png)
![DUDV](Images/Kikoo/DUDV.png)

The normals and texture coordinates of a plane are displaced using a "dudv" map.
The objects of the scene are reflected onto that plane using the displaced normals.
It also uses the fresnel equations to make the water more reflective based on the camera direction.

## Shadow mapping

The 3 most common types of light are supported :
    * Directional
    * Point
    * Spot
    
![LowResShadowmap](Images/Kikoo/LowResShadowmap.png)
* Example of a low resolution shadow map *

![Shadows](Images/Kikoo/Shadows.png)
* Higher resolution shadow map *

Soft shadows are achieved using either PCF or poisson disk sampling.


## Materials

Several type of materials are built in :
    * Unlit
    * Blinn-phong shading
    * Physically based shading

Lots of room for improvement in that area.


![Materials](Images/Kikoo/Materials.png)
* A few different material parameters *

## Normal maps

Basic implementation of normal mapping

![NormalMapping](Images/Kikoo/NormalMapping.png)
* Simple plane with displaced normals *

## Bump mapping

Basic implementation of bump mapping

![WithHeightMap](Images/Kikoo/WithHeightMap.png)  ![WithoutHeightMap](Images/Kikoo/WithoutHeightMap.png)
* On the left is with bump mapping, on the right is without bump mapping *

## Particle system

Simple particle system that uses texture atlases and billboards.

![Particles_1](Images/Kikoo/Particles_1.png)  ![Particles_2](Images/Kikoo/Particles_2.png)
* Same Particle system with two differents particle sizes*

## Volumetric ray marching

Tried to implement some ray marching for volumetric to render clouds.
Not 100% satisfied with the result.
It uses a 3d perlin worley noise.

![1](Images/Clouds/1.png)  ![2](Images/Clouds/2.png)  ![3](Images/Clouds/3.png)  
![4](Images/Clouds/4.png)  ![4](Images/Clouds/4.png)  ![6](Images/Clouds/6.png)
![7](Images/Clouds/7.png)  ![8](Images/Clouds/8.png)  ![9](Images/Clouds/9.png)



