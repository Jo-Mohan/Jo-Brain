#UIUC #Combinatorics

Insertion Algorithms are an efficient way of generating all possible combinations of a finite set. 

We want a listing of all permutations of $[n]={1,\dots,n}$ such that each step swaps two **adjacent** elements.

The following algorithm can accomplish that goal:

1. Base: output $[1]$.
    
2. For $k = 2.. n$:
    
    - If k is **even**: scan the previous list **top → bottom**. In each permutation, move `k` **left to right** (by adjacent swaps) across the word, outputting each new position.
        
    - If k is **odd**: scan the previous list **bottom → top**. In each permutation, move `k` **right to left** (by adjacent swaps), outputting each new position.
        
3. The concatenation is a list of all (n!) permutations where **successive permutations differ by one adjacent transposition**.

## Example

```
1
12  21
213 231  321  312  132  123   (each step swaps adjacent entries)
```


### Connections

- **Hasse diagram (weak order on S_n):** vertices = permutations; cover edges = swapping an **inversion** (adjacent increasing pair). The SJT listing traces a **Hamiltonian path** using only cover edges.
    
- **Inversions:** the sequence changes inversion count by (\pm1) each step.
    
- **Cyclic Gray code:** variants of SJT are cyclic (first and last differ by an adjacent swap).
    

---

Say instead we wanted an algorithm that inserts a new element in every possible spot to create the new permutations.


We want all $2^n$ subsets of $[n]$ so that consecutive sets differ by adding/removing **one element**.



- Let $G_1 = [0,1]$ (bit strings of length 1).
    
- For $k = 1..n-1$:
    
    - Form $G_{k+1} = 0\cdot G_k \Vert 1\cdot \text{reverse}(G_k)$.
        
- Interpreting `1` in position i as “include element i” gives a Gray-code order of subsets.
    

```
000 → 001 → 011 → 010 → 110 → 111 → 101 → 100
```

Consecutive strings differ in exactly **one bit** ⇒ consecutive subsets differ by adding/removing one element. 

---

## Some Pseudocode

#### SJT (permutations by adjacent swaps)

```text
SJT(n):
  L ← [[1]]
  for k = 2..n:
    L' ← []
    if k even:
      for π in L (top→bottom):
        insert k sweeping left→right across π, appending each new word to L'
    else:
      for π in L (bottom→top):
        insert k sweeping right→left across π, appending each new word to L'
    L ← L'
  output L
```

#### Reflected Gray (subsets)

```text
G ← ["0", "1"]
for k = 2..n:
  G ← ["0"+x for x in G] + ["1"+x for x in reverse(G)]
output G
```
