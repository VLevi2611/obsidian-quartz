---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

Matrix multiplication $AB$ represents the composition of two [[Linear Transformation]]s: applying $B$ first, then $A$. The calculation involves multiplying $A$ by each column of $B$.

$$\mathbf{A}= 
\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{pmatrix},
\mathbf{B}=\begin{pmatrix}
b_{11} & b_{12} \\
b_{21} & b_{22}
\end{pmatrix} 
$$
$$\mathbf{AB} = \begin{pmatrix}
a_{11}b_{11} + a_{12}b_{21} & a_{11}b_{12} + a_{12}b_{22} \\
a_{21}b_{11} + a_{22}b_{21} & a_{21}b_{12} + a_{22}b_{22}
\end{pmatrix}$$
