# Probability Inequality

[TOC]

## Markov's Inequality

> *Th.* **Markov's Inequality**
>
> Let $x\geq 0$ be random variable, $E[x] < \infty$, we have:
> $$
> P(x \geq \epsilon) \leq \frac{E[x]}{\epsilon},\ (\forall \epsilon > 0)
> $$
> **Generalized Markov's Inequality**
>
> Let $x\geq 0$ be random variable, $E[g(x)] < \infty$, $g(x)$ monotonic increasing and $g(x) > 0$ on $(0, +\infty)$. We have:
> $$
> \forall \epsilon > 0,\ P(x\geq \epsilon) \leq \frac{E[g(x)]}{g(\epsilon)}
> $$

**Proof**:
$$
\begin{split}
E[g(x)] &= \int_{0}^{\infty}g(x)p(x)dx \\
&\geq \int_{\epsilon}^{\infty}g(x)p(x)dx \\
&\geq \int_{\epsilon}^{\infty}g(\epsilon)p(x)dx \\
&= g(\epsilon)p(x\geq \epsilon)
\end{split}
$$

Also $g(x) >0$, so 
$$
p(x \geq \epsilon) \leq \frac{E[g(x)]}{g(\epsilon)}
$$


## Chebyshev's Inequality

> *Th.* **Chebyshev's Inequality**
>
> Let $x$ be random variable, $E[x] = \mu <\infty$ and $\text{var}[x] = \sigma^2 \leq\infty$, we have
> $$
> P(|x-\mu| \geq \epsilon) \leq \frac{\sigma^2}{\epsilon^2}
> $$

**Proof**:

From *Markov's Inequality*, let $x \leftarrow |x-\mu|$ and $g(x) = x^2$, we have:
$$
p(|x-\mu| \geq \epsilon) \leq \frac{E[(x-\mu)^2]}{\epsilon^2} = \frac{\sigma^2}{\epsilon^2}
$$

## Jensen Inequality

> *Th*. **Jenson Inequality**
>
> Let $x$ be random variable and $f(x)$ a convex function, we have:
> $$
> E[f(x)] \geq f(E[x])
> $$



## Hoeffding Inequality

> *Th.* **Hoeffding Inequality**
>
> Let $D = \{x_1, \dots, x_m\}$ be $m$ indenpent random variable and $x_i \in [0,1]$. $\bar{x} = \sum_{i=1}^{m}x_i/m$, $\mu_i = E[x_i]$, $\bar{\mu} = \sum_{i=1}^m\mu_i$ we have:
> $$
> \begin{split}
> P\left( \bar{x} - \bar{\mu} \geq \epsilon \right) &\leq \exp(-2m\epsilon^2) \\
> P\left( |\bar{x} - \bar{\mu}| \geq \epsilon \right) &\leq 2\exp(-2m\epsilon^2)
> \end{split}
> $$

