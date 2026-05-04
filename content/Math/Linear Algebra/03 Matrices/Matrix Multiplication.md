---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

Matrix multiplication $AB$ represents the composition of two [[Linear Transformation]]s: applying $\mathbf{B}$ first, then $\mathbf{A}$. The calculation involves multiplying $\mathbf{A}$ by each column of $\mathbf{B}$.

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
