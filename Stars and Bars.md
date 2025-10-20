#UIUC #Combinatorics

Counts the number of ways to distribute identical objects (stars) into distinct bins (bars).

---

## Formulas

- **Nonnegative solutions** to $x_1 + x_2 + \dots + x_k = n$:  
    $\text{ways} = \binom{n + k - 1}{k - 1}$
    
- **Positive solutions** (each bin ≥1):  
    $\text{ways} = \binom{n - 1}{k - 1}$
    

---

## Example

5 candies, 3 kids:

- Zeros allowed: $\binom{7}{2} = 21$
    
- At least one each: $\binom{4}{2} = 6$
    

```
**|*|*
*|**|*
***||*
```

Each line = one placement of bars among stars.

It is easy to see how we can biject the amount of stars and bars to the permutations of the set $S$
