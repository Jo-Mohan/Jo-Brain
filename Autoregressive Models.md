#Quant 

Autoregressive Models are a special type of statistical model used to predict future behavior based of past values by extrapolating a value through regression on its own past values. Numerically:

$$x_t = \phi_{t -1} + \epsilon_t $$
$x_t :=$ value at time $t$
$\phi :=$ autocorrelation factor $\in [-1,1]$
$\epsilon :=$ random shock (markets always have some random noise)

Together, these factors create an $AR(1)$ process, with the value $1$ just meaning the model predicts based on only the last timestamp and some random noise.

Generally, an $AR(p)$ process can be defined as:

$$X_t = \sum_{i = 1}^{p}\rho_i X_{t-i } + \epsilon_t $$
where $\rho$ is the parameters of the model.

For [[Quantitative Finance|quant finance]], we can use this concept to model how different stocks move as a function of time and their own previous price points.

"Yesterday and today are similar, just with some random noise."



