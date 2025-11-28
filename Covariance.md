#Quant #Statistics
### Definition

Covariance is the measure of the joint variable between two random variables. $Cov(X,Y) \in [-1,1]$ with the magnitude indicated how correlated the signals are. (1 for perfectly in sync while -1 means perfectly opposite). Covariance has units and it affected if they change. To solve this we can also look at the [[Correlation Coefficent|correlation coefficient]], which normalizes the covariance by dividing it by the geometric mean of the total variances between the two distributions.

Statistically:

$$Cov(X,Y) = \mathbb{E}[XY] - \mathbb{E}[X] \cdot \mathbb[Y]$$
If $X$ and $Y$ are independent, then the covariance is 0 but the opposite does not always hold true.

---
### Intuition

Imagine generating two random variables $X_1$ and $X_2$ through flipping ten fair coins . If, for each of the variables, we flip the coins independently, then $Cov(X_1, X_2) = 0$. But now lets say we flip one coin for $X_1$ and leave it for $X_2$, now the $Cov(X_1,X_2) = \frac{1}{10}$. We can keep expanding this until we flip the ten coins for $X_1$ and leave them the same for $X_2$ making their covariance $1$.


---
### Application

We can apply this idea to [[Quantitative Finance|quant finance]] through viewing each of the coins as common risk factor exposures for an asset class. Individual stocks have a correlation to the overall market $\in [0.5,0.8]$ but the issue is, you aren't able to see the individual coins, only their sum. It is the job of the strategy to break up the large signal into smaller pieces and predict how much strength is coming from each factor.