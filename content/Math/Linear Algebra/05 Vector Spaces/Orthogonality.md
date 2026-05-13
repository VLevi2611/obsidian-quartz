---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

**Orthogonality** defines perpendicular relationships between [[Vector|Vectors]] and [[Subspace|Subspaces]], and pair the [[Fundamental Subspaces]] of a [[Matrix]] into complementary structures.

Two vectors $\mathbf{u,v} \in \mathbb{R}^n$ are [[Orthogonal Vectors]] if their [[Dot Product]] is 0.
Two subspaces are orthogonal if **every vector** in one is orthogonal to **every vector** in the other.

Let $\mathbf{A} \in \mathbb{R}^{m \times n}$. 
In $\mathbb{R}^m$ 
$$
Row(\mathbf{A}) \perp Null(\mathbf{A})
$$
In $\mathbb{R}^n$ 
$$
Col(\mathbf{A}) \perp Null(\mathbf{A}^T)
$$
There are [[Dimension]]al relationships between the subspaces:
$$
\begin{aligned}
\dim (Row(\mathbf{A})) + \dim(Null(\mathbf{A})) &=n \\
\dim (Col(\mathbf{a})) + \dim(Null(\mathbf{A}^T)) &=m
\end{aligned}
$$
