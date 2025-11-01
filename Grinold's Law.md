#Quant 

Grinold's Law is an aspect of [[Quantitative Finance |quant finance]] that aims to create a relation between performance, breath and skill. Formally:

$$IR = IC \cdot \sqrt{n}$$ $IR :=$ $\frac{\text{expected active return}}{\text{active risk}}$ 
$IC :=$  [[Information Coefficient |information coefficient]] between forecasts and real returns
$N :=$ the number of independent bets made


An obvious caveat is that $N$ is the number of $\bf{\text{independent bets}}$, something we often don't see in the market. To combat this, we can use $N_{eff}$ which can be obtain as follows:

$$N_{eff} = \frac{N}{1 + 2 \sum_{k>0}\rho_k}$$ where $\rho$ is the [[Autocorrelation |autocorrelation]] between the signals

If we have no [[Benchmarking |benchmark]], then the $IR \approx \text{Sharpe Ratio}$ 