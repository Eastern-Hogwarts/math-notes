# Application #

[TOC]

## Data Fitting ##

### Polynomial Interpolation ###

多项式内插值

Frequently polynomial interpolation is used when values of a function $f(t)$ are given in tabular form. For example, given a table of $n+1$ values of $f(t)$, an **interpolating polynomial** for $f(t)$ is a polynomial $p(t)$ of the form:
$$
p(t) = a_{0} + a_{1}t + a_{2}t^{2} + \cdots + a_{n}t^{n} \\
\text{s.t. }\ p(t_{i}) = y_{i} = f(t_{i})\text{ for } 0\leq i\leq n
$$



> *Th.* Given $n+1$ **distinct** numbers $t_{0}, t_{1}, \dots , t_{n}$ and any set of $n+1$ values $y_{0}, y_{1}, \dots , y_{n}$, there exists unique polynomial $p(t)$ of degree $n$ or less, $p(t) = a_{0} + a_{1}t + a_{2}t^{2} + \cdots + a_{n}t^{n}$, s.t. $\forall\ i,\ p(t_{i}) = y_{i}$. 
>
> *Proof.* From Lagrange Interpolation Formula.



From $\forall\ i,\ p(t_{i}) = y_{i} = f(t_{i})$, we have:
$$
a_{0} + a_{1}t_{0} + a_{2}t_{0}^{2} + \cdots + a_{n}t_{0}^{n} = y_{0} \\
a_{0} + a_{1}t_{1} + a_{2}t_{1}^{2} + \cdots + a_{n}t_{1}^{n} = y_{1} \\
\vdots \\
a_{0} + a_{1}t_{n} + a_{2}t_{n}^{2} + \cdots + a_{n}t_{n}^{n} = y_{n} \\
$$
Or $T\mathbf{a} = \mathbf{y}$ where 
$$
T = 
\begin{bmatrix}
    1 & t_{0} & t_{0}^{2} & \dots & t_{0}^{n} \\
    1 & t_{1} & t_{1}^{2} & \dots & t_{1}^{n} \\
    \vdots & \vdots & \vdots & \ddots & \vdots \\
    1 & t_{n} & t_{n}^{2} & \dots & t_{n}^{n} \\
\end{bmatrix}
$$
$T$ is called **Vandermonde Matrix**.



> *Th.* Vandermonde Matrix is nonsingular provided that all $t_{i}$ are distinct.



### Solutions to Initial Value Problems ###

Useless



## Numerical Integration and Differentiation ##

 These are also applications of Vandermonde matrix.

### Numerical Integration ###

Suppose we have:
$$
I(f) = \int_{a}^{b}f(t)dt
$$
If the integrand is fairly complicated or if the integrand is not a standard form that can be found in a table of integrals, then it will be necessary to approximate the value numerically.
