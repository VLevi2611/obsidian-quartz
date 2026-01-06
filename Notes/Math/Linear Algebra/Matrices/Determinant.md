---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

The determinant of a [[Matrix]] $\det A$ measures the factor by with the area (2D) or volume (3D) is scaled by the [[Linear Transformation]].
If the determinant is 0, the space is compressed into a lower dimension.

--- 

### In $2*2$
$$\mathbf{A} = \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}$$
$$\det \mathbf{A}= \begin{vmatrix}
a & b \\
c & d
\end{vmatrix} = ad-bc$$

### In $3*3$

To calculate 3x3 and higher order matrices, we need to compute their minors.
The minor of the entry in the $i$ row and $j$ column $M_{i,j}$ is the determinant  of the submatrix formed by deleting the $i$ row and the $j$ column.
The determinant is the sum of all the minors multiplied by the base element.

$$\begin{vmatrix}
a & b & c \\
d & e & f \\
g & h & i 
\end{vmatrix}=
a \begin{vmatrix}
e & f \\
h & i
\end{vmatrix}+
b \begin{vmatrix}
d & f \\
g & i
\end{vmatrix}+
c \begin{vmatrix}
d & e \\
g & h
\end{vmatrix}
$$
---

### Properties

1. The determinant of the [[Identity Matrix]] is 1.
2. The exchange of two rows multiplies the determinant by -1.
3. Multiplying a row by a number multiplies the determinant by this number.
4. Adding a multiple of one row to another row does not change the determinant. 