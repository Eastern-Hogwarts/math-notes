# Basic Concepts of Linear Algebra #


[TOC]


## Linear Systems ##


> *Def.* **Equivalent linear systems**
> 
> Two systems of linear equations on $u$ unknowns are **equivalent** provided that they have the same set of solutions

  


> *Def.* **Raw Operations**
> 
> The following operations, performed on the rows of a matrix, are called **elementary row operations**:
> 
> 1. Interchange two rows.
> 2. Multiply a row by a **nonzero** scalar.
> 3. Add a constant multiple of one row to another.

  


> *Def.* **Raw Equivalent**
> 
> We say two matrices with same shape, $B$ and $C$,  are **raw equivalent** if one can be obtained from the other by a sequence of elementary row operations.
> 
> *Corollary.* Suppose $[A|\vec{b}]$ and $[C|\vec{d}]$ are augmented matrices with same shape. If these two augmented matrices are row equivalent matrices, then the two systems are also equivalent.




> *Def.* **Echelon Form**
> 
> An $m\times n$ matrix $B$ is in **Echelon Form** if:
> 
> 1. All rows whose elements are all zero are at the bottom of the matrix.
> 2. In every nonzero row, the first nonzero entry is 1.
> 3. If the ($i+1$)-st row contains nonzero entries, then the 1-st non-zero entry is in a column to the right of the first nonzero entry in the $i$-th row.




> *Def.* **Reduced Echelon Form**
> 
> A matrix that is in echelon form is also in **reduced echelon form** provided that the first nonzero entry in any row is the **only** nonzero entry in its **column**.
> 
> *Note*: The reduced echelon form of a linear system is unique.




> *Def.* **Inconsistent System**
> 
> If a linear system whose augmented matrix $[A|\vec{b}]$ is in reduced echelon form and the last nonzero row of it has its leading 1 in the last column, then the linear system is inconsistent and has no solution.




> *Th.* Let $A=[C|\vec d]$ be an matrix whose shape is [m, n+1] in reduced echelon form, where $[C|\vec{d}]$ represents a consistent system. Let $A$ have $r\leq m$ nonzero rows. Then $r \leq n$ and in the solution of the system there are $n-r$ variables that can be assigned arbitrary values.
>
> *Remark.* $r$: number of relation between variable or the **rank**, $x_i$. $n-r$: number of free variable.
>
> *Corollary.* Consider an $(m\times n)$ system of linear equations. If $m < n$, then either the system is inconsistent or it has infinitely many solutions.




> *Def.* **Homogeneous System**
> 
> A $(m\times n)$ system of linear equation given below in called a **homogeneous system** of linear equations:
> 
> $$
> a_{1,1}x_{1} + a_{1,2}x_{2} + \cdots + a_{1,n}x_{n} = 0 \\
> a_{2,1}x_{1} + a_{2,2}x_{2} + \cdots + a_{2,n}x_{n} = 0 \\
> \cdots \\
> a_{m,1}x_{1} + a_{m,2}x_{2} + \cdots + a_{m,n}x_{n} = 0
> $$
> 
> *Remark.* Homogeneous system always has a solution $x_{i}=0\ \forall i$ and this solution is called **trivial solution** or zeros solution, and other solution is called a **nontrivial solution**.
> 
> *Th.* A homogeneous system of linear equations with shape $m\times n$ always has infinitely many **nontrivial solutions** when $m < n$ . [From the corollary above]



### Application of Homogeneous System: Conic Sections and Quadric Surfaces ###

An interesting application of homogeneous equations involves the quadratic equation in two variables.

$$
ax^2 + bxy + cy^2 + dx + ey + f = 0
$$

If the equation above has real solutions, then the graph is a curve in the $xy$-plane. If at least one of $a$, $b$ and $c$ is nonzero, the resulting graph is known as a **conic section**. 

## Matrix ##

> *Def.* **Matrix Product**
> 
> **Scalar Definition**
> 
> Let $A=(a_{i,j})$ be an $(m\times n)$  matrix, and let $B=(b_{i,j})$ be an $(r\times s)$ matrix. If $n=r$, then the product $AB$ is the matrix $(m\times s)$ matrix defined by:
> $$
> (AB)_{i,j}=\sum_{k=1}^{n}a_{i,k}b_{k,j}
> $$
> **Vector Definition**
> 
> *Lemma.* Let $A=[\mathbf{A}_{1}, \mathbf{A}_{2}, \dots , \mathbf{A}_{n}]$ , where for each $j,\ 1\leq j \leq n$ , $\mathbf{A}_{j}$ denotes the $j$-th column vector of $A$ with shape $(m\times 1)$. And let vector $\mathbf{x}$ with shape $(n\times 1)$, we have:
> $$
> A\mathbb{x} = x_{1}\mathbf{A}_{1} + x_{2}\mathbf{A}_{2} + \cdots + x_{n}\mathbf{A}_{n}
> $$
> Let  $A=[\mathbf{A}_{1}, \mathbf{A}_{2}, \dots , \mathbf{A}_{n}]$ with shape $(m\times n)$ and $B=[\mathbf{B}_{1}, \mathbf{B}_{2}, \dots , \mathbf{B}_{s}]$ with shape $(n\times s)$, we have 
> $$
> AB = A[\mathbf{B}_{1}, \mathbf{B}_{2}, \dots , \mathbf{B}_{s}] = [A\mathbf{B}_{1}, A\mathbf{B}_{2}, \dots , A\mathbf{B}_{s}]
> $$
> **Dot Product Definition**
> 
> Let $A=[\mathbf{\alpha}^{T}_{1} ; \mathbf{\alpha}^{T}_{2}; \cdots ; \mathbf{\alpha}^{T}_{m}]$ be an $(m\times n)$ matrix with row vector $\mathbf{\alpha}^{T}_{i}$ . And $B=[\mathbf{B}_{1}, \mathbf{B}_{2}, \dots , \mathbf{B}_{s}]$ with shape $(n\times s)$, the product $AB$ is matrix:
> $$
> (AB)_{i,j} = \mathbf{\alpha}_{i}^{T} \mathbf{B}_{j}
> $$
> **Matrix Definition**
> 
> Let $A=[\mathbf{A}_{1}, \mathbf{A}_{2}, \dots , \mathbf{A}_{n}]$ and $B=[\mathbf{\beta}^{T}_{1} ; \mathbf{\beta}^{T}_{2}; \cdots ; \mathbf{\beta}^{T}_{n}]$, we have:
> $$
> AB = \sum_{k=1}^{n}\mathbf{A}_{k}\mathbf{\beta}_{k}^{T} \\
> (\mathbf{A}_{k}\mathbf{\beta}_{k}^{T})_{i,j} = A_{i,k}B_{k,j}
> $$
>




> *Prop.* **Properties of Matrix Operations**
> 
> 1. $A+B=B+A$
> 2. $(A+B)+C=A+(B+C)$
> 3. $\exist$ unique matrix $O$ with shape $(m\times n)$ that $A + O = A$ for any matrix $A$ with shape $(m\times n)$.
> 4. Given an $(m \times n)$ matrix $A$, there exists a unique matrix $P$ with shape $(m\times n)$ s.t. $A + P = O$ 
> 5. Given matrices $A, B, C$ with shape $(m\times n), (n\times p), (p\times q)$, we have $(AB)C = A(BC)$
> 6. $r, s$ are scalars, we have $r(sA)=(rs)A$
> 7. $r(AB)=(rA)B=A(rB)$
> 8. With valid shape, we have $(A+B)C=AC+BC$
> 9. With valid shape, we have $A(B+C)=AB+AC$
> 10. $(r+s)A=rA+sA$
> 11. $r(A+B)=rA+rB$




> *Def.* **Transpose of a Matrix**
> 
> If $A=(a_{i,j})$ is an $(m\times n)$ matrix, then the **transpose** of $A$, denoted as $A^{T}$, is the $(n\times m)$ matrix $A^{T}=(b_{i,j})$ and $b_{j,i}=a_{i,j}$.
> 
> *Prop.*
> 
> 1. $(A+B)^{T} = A^{T} + B^{T}$
> 2. $(AB)^{T} = B^{T}A^{T}$
> 3. $(A^{T})^{T} = A$




> *Def.* **Symmetric Matrix** 
> 
> A matrix $A$ is symmetric if $A=A^{T}$ 
> 
> *Prop.* $Q^{T}Q$ is **always** a symmetric matrix.



> *Def.* **Skew Symmetric Matrix**
>
> A **square matrix**, $A=(a_{i,j})$, is called **skew symmetric** if $A^{T} = -A$.



## Linear Independence and Non-singular Matrix

> *Def.* **Linear Combination**
>
> If $A=[\mathbf{A}_{1}, \mathbf{A}_{2}, \cdots , \mathbf{A}_{n}]$, we call $x_{1}\mathbf{A}_{1} + x_{2}\mathbf{A}_{2} + \cdots + x_{n}\mathbf{A}_{n}$ a linear combination of the vectors $\mathbf{A}_{1}, \mathbf{A}_{2}, \cdots , \mathbf{A}_{n}$.




> *Th.* System of linear equations $A\mathbf{x}=\mathbf{b}$ is consistent if and only if $\mathbf{b}$ if a linear combination of the columns of $A$.
>
> *Note.* Here $\mathbf{x}$ is variable and unknown.
>
> *Remark.* Homogeneous system $A\mathbf{x}=\mathbf{\theta}$ always has a trivial solution $\mathbf{x}=\mathbf{\theta}$.




> *Def.* **Linearly Independence**
>
> A set of m-dimensional vectors $\{ \mathbf{v}_{1}, \mathbf{v}_{2}, \cdots , \mathbf{v}_{p} \}$ is said to be **linearly independent** if the **only** solution to the vector equation
> $$
> a_{1}\mathbf{v}_{1} + a_{2}\mathbf{v}_{2} + \cdots + a_{p}\mathbf{v}_{p} = \mathbf{\theta} \\
> \text{or} \\
>  V\mathbf{a} = \mathbf{\theta} \text{ where } V = [\mathbf{v}_{1}, \mathbf{v}_{2}, \cdots , \mathbf{v}_{p}]
> $$
> is the trivial solution $a_{1} = a_{2} = \cdots = a_{p} = 0$.
>
> The set of vectors is said to be **linearly dependent** if it is not linearly independent. That is, the set is linearly dependent if we can find a non-trivial solution to the equation above.
>
> *Remark.* If a set of vectors has zero vector, then this set of vector must be linearly dependent.



> *Th.* Let $\{ \mathbf{v}_{1}, \mathbf{v}_{2}, \cdots , \mathbf{v}_{p} \}$ be a set of vectors in $\mathcal{R}^{m}$. If $p>m$, then this set is linearly dependent. Else if $p \leq m$, this set of vectors may be either linearly independent or linearly dependent.



> *Def.* **Non-singular Matrix**
>
> An $(n\times n)$ matrix $A$ is **nonsingular** if the only solution to $A\mathbf{x} = \mathbf{\theta}$ is its trivial solution. Otherwise $A$ is singular matrix.
>
> *Corollary.* The $(n\times n)$ matrix $A=[\mathbf{A}_{1}, \mathbf{A}_{2}, \cdots , \mathbf{A}_{n}]$ is nonsingular matrix if and only if the set of vector $\{ \mathbf{A}_{1}, \mathbf{A}_{2}, \cdots , \mathbf{A}_{n} \}$ is linearly independent.  



> *Th.* Let $A$ be an $(n\times n)$ matrix. The equation $A\mathbf{x} = \mathbf{b}$ has **unique** solution for any $(n\times 1)$ column vector $\mathbf{b}$ if and only if $A$ is nonsingular.
>
> *proof.*: $A\mathbf{x}=\mathbf{b}$ must has solution because $A$ is row equivalent to $I$ and $A$ is square matrix. If $A\mathbf{x}_{1} = \mathbf{b} = A\mathbf{x}_{2}$ and $\mathbf{x}_{1} \neq \mathbf{x}_{2}$, we have: $A(\mathbf{x}_{1} - \mathbf{x}_2) = \theta$. But $A\mathbf{v} = \mathbf{\theta}$ has only trivial solution, so $\mathbf{x}_{1} = \mathbf{x}_{2}$, which is a conflict. QED.



## Matrix Inverse and Properties ##

> *Def.* **Matrix Inverse**
>
> Let $A$ be an $(n\times n)$ matrix. We say that $A$ is **invertible** if we can find an $(n\times n)$ matrix $A^{-1}$ s.t.:
> $$
> A^{-1}A = AA^{-1} = I.
> $$
> The matrix $A^{-1}$ is called an inverse for $A$. 
>
> *Note.* If $A$ is invertible, then $A^{-1}$ is unique.



### The Existence of Inverses

> *Lemma.* Let $P$, $Q$ and $R$ be $(n\times n)$ square matrix s.t. $PQ=R$. We have
> $$
> (P \text{ is singular}) \or (Q \text{ is singular}) \rightarrow (R \text{ is singular})
> $$
>



> *Th.* Let $A$ be an $(n\times n)$ matrix. Then $A$ is invertible if and only if $A$ is nonsingular. 
>
> *remark.* 
>
> * If $A$ is invertible. we have $AB =BA = I$ and $B$ is unique, or $A\mathbf{B}_{i} = e_{i}$ has unique solution $\mathbf{B}_{i}$ for $i=1,\dots,n$. And for any vector $\mathbf{b}$, it can be represent by $e_{i}$ uniquely, i.e. for any vector $\mathbf{b}$, $A\mathbf{x} =\mathbf{b}$ has unique solution, which means $A$ is non-singular.
> * If A is non-singular, we can find unique vector $\mathbf{B}_{i}$ such that $A\mathbf{B}_{i} = e_{i}$, which means we can find unique matrix $B$ such that $AB = I$. 



> *Th.* Let $A$ be an $(n\times n)$ matrix. Then $A$ is nonsingular if and only if $A$ is row equivalent to $I$.



> *Prop.* **Properties of Matrix Inverse**
>
> Let $A$ and $B$ be $(n\times n)$ matrices, each of which has an inverse. Then:
>
> 1. $A^{-1}$ has an inverse and $(A^{-1})^{-1}=A$.
> 2. $AB$ has an inverse, and $(AB)^{-1}=B^{-1}A^{-1}$.
> 3. If $k\neq0$, then $kA$ has an inverse and $(kA)^{-1} = (1/k)A^{-1}$.
> 4. $A^{T}$ has an inverse and $(A^T)^{-1} = (A^{-1})^T$.



> *Th.* Let $A$ be an $(n\times n)$ matrix. The following are equivalent:
>
> 1. $A$ is nonsingular.
> 2. The column vectors of $A$ are linearly independent.
> 3. $A\mathbf{x}=\mathbf{b}$ always has a unique solution.
> 4. $A$ is invertible.
> 5. $A$ is row equivalent to $I$.



## Ill-Conditioned Matrix ##

In applications the equation $A\mathbf{x} = \mathbf{b}$ often serves as a mathematical model for a physical problem. In these cases it is important to know whether solutions to this system are sensitive to small changes in the right-hand side $\mathbf{b}$. If small changes in $\mathbf{b}$ can lead to relatively large changes in the solution $\mathbf{x}$, then the matrix $A$ is called **ill-conditioned**.



Ill-conditioned matrix usually has large scale inverse.



## Partitioned Matrix (Block Matrix) ##

A matrix $A$ is a (2 x 2) **block matrix** if it is represented in the form:
$$
A = 
\begin{bmatrix}
A_{1} & A_{2} \\
A_{3} & A_{4}
\end{bmatrix}
$$
Note that the matrix $A$ need not be a square matrix. The partition can have any shape.

Now suppose matrix $B$ is also a (2 x 2) block matrix given by:
$$
B = 
\begin{bmatrix}
B_{1} & B_{2} \\
B_{3} & B_{4}
\end{bmatrix}
$$
with all submatrix products valid, we have:
$$
AB = 
\begin{bmatrix}
A_{1}B_{1} + A_{2}B_{3} & A_{1}B_{2} + A_{2}B_{4} \\
A_{3}B_{1} + A_{4}B_{3} & A_{3}B_{2} + A_{4}B_{4}
\end{bmatrix}
$$

