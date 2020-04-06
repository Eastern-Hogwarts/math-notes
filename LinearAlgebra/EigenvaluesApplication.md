# Eigenvalues and Applications #

[TOC]

## Quadratic Forms ##

### Basic ###

> *Def.* **Quadratic Form**
>
> In General, a **quadratic form** in the variables $x_{1:n}$ is an expression of the form:
> $$
> q(\mathbf{x}) = q(x_{1}, x_{2}, \dots, x_{n}) = \sum_{i=1}^{n}\sum_{j=1}^{n}b_{i,j}x_{i}x_{j}
> $$
>
> **Matrix Representation for Quadratic Form**
>
> Define $a_{i,i} = b_{i,i}$ and $a_{i,j} = (b_{i,j} + b_{ji})/2,\ i\neq j$, we have 
> $$
> q(\mathbf{x}) = \mathbf{x}^{T}A\mathbf{x}
> $$
> where $A$ is a symmetric matrix.



**Homogeneous**: All terms in this equation(or function, etc.) have the same exponential degree.



> **From Text Book**
>
> The term *form* means homogeneous polynomial; that is, $q(a\mathbf{x}) = a^{k}q(\mathbf{x})$. 



> *Th.* For $\mathbf{x}\in R^n$, let $q(\mathbf{x})$ denote the quadratic form that:
> $$
> q(\mathbf{x}) = \sum_{i=1}^{n}\sum_{j=1}^{n}b_{i,j}x_{i}x_{j}.
> $$
> Let $A=(a_{i,j})$ be the $(n\times n)$ matrix defined by
> $$
> a_{i,j} = (b_{i,j} + b_{j,i})/2
> $$
> The matrix $A$ is symmetric and $q(\mathbf{x}) = \mathbf{x}^{T}A\mathbf{x}$. Moreover, there is no other **symmetric** matrix $B$ s.t. $\mathbf{x}^{T}B\mathbf{x} = q(\mathbf{x})$. 
>
> *Note.* But there exists many **nonsymmetric** matrix $B$ s.t. $\mathbf{x}^{T} B \mathbf{x} = q(\mathbf{x})$.



### Diagonalizing Quadratic Forms ###

For many applications, it is useful top have the even simpler representation described in this subsection. Because a real symmetric matrix can be diagonalized with an orthogonal matrix. That is, there is a square matrix $Q$ s.t.

1. $Q^TQ=I$.
2. $Q^TAQ=D$, where $D$ is diagonal.
3. The diagonal entries of $D$ are the eigenvalues of $A$.

If we make the substitution $\mathbf{x} = Q\mathbf{y}$, we have:
$$
\begin{split}
q(\mathbf{x}) &= q(Q\mathbf{y}) \\
&= (Q\mathbf{y})^{T}A(Q\mathbf{y}) \\
&= \mathbf{y}^{T}Q^{T}AQ\mathbf{y} \\
&= \mathbf{y}^{T}D\mathbf{y} \\
&= \sum_{i=1}^{n}\lambda_{i}y_{i}^{2}
\end{split}
$$


### Classifying Quadratic Forms ###

We can think of a quadratic form as a function from $R^n$ to $R$. Specifically, if $q(\mathbf{x}) = \mathbf{x}^{T}A\mathbf{x}$ where $A$ is a real symmetric matrix, then we can define a real-valued function with domain $R^n$ where
$$
y = q(\mathbf{x}) = \mathbf{x}^{T}A\mathbf{x}
$$
The quadratic form is classified as:

1. **Positive Definite**: if $q(\mathbf{x}) > 0$ for all $\mathbf{x}\in R^n$, $\mathbf{x}\neq \theta$.
2. **Positive Semidefinite**: if $q(\mathbf{x}) \geq 0$ for all $\mathbf{x}\in R^n$, $\mathbf{x}\neq \theta$.
3. **Negative Definite**: if $q(\mathbf{x}) < 0$ for all $\mathbf{x}\in R^n$, $\mathbf{x}\neq \theta$.
4. **Negative Semidefinite**: if $q(\mathbf{x}) \leq 0$ for all $\mathbf{x}\in R^n$, $\mathbf{x}\neq \theta$.
5. **Indefinite**: if $q(\mathbf{x})$ assumes both positive and negative values.



> *Th.* Let $q(\mathbf{x})$ be a quadratic form with representation $q(\mathbf{x}) = \mathbf{x}^{T}A\mathbf{x}$, where $A$ is a symmetric $(n\times n)$ matrix. Let the eigenvalues of $A$ be $\lambda_{1}, \lambda_{2}, \dots, \lambda_{n}$. The quadratic form is:
>
> 1. Positive definite $\Leftrightarrow \forall i,\ \lambda_{i}>0$.
>
> 2. Positive semidefinite $\Leftrightarrow  \forall\ i,\ \lambda_{i} \geq 0$.
>
> 3. Negative definite $\Leftrightarrow  \forall\ i,\ \lambda_{i}<0$.
>
> 4. Negative semidefinite $\Leftrightarrow \forall\ i,\lambda_{i}\leq 0$.
>
> 5. Indefinite $\Leftrightarrow $ $A$ has both positive and negative eigenvalues.



