#Algorithms 

Perlin noise is a type of [[Gradient Noise |gradient noise]]. The idea with Perlin Noise is that there is a permutation table for pseudo-random gradients and a specific fade function: 

$$f(t) = 6t^2 - 15t^4 + 10t^3$$
There is also a lattice lookup table for N-dimensional noise. In more layman terms, Perlin Noise is just a very efficient and hashed version of gradient noise used in [[Procedural Generation |procedural generation]]. 