#Quant 

When observing an [[Order Book|order book]], there are many micro signals that can be quantified and turned into metrics for larger trading strategies. Outlined below are some of the most basic but useful signals to look for.

----
## Book Pressure

This is simply how skewed the true price of a security is based on the volume and price difference on the buy and sell side. Formally:

$$ \text{Book Pressure} = \frac{\sum_{i \in I}{v_i \cdot p_i}}{\sum_{i \in I}{v_i}} $$
where $v_i$ is the volume of the security traded and $p_i$ is the price of the security. 

----
## Trade Impulse

