# Determinant #

If $A$ is an $(n\times n)$ matrix, the determinant of $A$, denoted $det(A)$, is a number that we associate with $A$. Determinants are usually defined either in terms of *cofactors* or in terms of *permutations*, and we elect to use the cofactor definition here.

[TOC]

## Definition ##

> *Def.* **Cofactor**
>
> Let $A=(a_{i,j})$ be an $(n\times n)$ matrix, and let $M_{r,s}$ denote the $[(n-1)\times (n-1)]$ matrix obtained by deleting the $r$th row and $s$th column of $A$. Then $M_{r, s}$ is called a **minor matrix** of $A$, and the number $det(M_{r,s})$ is the minor of the $(r,s)$th entry, $a_{r,s}$. In addition, the numbers:
> $$
> A_{i,j} = (-1)^{i+j}det(M_{i,j})
> $$
> are called **cofactors** (or **signed minors**).



> *Def.* **Determinant(cofactor)**
>
> Let $A=(a_{i,j})$ be an $(n\times n)$ matrix. Then the **determinant** of $A$ is:
> $$
> det(A) = a_{1,1}A_{1,1} + a_{1,2}A_{1,2} + \cdots + a_{1,n}A_{1,n}
> $$
> where $A_{i,j}$ is the cofactor of $a_{i,j}$



> *Def.* **Permutation**
>
> A **permutation** $(j_{1}, j_{2}, \cdots, j_{n})$ of the set $S=\{ 1,2,\cdots, n \}$ is just a rearrangement of the numbers in $S$. In **inversion** of this permutation occurs whenever a number $j_{r}$ is followed by a smaller number $j_{s}$, or $j_{r} > j_{s}$ but $r<s$. A permutation of $S$ is called *odd* or *even* if it has an odd or even number of inversions.



> *Def.* **Determinant(Permutation)**
>
> It can be shown that $det(A)$ is the sum of all possible terms of the form $\pm a_{1,j_{1}}a_{2,j_{2}}\cdots a_{n,j_{n}}$, where the sign is taken as $+$ or $-$, depending on whether the permutation is even or odd.
>
> Let $p=(j_{1}, j_{2}, \cdots, j_{n})$ be any permutation, we have:
> $$
> det(A) = \sum_{(j_{1}, j_{2}, \cdots, j_{n})}(-1)^{\Gamma(j_{1}, j_{2}, \cdots, j_{n})}\prod_{i=1}^{n}a_{i,j_i}
> $$



> *Th.* Let $T=(t_{i,j})$ be an $(n\times n)$ lower-triangular matrix. Then
> $$
> det(T) = \prod_{i=1}^{n}t_{i,i}
> $$





 ## Elementary Operations ##

> *Th.* If $A$ is an $(n\times n)$ matrix, then $det(A) = det(A^T)$



> *Th.* Let $A = [\mathbf{A}_{1}, \mathbf{A}_{2}, \cdots, \mathbf{A}_n]$ be an $(n\times n)$ matrix. If $B$ is obtained from $A$ by interchanging two rows (or columns) of $A$, then $det(B) = -det(A)$.



> *Th.* If $A$ is an $(n\times n)$ matrix, and if $B$ is the $(n\times n)$ matrix resulting from multiplying the $k$th column (or row) of $A$ by a scalar $c$, then $det(B) = c\cdot det(A)$.
>
> *Corollary.* $det(cA) = c^{n}A$



> *Th.* If $A$, $B$ and $C$ are $(n\times n)$ matrices that are equal except that the $s$th column (or row) if $A$ is equal to the sum of the $s$th column (or row) of $B$ and $C$, then $det(A) = det(B) + det(C)$
>
> *Note.* $det(A+B) \neq det(A) + det(B)$



> *Th.* Let $A$ be an $(n\times n)$ matrix. If the $j$th column (or row) of $A$ is a multiple of the $k$th column (or row) of $A$, then $det(A) = 0$.



> *Th.* If $A$ is an $(n\times n)$ matrix, and if a multiple of the $k$th column (or row) is added to the $j$th column (or row), then the determinant is not changed.



## Cramer's Rule ##

> *Lemma.* Let $A=[\mathbf{A}_{1}, \mathbf{A}_{2}, \cdots, \mathbf{A}_{n}]$ be an $(n\times n)$ matrix, and let $\mathbf{b}$ be any vector in $R^n$. For each $i,\ 1\leq i\leq n$, let $B_i$ be the $(n\times n)$ matrix:
> $$
> B_{i} = [\mathbf{A}_{1}, \dots, \mathbf{A}_{i-1}, \mathbf{b}, \mathbf{A}_{i+1}, \dots, \mathbf{A}_{n}].
> $$
> If the system of equations $A\mathbf{x} = \mathbf{b}$ is consistent and $x_i$ is the $i$th component of a solution, then:
> $$
> x_{i}det(A) = det(B_{i})
> $$



> *Th.* If $A$ is an $(n\times n)$ **singular** matrix, then $det(A) = 0$.
>
> *Proof.* $A$ is singular matrix, $A\mathbf{x} = \mathbf{b}$ has nontrivial solution. Choose $i$ s.t. $x_i \neq 0$, we have $x_{i}det(A) = det(B_{i})$. But $det(B_{i}) = 0$, and $x_i \neq 0$, so $det(A) = 0$.



> *Th.* If $A$ and $B$ are $(n\times n)$ matrices, then 
> $$
> det(AB) = det(A)det(B)
> $$



> *Lemma*. Let $A$ and $B$ be $(n\times n)$ matrices, and let $C = AB$. Let $\hat{C}$ denote the result of applying an elementary column operation to $C$ and let $\hat{B}$ denote the result of applying the same column operation to $B$. Then $\hat{C} = A\hat{B}$



> *Th.* If the $(n\times n)$ matrix $A$ is nonsingular, then $det(A)\neq 0$. Moreover, $det(A^{-1}) = 1/det(A)$.



> *Th.* **Cramer's Rule**
>
> Let $A=[\mathbf{A}_{1}, \cdots, \mathbf{A}_{n}]$ be a nonsingular $(n\times n)$ matrix, and let $\mathbf{b}$ be any vector in $R^n$. For each $i,\ 1\leq i\leq n$, let $B_{i}$ be the matrix $B_{i} = [\mathbf{A}_{1}, \dots, \mathbf{A}_{i-1}, \mathbf{b}, \mathbf{A}_{i+1}, \dots, \mathbf{A}_{n}]$. Then the $i$th component, $x_i$ of the solution of $A\mathbf{x}=\mathbf{b}$ is given by:
> $$
> x_{i} = \dfrac{det(B_{i})}{det(A)}.
> $$
> *Proof.* From the first lemma in this section.
>
> *Note.* Cramer's rule is a valuable theoretical tool instead of a practical tool for real computation.



## Applications of Determinants ##

### Inverses ###

> *Lemma.* Let $A$ be an $(n\times n)$ matrix. Then there is a nonsingular matrix $Q_{n\times n}$ such that $AQ=L$, where $L$ is lower triangular. Moreover, $det(Q^{T}) = det(Q)$.
>
> This Lemma can give the proof for the fact that $det(A) = det(A^T)$



> *Th.* Let $A=(a_{i,j})$ be an $(n\times n)$ matrix, Then:
> $$
> det(A) = a_{i,1}A_{i,1} + a_{i,2}A_{i,2} + \cdots + a_{i,n}A_{i,n} \\
> det(A) = a_{1,j}A_{1,j} + a_{2,j}A_{2,j} + \cdots + a_{n,j}A_{n,j}
> $$



> *Lemma.* If $A$ is an $(n\times n)$ matrix and if $i\neq k$, then $\sum_{j=1}^{n}a_{i,j}A_{k,j} = 0$.



> *Def.* **Adjoint Matrix**
>
> Let $A$ be an $(n\times n)$ matrix, and let $C$ denote the matrix of cofactors; $C=(c_{i,j})$ is $(n\times n)$, and $c_{i,j} = A_{i,j}$. The **adjoint matrix** of $A$, denoted $\text{Adj}(A)$, is equal to $C^T$.



> *Th.* If $A$ is an $(n\times n)$ **nonsingular** matrix, then
> $$
> A^{-1} = \dfrac{1}{\text{det}(A)}\text{Adj}(A).
> $$





## Elementary Matrices ##

The result of applying a sequence of elementary column operations to a matrix $A$ can be represented in matrix terms as multiplication of $A$ by a sequence of elementary matrices.



> *Def.* Let $I$ denote the $(n\times n)$ identity matrix, and let $E$ be the matrix that results when an elementary column operation is applied to $I$. Such a matrix $E$ is called an **elementary matrix**.



> *Th.* Let $E$ be the $(n\times n)$ elementary matrix that results from performing a certain column operation on the $(n\times n)$ identity matrix. If $A$ is any $(n\times n)$ matrix, then $AE$ is the matrix that results when this same column operation is performed on $A$.








