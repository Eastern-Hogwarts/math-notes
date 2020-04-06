# The Eigenvalue Problem #

[TOC]

## The Eigenvalue Problem ##

> *Def.* **The Eigenvalue Problem**
>
> For an $(n\times n)$ matrix $A$, find all scalars $\lambda$ s.t. the equation:
> $$
> A\mathbf{x} = \lambda \mathbf{x}
> $$
> has a **nonzero** solution, $\mathbf{x}$. Such a scalar $\lambda$ is called an **eigenvalue** of $A$, and any **nonzero** $(n\times 1)$ vector $\mathbf{x}$ satisfying the equation above is called an **eigenvector** corresponding to $\lambda$.
>
> *Note.* The equation above is equivalent to
> $$
> (A-\lambda I)\mathbf{x} = \theta,\ \mathbf{x}\neq \theta.
> $$
>
> Therefore, the eigenvalue problem consists of 2 parts:
>
> 1. Find all scalars $\lambda$ such that $A-\lambda I$ is singular.
> 2. Given a scalar $\lambda$ such that $A-\lambda I$ is singular, find all nonzero vectors $\mathbf{x}$ such that $(A-\lambda I)\mathbf{x} = \theta$.



> *Th.* Let $A$ be an $(n\times n)$ matrix. Then $\text{det}(A-tI)$ is a polynomial of degree $n$ in $t$.



> *Def.* **Characteristic Polynomial**
>
> Let $A$ be an $(n\times n)$ matrix. The $n$th-degree polynomial, $p(t)$, given by
> $$
> p(t) = \text{det}(A-tI)
> $$
> is called the **characteristic polynomial** for $A$.



> *Th.* Let $A$ be an $(n\times n)$ matrix, and let $p$ be the characteristic polynomial for $A$. Then the eigenvalues of $A$ are precisely the roots of $p(t) = 0$. This equation is called the **characteristic equation**.
>
> *Note.*
>
> 1. An $(n\times n)$ matrix can have no more than $n$ distinct eigenvalues.
> 2. An $(n\times n)$ matrix always has at least one eigenvalue (possible complex).
> 3. The characteristic polynomial can be rewritten as $p(t) = a\prod_{i=1}^{n}(t-r_{i})$. The number of times the factor $(t-r)$ appears in the factorization of $p(t)$ given above is called the **algebraic multiplicity** of $r$.



### Special Results ###

> *Th.* Let $A$ be an $(n\times n)$ matrix, and let $\lambda$ be an eigenvalue of $A$. Then
>
> 1. $\lambda^k$ is an eigenvalue of $A^k$, $k=2,3,\cdots$
> 2. If $A$ is nonsingular, then $1/\lambda$ is an eigenvalue of $A^{-1}$
> 3. If $\alpha$ is any scalar, then $\lambda + \alpha$ is an eigenvalue of $A + \alpha I$.



> *Th.* Let $A$ be an $(n\times n)$ matrix. Then $A$ and $A^T$ have the same eigenvalues.



> *Th.* Let $A$ be an $(n\times n)$ matrix. Then $A$ is singular if and only if $\lambda = 0$ is an eigenvalue of $A$.
>
> *Proof.* From the definition of eigenvalue problem.



> *Th.* Let $T = (t_{i,j})$ be an $(n\times n)$ triangular matrix. Then the eigenvalues of $T$ are the diagonal entries, $t_{1,1}, t_{2,2}, \dots, t_{n,n}$.



## Eigenvectors and Eigenspaces ##

If $\lambda$ is an eigenvalue of $A$, then the eigenvectors corresponding to $\lambda$ are precisely the **nonzero** vectors in the null space of $A-\lambda I$.



> *Def.* Let $A$ be an $(n\times n)$ matrix. If $\lambda$ is an eigenvalue of $A$, then:
>
> * The null space of $A-\lambda I$ is denoted by $E_{\lambda}$ and is called the **eigenspace** of $\lambda$.
> * The dimension of $E_{\lambda}$ is called the **geometric multiplicity** of $\lambda$.
>
> *Note*: The geometric multiplicity of $\lambda$ is never larger than the algebraic multiplicity of $\lambda$.



## Defective Matrix ##

If $A$ is an $(n\times n)$ matrix and if some eigenvalue of $A$ has a geometric multiplicity that is less than its algebraic multiplicity, then $A$ will not have a set of $n$ linearly independent eigenvectors. Such a matrix is called defective.



> *Def.* Let $A$ be an $(n\times n)$ matrix. If there is an eigenvalue $\lambda$ of $A$ such that the geometric multiplicity of $\lambda$ is less than the algebraic multiplicity of $\lambda$, then $A$ is called a **defective** matrix.

 

> *Th.* Let $\mathbf{u}_{1}, \mathbf{u}_{2}, \dots, \mathbf{u}_{k}$ be eigenvectors of an $(n\times n)$ matrix $A$ corresponding to distinct eigenvalues $\lambda_{1}, \lambda_{2}, \dots, \lambda_{k}$. That is,
> $$
> A\mathbf{u}_{j} = \lambda_{j}\mathbf{u}_{j}\ \ \forall\ j=1,2,\dots,k.\ \ k\leq n \\
> \lambda_{i} \neq \lambda_{j}\ \ \forall\ i\neq j.
> $$
>
> Then $\{ \mathbf{u}_{1}, \mathbf{u}_{2}, \dots, \mathbf{u}_{k} \}$ is a linearly independent set
>
> *Corollary.* Let $A$ be an $(n\times n)$ matrix. If $A$ has $n$ distinct eigenvalues, then $A$ has a set of $n$ linearly independent eigenvectors.



## Complex Eigenvalues and Eigenvectors ##

When the characteristic equation has complex roots.



> *Def.* **The Norm of Complex Vector**
>
> The norm of a complex vector $\mathbf{x}$ (denoted by $\| \mathbf{x} \|$) is defined in terms of $\mathbf{x}$ and $\bar{\mathbf{x}}$:
> $$
> \| \mathbf{x} \| = \sqrt{\bar{\mathbf{x}}^{T}\mathbf{x}}.
> $$



> *Th.* Let $A$ be a real $(n\times n)$ matrix with an eigenvalue $\lambda$ and corresponding eigenvector $\mathbf{x}$. Then $\bar{\lambda}$ is also an eigenvalue of $A$, and $\bar{\mathbf{x}}$ is an eigenvector corresponding to it.



> *Th.* If $A$ is an $(n\times n)$ real symmetric matrix, then all the eigenvalues of $A$ are real.



## Similarity Transformations and Diagonalization ##

### Similarity ###

We are interested in identifying classes of matrices that have the same eigenvalues.

In particular, let $A$ be an $(n\times n)$ matrix, and let $S$ be a **nonsingular** $(n\times n)$ matrix and let $B=S^{-1}AS$. Let $p(t)$ be the characteristic polynomial of $B$. Then we have:
$$
\begin{split}
p(t) &= \text{det}(S^{-1}AS - tI) = \text{det}(S^{-1}AS - tS^{-1}S) \\
&=\text{det}[S^{-1}(A-tI)S] = \text{det}(S^{-1})\text{det}(A-tI)\text{det}(S) \\
&=\text{det}(S^{-1})\text{det}(S)\text{det}(A-tI) \\
&=\text{det}(A-tI)
\end{split}
$$

> *Def.* **Similarity**
>
> The $(n\times n)$ matrices $A$ and $B$ are said to be **similar** if there is a nonsingular $(n\times n)$ matrix $S$ such that $B=S^{-1}AS$.



> *Th.* If $A$ and $B$ are similar $(n\times n)$ matrices, then $A$ and $B$ have the same eigenvalues. Moreover, these eigenvalues have the same algebraic multiplicity.
>
> *Note.* Although similar matrices always have the same characteristic polynomial, it is not true that two matrices with the same characteristic polynomial are necessarily similar.
>
> *Remark.* The only matrix similar to the identity matrix is $I$ itself.
>
> *Note.* Similar matrices do not generally have the same eigenvector. If $B=S^{-1}AS$ and $B\mathbf{x}=\lambda\mathbf{x}$, then $S^{-1}AS\mathbf{x} = \lambda\mathbf{x}$ or $A(S\mathbf{x}) = \lambda(S\mathbf{x})$.



### Diagonalization ###

Computations involving an $(n\times n)$ matrix $A$ can often be simplified if we know that $A$ is similar to a diagonal matrix. Suppose $S^{-1}AS = D$, where $D$ is a diagonal matrix. we have:
$$
\begin{split}
D^{k} &= (S^{-1}AS)^k \\
&=S^{-1}ASS^{-1}AS\cdots AS \\
&=S^{-1}A^{k}S
\end{split}
$$
Then we have:
$$
A^{k} = SD^{k}S^{-1}
$$

> *Def.* **Diagonalizable Matrix**
>
> Let $A$ be an $(n\times n)$ matrix and $A$ is similar to a diagonal matrix, we say that $A$ is **diagonalizable**.



How to determine whether a matrix is diagonalizable?

> *Th.* An $(n\times n)$ matrix $A$ is diagonalizable if and only if $A$ possesses(has) a set of $n$ linearly independent eigenvectors.



If $A$ is an $(n\times n)$ diagonalizable matrix and let matrix $S=[\mathbf{S}_{1}, \mathbf{S}_{2},\cdots, \mathbf{S}_{n}]$ composed by the eigenvectors of $A$. We have:
$$
S^{-1}AS = D
$$
where
$$
D = 
\begin{bmatrix}
\lambda_{1} & ~ & ~ & ~ \\
~ & \lambda_{2} & ~ & ~ \\
~ & ~ & \ddots & ~ \\
~ & ~ & ~ & \lambda_{n} 
\end{bmatrix}
$$
is a diagonal matrix whose elements are eigenvalues of $A$ corresponding to the eigenvectors in $S$.



*Proof.*
$$
\begin{split}
AS &= [A\mathbf{S}_{1}, A\mathbf{S}_{2}, \cdots, A\mathbf{S}_{n}] \\
&= [\lambda_{1}\mathbf{S}_{1}, \lambda_{2}\mathbf{S}_{2}, \cdots, \lambda_{n}\mathbf{S}_{n}] \\
\end{split}
$$
and 
$$
\begin{split}
SD &= [S\mathbf{D}_{1}, S\mathbf{D}_{2}, \cdots, S\mathbf{D}_{n}] \\
&= [\lambda_{1}\mathbf{S}_{1} + 0\mathbf{S}_{2} + \cdots + 0\mathbf{S}_{n}, \cdots] \\
&= [\lambda_{1}\mathbf{S}_{1}, \lambda_{2}\mathbf{S}_{2}, \cdots, \lambda_{n}\mathbf{S}_{n}]
\end{split}
$$
thus
$$
AS = SD\ \text{ or }\ S^{-1}AS = D
$$

> *Corollary.* Let $A$ be an $(n\times n)$ matrix with $n$ distinct eigenvalues. Then $A$ is diagonalizable.



### Orthogonal Matrix ###

> *Th.* A real symmetric matrix is always diagonalizable.



> *Def.*  **Orthogonal Matrix**
>
> A **real** $(n\times n)$ matrix $Q$ is called an **orthogonal** matrix if $Q$ is **invertible** and $Q^{-1} = Q^{T}$. 
>
> Or
>
> A real square matrix $Q$ is **orthogonal** if and only if $Q^{T}Q = I$.
>
> Or
>
> An $(n\times n)$ matrix $Q=[\mathbf{Q}_{1}, \mathbf{Q}_{2}, \cdots, \mathbf{Q}_{n}]$ is orthogonal if and only if the columns of $Q$ from an **orthonormal (Not Orthogonal)** set of vectors.
>
> *Corollary.* If $Q$ is an $(n\times n)$ orthogonal matrix and if $P$ is formed by rearranging the columns of $Q$, then $P$ is also an orthogonal matrix.



> *Def.* If $P$ is an $(n\times n)$ matrix formed by rearranging the columns of $I_{n\times n}$, then $P$ is called a **permutation** matrix.
>
> *Note.* Permutation matrix is orthogonal matrix.



> *Th.* Let $Q$ be an $(n\times n)$ orthogonal matrix.
>
> 1. If $\mathbf{x}\in R^{n}$, then $\|Q\mathbf{x}\| = \| \mathbf{x} \|$. (because $\| Q\mathbf{x} \| = \sqrt{\mathbf{x}^{T}QTQ\mathbf{x}} = \sqrt{\mathbf{x}^{T}I\mathbf{x}}$).
> 2. If $\mathbf{x} \in R^n$ and $\mathbf{y}\in R^n$, then $(Q\mathbf{x})^{T}(Q\mathbf{y}) = \mathbf{x}^{T}\mathbf{y}$.
> 3. $\text{det}(Q) = \pm 1$.
>
> *Note.* Orthogonal matrix is a rotation linear transformation.



### Diagonalization of Symmetric Matrices ###

Every symmetric matrix can be diagonalized by an orthogonal matrix.



> *Th.* **Schur's Theorem(special case)**
>
> Let $A$ be an $(n\times n)$ matrix, where $A$ has only real eigenvalues. Then there is an $(n\times n)$ orthogonal matrix $Q$ such that:
> $$
> Q^{T}AQ = T
> $$
> where $T$ is an $(n\times n)$ **upper-triangular** matrix.
>
> Note that we can rewrite $Q^{T}AQ=T$ as $A = QTQ^T$, which is called a **Schur decomposition** or **Schur factorization** of $A$.



> *Th.* Let $A$ be a real $(n\times n)$ matrix.
>
> 1. If $A$ is symmetric, then there is an orthogonal matrix $Q$ such that $Q^TAQ=D$, where $D$ is diagonal.
> 2. If $Q^TAQ=D$, where $Q$ is orthogonal and $D$ is diagonal, then $A$ is a symmetric matrix.



> *Corollary.* Let $A$ be a real $(n\times n)$ symmetric matrix. It is possible to choose eigenvectors $\mathbf{u}_{1}, \dots, \mathbf{u}_{n}$ for $A$ such that $\{ \mathbf{u}_{1}, \mathbf{u}_{2}, \dots, \mathbf{u}_{n} \}$ is an **orthonormal** basis for $R^n$.



### Spectral Decomposition ###

Let $A$ be an $(n\times n)$ symmetric matrix with eigenvalues $\lambda_{1}, \dots, \lambda{n}$. Let $\mathbf{u}_{1}, \dots, \mathbf{u}_{n}$ be a corresponding set of orthonormal eigenvectors. where $A\mathbf{u}_{i} = \lambda_{i}\mathbf{u}_{i}$. Matrix $A$ can be expressed in the form:
$$
A = \lambda_{1}\mathbf{u}_{1}\mathbf{u}_{1}^{T} + \lambda_{2}\mathbf{u}_{2}\mathbf{u}_{2}^{T} + \cdots + \lambda_{n}\mathbf{u}_{n}\mathbf{u}_{n}^{T}
$$
Each $(n\times n)$ matrix $\mathbf{u}_{i}\mathbf{u}_{i}^{T}$ is a rank-one matrix. And the equation above is called **spectral decomposition** of $A$.



*Proof.* Let $U = [\mathbf{u}_{1}, \dots, \mathbf{u}_{n}]$, because $\{ \mathbf{u}_{1}, \dots, \mathbf{u}_{n} \}$ is an orthonormal vector set, so $U$ is an orthogonal matrix. We have $UU^{T} = I$. So:
$$
A = AUU^T = A\sum_{i=1}^{n}\mathbf{u}_{i}\mathbf{u}_{i}^{T} = \sum_{i=1}^{n}A\mathbf{u}_{i}\mathbf{u}_{i}^{T} \\
A\mathbf{u}_{i} = \lambda_{i}\mathbf{u}_{i}
$$
Then
$$
A = \sum_{i=1}^{n}\lambda_{i}\mathbf{u}_{i}\mathbf{u}_{i}^{T}
$$

