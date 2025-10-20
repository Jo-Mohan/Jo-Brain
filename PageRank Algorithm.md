#UIUC #Algorithms
The PageRank Algorithm is a way to numerically assign a weight to the hyperlinks on a page with hyperlinks. The overarching logic is that if many external pages point towards a page $P$, then $P$ must be an important page and subsequently is given a higher page rank.

Templated version:
``` python
import numpy as np

def pagerank(M, d: float = 0.85):
    """PageRank algorithm with explicit number of iterations. Returns ranking of nodes (pages) in the adjacency matrix.

    Parameters
    ----------
    M : numpy array
        adjacency matrix where M_i,j represents the link from 'j' to 'i', such that for all 'j'
        sum(i, M_i,j) = 1
    d : float, optional
        damping factor, by default 0.85

    Returns
    -------
    numpy array
        a vector of ranks such that v_i is the i-th rank from [0, 1],

    """
    N = M.shape[1]
    w = np.ones(N) / N
    M_hat = d * M
    v = M_hat @ w + (1 - d) / N
    # only update while meaningful change between norms occurs
    while np.linalg.norm(w - v) >= 1e-10:
        w = v
        v = M_hat @ w + (1 - d) / N
    return v

M = np.array([[0, 0, 0, .25],
              [0, 0, 0, .5],
              [1, 0.5, 0, .25],
              [0, 0.5, 1, 0]])
v = pagerank(M, 0.85)
```
```