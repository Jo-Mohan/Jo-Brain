#Algorithms

We understand that Perlin Noise give a smooth single scale pattern but often in real life (i.e. mountains, clouds, sand, ocean) there are structures at multiple scales.

Fractal noise aims to create several layers of Perlin noise, each smaller and faster, and blend them together. This creates a self similar looks hence the name "fractal".

The formula is as follows:

$$f(x,y) = \sum_{i=1}^{N - 1}{a_i \cdot noise(x \cdot f_i, y \cdot f_i)}$$
where:
- N $:=$ number of octaves (layers $\approx$ 5-8)
- $f_i$ $:=$ frequency of the $i$-th octave
- $a_i :=$ amplitude (weight)
- noise $:=$ Perlin or Simplex noise

A common choice is $f_i = 2^i$ and $a_i = p^i$ and $p \approx 0.5$ so that the pattern gets denser and finer while each smaller layer contributes less.

For example, octave one could be the hill, two is mid sized bumps, all the way up to five which is the micro texture.
