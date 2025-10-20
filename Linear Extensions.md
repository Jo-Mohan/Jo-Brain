#UIUC #Combinatorics


A **linear extension** of a poset is a total order that respects its partial order.


For a poset $(P, \le)$, a **linear extension** is a sequence $x_1, x_2, \dots, x_n$ of all elements in $P$ such that:  
$$
x_i \le x_j \text{ in } P \Rightarrow i < j.  
$$

---


For the divisibility poset on {1,2,3,6}:

- Valid linear extensions: $[1,2,3,6], [1,3,2,6]$.
    

Each respects the order $1 < 2, 3 < 6$.

---

## Key Ideas

- Extends a partial order to a full order (no incomparables left).
    
- Equivalent to a **topological sort** of the Hasse diagram.
    
- Number of linear extensions measures how flexible a poset is.
