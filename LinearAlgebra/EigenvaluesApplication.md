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





## Power Iteration

A numerical method to calculate the dominant eigenvalues and eigenvectors approximately.

More can be found in [ref1](http://staff.ustc.edu.cn/~rui/ppt/num/num-eigen-power.html) and [ref2](http://mlwiki.org/index.php/Power_Iteration)

**Condition**: The matrix $A \in R^{n\times n}$ has $n$ linearly independent eigenvector, i.e. the matrix has complete eigenvectors or this matrix is not defective.



**Method**: Start from a non-zero vector $\mathbf{x}^{(0)}$, iteratively calculate $\mathbf{x}^{(t+1)} = A\mathbf{x}^{(t)}$.



**Analysis**:

Suppose the eigenvectors of $A$ are $\mathbf{v}_1, \dots \mathbf{v}_n$ which are linearly independent. We can write $\mathbf{x}^{(0)}$ as 
$$
\mathbf{x}^{(0)} = \sum_{i=1}^{n}a_i\mathbf{v}_i
$$
Thus
$$
\mathbf{x}^{(k)} = A^k\sum_{i=1}^{n}a_i\mathbf{v}_i = \sum_{i=1}^{n}a_iA^k\mathbf{v}_i
$$
and $A^k \mathbf{v}_i = \lambda_i^k \mathbf{v}_i$. Therefore
$$
\mathbf{x}^{(k)} = \sum_{i=1}^{n}a_i\lambda_i^k\mathbf{v}_i
$$
suppose $|\lambda_1| \geq |\lambda_2| \geq \dots \geq |\lambda_n|$, we have
$$
\mathbf{x}^{(k)} = \lambda_1^k\sum_{i=1}^{n}a_i(\dfrac{\lambda_i}{\lambda_1})^k\mathbf{v}_i
$$

1. **Converge situation**: If $|\lambda_1| > |\lambda_2| \geq \dots \geq |\lambda_n|$,  $\lim_{k\rightarrow \infin} (\dfrac{\lambda_i}{\lambda_1})^k = 0,~i\neq  1$. Thus if $k$ large enough, we have
   $$
   \mathbf{x}^{(k)} \approx \lambda_1^k \alpha_1 \mathbf{v}_1
   $$
   i.e. $\mathbf{x}^{(k)}$ is parallel to $\mathbf{v}_1$ and we also have:
   $$
   \mathbf{x}^{(k+1)} = A\mathbf{x}^{(k)} \approx \lambda_1^k \alpha_1 \mathbf{v}_1 = \lambda_1 (\lambda_1^k \alpha_1 \mathbf{v}_1) \approx \lambda_1 \mathbf{x}^{(k)}
   $$
   thus
   $$
   \lambda_1 \approx \dfrac{\mathbf{x}_{i}^{(k+1)}}{\mathbf{x}_{i}^{(k)}},~ i = 1,2,\dots n
   $$

2. **Jump situation**: If $|\lambda_1| = |\lambda_2| > \dots \geq |\lambda_n|$ and $\lambda_1 = -\lambda_2$
   $$
   \begin{split}
   \mathbf{x}^{(k)} &= \lambda_1^k \left( \alpha_1 \mathbf{v}_1 + (-1)^k\alpha_2 \mathbf{v}_2 + \dots + \left(\dfrac{\lambda_n}{\lambda_1}\right)^k\alpha_n \mathbf{v}_n \right) \\
   &\approx \lambda_1^k ( \alpha_1 \mathbf{v}_1 + (-1)^k\alpha_2 \mathbf{v}_2 )
   \end{split}
   $$
   Thus
   $$
   \begin{split}
   \mathbf{x}^{(k+1)} &\approx \lambda_1^{k+1}(\alpha_1 \mathbf{v}_1 + (-1)^{k+1}\alpha_2\mathbf{v}_2) \\
   \mathbf{x}^{(k+2)} &\approx \lambda_1^{k+2}(\alpha_1 \mathbf{v}_1 + (-1)^{k+2}\alpha_2\mathbf{v}_2) \\
   & \approx \lambda_1^2 \mathbf{x}^{(k)}
   \end{split}
   $$
   Thus
   $$
   \lambda_1 = \sqrt{\dfrac{\mathbf{x}^{(k+2)}_{i}}{\mathbf{x}^{(k)}_{i}}},~i=1,2,\dots,n
   $$
   And
   $$
   \begin{equation}
   \begin{split}
   2\lambda_1^{k+2}\alpha_1\mathbf{v}_1 &= \mathbf{x}^{(k+2)} + \lambda_1 \mathbf{x}^{(k+1)} \\ 
   2(-1)^k \lambda_1^{k+2}\alpha_2\mathbf{v}_2 &= \mathbf{x}^{(k+2)} - \lambda_1 \mathbf{x}^{(k+1)} \\ 
   \end{split}
   \end{equation}
   $$

3. **Other situation**: Too complex to concern



**Normalization**: The values produced by the power method are quite large

- better if we scale them down
- should scale the values at each iteration
- for example, can find the largest component of $\mathbf{x}^{(k)}$ and divide by it (i.e. divided by the infinite norm $\|\mathbf{x}\|_{\infin} = \max_i |\mathbf{x}_i|$)
- more commonly, we just unit-normalize it `v_new = v_old / np.linalg.norm(v_old)`

*Note*: The normalized power iteration has similar situation division as the vanilla power iteration. See [here](http://staff.ustc.edu.cn/~rui/ppt/num/num-eigen-power.html#/eigen-power-regular). 



**Shift**: Let $B = A - pI$, we have $\lambda_B = \lambda_A - p$, if we can choose proper $p$ s.t. 
$$
\left| \dfrac{\lambda_2 - p}{\lambda_1 - p} \right| < \left| \dfrac{\lambda_2}{\lambda_1} \right|
$$
Then we can improve the convergence speed.

