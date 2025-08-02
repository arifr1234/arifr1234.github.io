# Ari Friedman
https://github.com/arifr1234  
arifr1234@gmail.com

## [My shadertoy profile](https://www.shadertoy.com/user/arifr123)

![image1](https://github.com/user-attachments/assets/c90cf09d-122d-4858-ae17-491d5ddf9c2b) ![image2](https://github.com/user-attachments/assets/e93314de-6f8c-431d-89f1-9619504a8074)  
![image3](https://github.com/user-attachments/assets/7725844f-c151-41c7-bf28-4e4bd6003dc8) ![image4](https://github.com/user-attachments/assets/359ca90b-2756-4db0-8644-8489ac464a7b)  
![image5](https://github.com/user-attachments/assets/d34eaeb7-3442-4741-83d7-a37f6c1b94f8) ![image6](https://github.com/user-attachments/assets/8c746091-65fc-4f71-b935-2ddfaa050719)  

## Websites
Old projects that are also websites.

### [wikipedia-graph](https://arifr1234.github.io/wikipedia-graph/)
Track the Wikipedia pages you visit and the network of links between them.  
![110713750-1dbb5700-820b-11eb-868c-07fb6b61b241](https://github.com/user-attachments/assets/a92153af-45f5-4063-a0cf-46f62346a777)  
For more info, see https://github.com/arifr1234/wikipedia-graph#wikipedia-graph.

### Esoteric 3d graphics
#### [implicit-equation-plotter](https://arifr1234.github.io/implicit-equation-plotter/)
This one is actually pretty cool, as at the time I created it, there wasn't any other plotter online that could view animated implicit surfaces in real-time (at least that I could find), and this probably didn't change since this is a pretty niche problem.  
By "[implicit surface](https://en.wikipedia.org/wiki/Implicit_surface)" or "implicit equation", I refer to a surface defined by an equation $R(x, y, z)=0$, when $R$ is differentiable (and hopefully nice in other aspects too).  
For instance, the unit sphere can be described as $x^2 + y^2 + z^2 - 1 = 0$.  
The user defines the surface by writing the $R(x, y, z)$ function, and the displayed surface is the set of points where it is zero.  
The function is written in the GLSL programming language with custom [dual numbers](https://en.wikipedia.org/wiki/Dual_number) types and functions to enable the automatic calculation of the Jacobian of the provided function on the GPU ([automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation)).  
Using a [cellular-automata](https://en.wikipedia.org/wiki/Cellular_automaton)-inspired algorithm, the surface can be animated in real time, just by depending on the `time` parameter in your $R$ function.  

#### [webglParametricSurfacePlotter](https://arifr1234.github.io/webglParametricSurfacePlotter/)
Same as the last one, but for parametric surfaces instead of implicit surfaces.  
It's a lot less interesting because plotters of parametric surfaces are a lot more common and a lot better (also true for animated parametric surface plotters), but still it's cool because it's [shadertoy](https://www.shadertoy.com/)-style hard mode, using mostly a fragment shader (in that sense it is novel).  

#### [clifford-torus](https://arifr1234.github.io/clifford-torus)
![image8](https://github.com/user-attachments/assets/eebd7d48-e877-4996-b126-53041a001b85)  
The name of the repo is misleading, this is another parametric surfaces ploter, but this time more traditional. The interesting thing here is that the normals of the surface are calculated in real time on the GPU.  
This by itself isn't novel because it can be done using a compute shader or a geometry shader, but WebGL does not support these kinds of shaders, so I figured out a clever trick to use another vertex shader that acts as a primitive geometry shader.  
