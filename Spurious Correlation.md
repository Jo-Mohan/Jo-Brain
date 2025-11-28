Spurious Correlation is the idea that two things move together briefly when they in fact have nothing to do with each other. In [[Quantitative Finance|quant fInance]], this can be dangerous as models could pick up on seemingly statistically significant trends when in reality, this was pure coincidence. 

A rather absurd example is the graph between the price of Blackrock stock and the average yearly consumption of cheese by Americans.

![[Screenshot 2025-11-22 at 6.36.24 PM.png]]

Clearly the two are unrelated, but certain models could pick up on trends between the two assets.

More practically, there is usually some sort of confounding variable between the two assets that causes the brief correlation. Techniques to combat this include running multiple regression analysis, pruning noisy data, and generating small psuedo-labels for the model