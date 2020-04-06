# Linear Transformation #

[TOC]

## Linear Transformation ##

Linear transformations can be viewed as an extension of the notion of a matrix to general vector spaces.



> *Def.* **Linear Transformation**
>
> Let $U$ and $V$ be vector spaces, and let $T$ be a function from $U$ to $V$, $T: U\rightarrow V$. We say that $T$ is a linear transformation if $\forall\ \mathbf{u}, \mathbf{v}\in U$ and all scalars $a$, we have:
>
> 1. $T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$.
> 2. $T(a\mathbf{u}) = aT(\mathbf{u})$
>
> *Remark.* $T(c_{1}\mathbf{v}_{1} + c_{2}\mathbf{v}_{2} + \cdots + c_{n}\mathbf{v}_{n}) = c_{1}T(\mathbf{v_{1}}) + c_{2}T(\mathbf{v_{2}}) + \cdots + c_{n}T(\mathbf{v_{n}})$.



> **Linear Transformation Using Basis in $R^{n}$**
>
> Let $V$ be vector space with basis $S=\{ \mathbf{u}_{1}, \mathbf{u}_{2}, \cdots , \mathbf{u}_{p} \}$. Let linear transformation $T:V\rightarrow U$ . For any vector $\mathbf{v}\in V$, we have 
> $$
> \mathbf{v} = a_{1}\mathbf{u}_{1} + a_{2}\mathbf{u}_{2} + \cdots + a_{p}\mathbf{u}_{p} \\
> T(\mathbf{v}) = a_{1}T(\mathbf{u}_{1}) + a_{2}T(\mathbf{u}_{2}) + \cdots + a_{p}T(\mathbf{u}_{p})
> $$
> *Th.* Let $T:\mathcal{R}^{n} \rightarrow \mathcal{R}^{m}$ be a linear transformation, and let $\mathbf{e}_{1}, \mathbf{e}_{2}, \cdots \mathbf{e}_{n}$ be the unit vectors in $\mathcal{R}^{n}$. If $A$ is an $(m\times n)$ matrix defined by:
> $$
> A = [T(\mathbf{e}_{1}), T(\mathbf{e}_{2}), \dots, T(\mathbf{e}_{n})]
> $$
> Then we have $T(\mathbf{x}) = A\mathbf{x}$ for all $\mathbf{x} \in \mathcal{R}^{n}$.
>
> *Proof.*:
> $$
> \mathbf{x} = \sum_{i=1}^{n}x_{i}\mathbf{e}_{i} \\
> T(\mathbf{x}) = \sum_{i=1}^{n}x_{i}T(\mathbf{e}_{i}) = A\mathbf{x}
> $$



**The Matrix of Transformation**

Suppose that $U$ and $V$ both have finite dimension, say $dim(U)=n$ and $dim(V) = m$. We have that $U$ is isomorphic to $R^{n}$ and $V$ is isomorphic to $R^m$. Let $B$ be a basis for $U$ and $C$ be a basis for $V$. Then each vector $\mathbf{u}\in U$ and $\mathbf{v} \in V$ can be represented by the vectors $[\mathbf{u}]_{B}\in R^n$ and $[\mathbf{v}]_{C}\in R^m$. Then the linear transformation $T:U\rightarrow V$ can be represented by an $(m\times n)$ matrix $Q$ in the sense that if $T(\mathbf{u}) = \mathbf{v}$, then $Q[\mathbf{u}]_{B} = [\mathbf{v}]_{C}$. 



> *Def.* **The Matrix of a Transformation**
>
> Let $T:U\rightarrow V$ be a linear transformation, where $dim(U) = n$ and $dim(V) = m$. Let $B = \{ \mathbf{u}_{1}, \mathbf{u}_{2}, \cdots, \mathbf{u}_{n} \}$ be a basis for $U$ and let $C = \{ \mathbf{v}_{1}, \mathbf{v}_{2}, \cdots, \mathbf{v}_{m} \}$ be a basis for $V$. The **matrix representation** for $T$ with respect to the bases $B$ and $C$ is the $(m\times n )$ matrix $Q$ defined by:
> $$
> Q = [\mathbf{Q}_{1}, \mathbf{Q}_{2}, \cdots, \mathbf{Q}_{n}]. \\
> \mathbf{Q}_{j} = [T(\mathbf{u}_{j})]_{C}
> $$
>
> and we have:
> $$
> Q[\mathbf{u}]_{B} = [\mathbf{v}]_{C}\ \text{ if }\ T(\mathbf{u}) = \mathbf{v}.
> $$
> *Proof.*
> $$
> [\mathbf{u}]_{B} = [b_{1}, b_{2}, \cdots, b_{n}]^{T}. \\
> Q[\mathbf{u}]_{B} = \sum_{i=1}^{n}b_{i}\mathbf{Q}_{i} = \sum_{i=1}^{n}b_{i}[T(\mathbf{u}_{i})]_{C} = [T(\sum_{i=1}^{n}b_{i}T(\mathbf{u}_{i}))]_{C} = [T(\mathbf{u})]_{C} = [\mathbf{v}]_{C}.
> $$
>



> *Th.* **The Representation Theorem**
>
> Let $T:U\rightarrow V$ be a linear transformation, where $dim(U) = n$ and $dim(V) = m$. Let $B$ and $C$ be bases for $U$ and $V$, and let $Q$ be the matrix of $T$ relative to $B$ and $C$. If $\mathbf{u}$ is a vector in $U$ and $T(\mathbf{u}) = \mathbf{v}$, then:
> $$
> Q[\mathbf{u}]_{B} = [\mathbf{v}]_{C}
> $$
> Moreover, $Q$ is the unique matrix that satisfies the equation above.
>
> 
>
> *Corollary.* Let $T_{1}$, $T_{2}$ and $T$ be transformation from U to V and let $Q_{1}$, $Q_{2}$ and $Q$ be the matrix representations with respect to $B$ and $C$ for $T_{1}, $ $T_{2}$ and $T$. Then:
>
> 1. $Q_{1} + Q_{2}$ is the matrix representation for $T_{1} + T_{2}$ with respect to $B$ and $C$.
> 2. For a scalar $a$, $aQ$ is the matrix representation for $aT$ with respect to $B$ and $C$.



> **Composition**
>
> *Th.* Let $T:U\rightarrow V$ and $S:V\rightarrow W$ be linear transformations, and suppose $dim(U)=n$, $dim(V) = m$ and $dim(W) = k$. Let $B$, $C$, $D$ be bases for $U$, $V$ and $W$. If the matrix for $T$ relative to $B$ and $C$ is $Q_{m\times n}$ and the matrix for $S$ relative to $C$ and $D$ is $P_{k\times m}$, then the matrix representation for $S\circ T$ is $PQ$.



> *Def.* **Null Space and Range**
>
> Let $V$ and $W$ be subspaces, and let $T:V\rightarrow W$ be a linear transformation. The **null space** of $T$, denoted by $\mathcal{N}(T)$, is the subset of $V$ given by:
> $$
> \mathcal{N}(T)=\{ \mathbf{v} | \mathbf{v}\in V \text{ and } T(\mathbf{v}) = \mathbf{\theta_{W}} \}
> $$
> The **range** of $T$, denoted by $\mathcal{R}(T)$, is the subset of $W$ defined by:
> $$
> \mathcal{R}(T) = \{ \mathbf{w} | \mathbf{w} \in W \text{ and for some } \mathbf{v} \in V\text{, we have }\mathbf{w}=T(\mathbf{v}) \}.
> $$
> We know that there exists a matrix $A$ s.t. $T(\mathbf{x}) = A\mathbf{x}$. In this case we have:
>
> 1. $\mathcal{N}(T) = \mathcal{N}(A)$.
> 2. $\mathcal{R}(T) = \mathcal{R}(A)$.



> *Def.* **One to One Linear Transformation**
>
> We say a linear transformation $T:U \rightarrow V$ in **one to one** if $T(\mathbf{u}) = T(\mathbf{v})$ implies $\mathbf{u} = \mathbf{v}$ for all $\mathbf{u}$ and $\mathbf{v}$ in $U$.
>
> *Remark.* One to one linear transformation has strong relation with unique solution $A\mathbf{x} = \mathbf{b}$.



> *Th.* Let $T:U\rightarrow V$ be a linear transformation. Then:
>
> 1. $T(\mathbf{\theta}_{U}) = \mathbf{\theta}_{V}$.
> 2. $\mathcal{N}(T)$ is a subspace of $U$.
> 3. $\mathcal{R}(T)$ is a subspace of $V$.
> 4. $T$ is one to one if and only if $\mathcal{N}(T) = \{ \mathcal{\theta}_{U}\}$; that is, $T$ is one to one if and only if $\text{nullity}(T)=0$.



> *Th.* [**for finite-dimensional vector space only**]
>
> Let $T:U\rightarrow V$ be a linear transformation and let $U$ be $p$-dimensional, where $B = \{ \mathbf{u}_{1}, \mathbf{u}_{2}, \cdots, \mathbf{u}_{p} \}$ is a basis for $U$.
>
> 1. $\mathcal{R}(T) = Sp\{ T(\mathbf{u}_{1}), T(\mathbf{u}_{2}), \cdots, T(\mathbf{u}_{p}) \}$.
> 2. $T$ is one to one if and only if $\{ T(\mathbf{u}_{1}), T(\mathbf{u}_{2}), \cdots, T(\mathbf{u}_{p}) \}$ is linearly independent in $V$.
> 3. $rank(T) + nullity(T) = p$.



> *Def.* **Operations with Linear Transformations**
>
> Let $U$ and $V$ be vector spaces and let $T_{1}$ and $T_{2}$ be linear transformations, where $T_{1}:U\rightarrow V$ and $T_{2}: U\rightarrow V$. 
>
> 1. **Sum**: $T_{3}:U\rightarrow V$, $T_{3}=T_{1} + T_{2}$ means $T_{3}(\mathbf{u}) = T_{1}(\mathbf{u}) + T_{2}(\mathbf{u})$.
> 2. **Scalar Product**: $aT$ denotes $(aT)(\mathbf{u}) = a(T(\mathbf{u}))$.
> 3. **Composition**: Let $U, V, W$ be vector space, let $S$ and $T$ be linear transformations, where $S:U\rightarrow V$ and $T:V\rightarrow W$. The composition, $L=T\circ S$, of $S$ and $T$ is defined to be function $L:U\rightarrow W$ given by $L(\mathbf{u}) = T(S(\mathbf{u}))$.



> *Def.* **Onto**(满射)
>
> A function $f:X\rightarrow Y$ is **onto** provided that $\mathcal{R}(f) = Y$. A linear transformation $T:U\rightarrow V$ is **onto** provided that $\mathcal{R}(T)=V$.



> *Def.* **Inverse**
>
> Let $f:X\rightarrow Y$ be a function. If $f$ is both one to one and onto, then the **inverse** of $f$, denoted by $f^{-1}:Y\rightarrow X$, is the function defined by:
> $$
> f^{-1}(y) = x \text{  if and only if  } f(x) = y.
> $$
> Therefore, if $T:U\rightarrow V$ is a linear transformation that is both one to one and onto, then the inverse function $T^{-1}:V\rightarrow U$ is defined.



> *Def.* **Invertible Linear Transformations**
>
> A linear transformation $T:U\rightarrow V$ that is both one to one and onto is called an **invertible** linear transformation. 



> *Th.* Let $U$ and $V$ be vector spaces, and let $T:U\rightarrow V$ be an invertible linear transformation. Then:
>
> 1. $T^{-1}:V\rightarrow U$ is a linear transformation.
> 2. $T^{-1}$ is invertible and $(T^{-1})^{-1} = T$.
> 3. $T^{-1}\circ T=I_{U}$ and $T\circ T^{-1}=I_{V}$, where $I_{U}$ and $I_{V}$ are the identity transformations on $U$ and $V$.
> 4. For each vector $\mathbf{b}\in V$, $\mathbf{x} = T^{-1}(\mathbf{b})$ is the unique solution of $T(\mathbf{x}) = \mathbf{b}$.
> 5. If $S$ and $T$ are invertible and $S\circ T$ is defined, then $S\circ T$ is invertible and $(S\circ T)^{-1} = T^{-1} \circ S^{-1}$.
>
> *Note.* Almost all properties of invertible matrix can be used in invertible linear transformation.



> **What is isomorphic**
>
> Suppose invertible transformation $T:U\rightarrow V$ is both one to one and onto, $T$ established an exact pairing between elements of $U$ and $V$. Moreover, because $T$ is a linear transformation, this pairing preserves algebraic properties. Therefore, although $U$ and $V$ may be different sets, they may be regraded as indistinguishable(or equivalent) algebraically. Stated another way, $U$ and $V$ both represent just one underlying vector space but perhaps with different "labels" for the elements. The invertible linear transformation $T$ acts as a translation from one set of labels to another.



> *Def.* **Isomorphic Vector Space**
>
> If $U$ and $V$ are vector spaces and if $T:U\rightarrow V$ is an invertible linear transformation, then $U$ and $V$ are said to be **isomorphic vector space**. Also, an invertible transformation $T$ is called an **isomorphism**.



> *Th.* If $U$ is a real $n$-dimensional vector space, then $U$ and $R^n$ are isomorphic.
>
> *Corollary.* If $U$ and $V$ are real $n$-dimensional vector spaces, then $U$ and $V$ are isomorphic.



## Change of Basis and Diagonalization ##

A linear transformation from $U$ to $V$ can be represented as an $(m\times n)$ matrix when $dim(U) = n$ and $dim(V) = m$. A consequence of this representation is that properties of transformations can be studied by examining their corresponding matrix representations.

For change of basis, we consider only transformations from $V$ to $V$. If we are interested in the properties of $T$, then it is reasonable to search for a basis for $V$ that makes the matrix representation of $T$ as simple as possible. Finding such a basis is the subject of this section.



> *Def.* **Diagonalizable Transformations**
>
> If $T$ is a linear transformation with a matrix representation that is diagonal, then $T$ is called diagonalizable.



> *Def.* **Eigenvalue and Eigenvector in General Vector Space Setting**
>
> A scalar $\lambda$ is called an **eigenvalue** for a linear transformation $T:V\rightarrow V$ provided that there is a **nonzero** vector $\mathbf{v} \in V$ such that $T(\mathbf{v}) = \lambda \mathbf{v}$. $\mathbf{v}$ is called an **eigenvector** for $T$ corresponding to $\lambda$.



> *Th.* Let $V$ be an $n$-dimensional vector space. A linear transformation $T:V\rightarrow V$ is diagonalizable if and only if there exists a basis for $V$ consisting of eigenvectors for $T$.



> *Th.* **Change of Basis**
>
> Let $B$ and $C$ be bases for the vector space $V$, with $B = \{ \mathbf{u}_{1}, \mathbf{u}_{2}, \cdots, \mathbf{u}_{n} \}$, and let $P_{n\times n}$ be the matrix given by $P=[\mathbf{P}_{1}, \mathbf{P}_{2}, \cdots, \mathbf{P}_{n}]$, where the $i$th column of $P$ is:
> $$
> \mathbf{P}_{i} = [\mathbf{u}_{i}]_{C}
> $$
> Then $P$ is nonsingular matrix and 
> $$
> [\mathbf{v}]_{C} = P[\mathbf{v}]_{B}
> $$
> The matrix $P$ is called the **transition matrix**. Since $P$ is nonsingular, we have
> $$
> [\mathbf{v}]_{B} = P^{-1}[\mathbf{v}]_{C}
> $$
> 
>
> *Proof.*: The linear transformation here is $T:V\rightarrow V$, or $T(\mathbf{v}) = \mathbf{v}$. Then the **The Representation Theorem** applies. For the fact that $P$ is nonsingular, we have:
> $$
> \sum_{i=1}^{n}a_{i}\mathbf{P}_{i} = \sum_{i=1}^{n}a_{i}[\mathbf{u}_{i}]_{C} = \sum_{i=1}^{n}[a_{i}\mathbf{u}_{i}]_{C} = [\theta]_{C} \\
> \text{And we have: }\sum_{i=1}^{n}a_{i}\mathbf{u}_{i} = \theta
> $$



**Matrix Representation and Change of Basis**

Given a basis $B$, the relationship between the matrix representations of a linear transformation with respect to two different bases suggests how to determine a basis $C$ such that the matrix relative to $C$ is simpler matrix.



> *Th.* Let $B$ and $C$ be bases for the $n$-dimensional vector space $V$, and let $T:V\rightarrow V$ be a linear transformation. If $Q_{1}$ is the matrix of $T$ with respect to $B$ and if $Q_{2}$ is the matrix of $T$ with respect to $C$, then:
> $$
> Q_{2} = P^{-1}Q_{1}P
> $$
> where P is the transition matrix from $C$ to $B$.
>
> *Proof.* $\forall\ \mathbf{v}\in V$, we have
> $$
> Q_{2}[\mathbf{v}]_{C} = [\mathbf{v}]_{C} = P^{-1}[\mathbf{v}]_{B} = P^{-1}Q_{1}[\mathbf{v}]_{B} = P^{-1}Q_{1}P[\mathbf{v}]_{C}
> $$
> and $Q_{2}$ is unique, so
> $$
> Q_{2} = P^{-1}Q_{1}P
> $$



**Application in Eigenvalue**

If $Q$ is similar to a diagonal matrix $R$. If we choose $\{ \mathbf{S}_{1}, \mathbf{S}_{2}, \cdots, \mathbf{S}_{n} \}$ to be a basis of $R^n$ consisting of eigenvectors for $Q$, then
$$
R = S^{-1}QS = 
\begin{bmatrix}
d_1		& 0		& \cdots & 0 \\
0		& d_2	& \cdots & 0 \\
\vdots	& ~		& ~		 & \vdots \\
0		& 0		& \cdots & d_n
\end{bmatrix}
$$
where  $d_i$ are eigenvalues for $Q$ and where $Q\mathbf{S}_{i} = d_{i}\mathbf{S}_{i}$.

