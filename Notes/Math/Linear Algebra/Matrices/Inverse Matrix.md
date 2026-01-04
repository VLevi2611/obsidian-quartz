---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

The inverse of a [[Matrix]] $A^{-1}$ exists only when the [[Determinant]] is not 0. The inverse reverses the [[Linear Transformation]] of the matrix.
There are several ways to compute the inverse:
### Gaussian elimination
$$A=\begin{pmatrix}
-1 & \frac{3}{2} \\
1 & -1
\end{pmatrix}$$
Create the augmented matrix:
$$\left(
\begin{array}{cc|cc}
-1 & \tfrac{3}{2} & 1 & 0 \\
 1 & -1           & 0 & 1
\end{array}
\right)

$$