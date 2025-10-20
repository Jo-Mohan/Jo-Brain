Gradient noise is a type of noise commonly used as an algorithmic way to create randomness. The method consists of creating a lattice of pseudorandom gradients which the dot products of are the interpolated to obtain values in between the lattices.

We can think of gradient noise as something that creates a smooth random field of values from $[-1,1]$ that looks almost "organic". Start with a grid, typically in 2D or 3D, where each point has a random gradient vector. Take an input point $(x,y)$ and find where in the lattice it falls into. (i.e. in a unit grid the point $x=0.3$ and $y=0.7$ would fall in between $(0,0),(1,0),(0,1),(1,1)$). From there, compute the vector from each corner to the input point and take the dot product between this vector and the corner gradient vector. This gives 4 scalars which represent how "aligned" the point is with each gradient.

To smooth these points out, apply some sort of fade function and use bilinear interpolation across the cells using the smooth weights. Repeat at multiple scales to creates "octaves" of increasing frequency and decreasing amplitude to create fractal noise.


Some more common implementations are [[Perlin Noise]] and [[Fractal Noise]]