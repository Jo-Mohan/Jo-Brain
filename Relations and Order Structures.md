#UIUC #Combinatorics 


A **binary relation** on a set $A$ is any subset of $(A \times A)$.  
Relations form the foundation for many combinatorial and structural ideas — including **equivalence classes**, **partial orders**, **Hasse diagrams**, and **lattices**.

---

Each property describes a logical condition on pairs (or triples) of elements.

  - Reflexive: $(x, x) ∈ R$ for all $x$
  - Irreflexive: $(x, x) ∉ R$ for all $x$
  - Symmetric: $(x, y) ⇒ (y, x)$
  - Antisymmetric: $(x, y) and (y, x) ⇒ x = y$
  - Asymmetric: $(x, y) ⇒$ $\neg (y, x)$
  - Transitive: $(x, y)$ and $(y, z) ⇒ (x, z)$
  - Connected (Total): For all distinct $x, y: (x, y)$ or $(y, x)$ holds.

---

##  Classification of Relations

| Type                  | Required Properties                             | Meaning                                                           | Examples                                  |
| --------------------- | ----------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------- |
| Equivalence Relations | Reflexive, Symmetric, Transitive                | Groups elements into [[Equivalence Classes\|equivalence classes]] | “≡ mod n”, “same remainder”, “same color” |
| Partial Orders        | Reflexive, Antisymmetric, Transitive            | Defines hierarchy; not all pairs comparable                       | “divides”, “⊆”                            |
| Total Orders          | Reflexive, Antisymmetric, Transitive, Connected | Every pair comparable                                             | “≤”, alphabetical order                   |
| Strict Partial Orders | Irreflexive, Transitive                         | Like a partial order but strict (“<”)                             | “<”, “⊂”                                  |
| Strict Total Orders   | Irreflexive, Transitive, Connected              | Strict linear hierarchy                                           | “<” on numbers                            |
| Preorders             | Reflexive, Transitive                           | Order-like but may have equivalences                              | “≤” on equivalent fractions               |

---

## Visual Tools

- [[Hasse Diagrams]]
- [[Chains and Antichains]]
- [[Lattices]]

---


