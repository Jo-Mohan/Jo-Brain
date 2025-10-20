#UIUC #Combinatorics

A Hasse diagram shows elements of a poset as nodes and draws an edge (x \to y) only if:

- $x < y$ in the relation, and
    
- there is **no** $z$ with $x < z < y$ (a _cover relation_).
    

Edges point upward but are usually drawn without arrows.

---

## Example

Divisibility on ${1,2,3,6}$:

```
   6
  / \
 2   3
  \ /
   1
```

Here 1 divides 2 and 3; both divide 6.

---

## Use Cases:

- Removes reflexive and transitive edges.
    
- Layers show order ranks (minimal → maximal).
    
- Useful for visualizing **chains**, **antichains**, and **lattices**.
    

---

 Related to [[Linear Extensions]] and[[Gray Codes]]