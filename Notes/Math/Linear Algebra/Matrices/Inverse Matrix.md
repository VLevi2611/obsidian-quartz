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
-1 & \frac{3}{2} & 1 & 0 \\
 1 & -1           & 0 & 1
\end{array}
\right)

$$
Manipulate the left side of the matrix to be the [[Identity Matrix]].
Call the first row of the matrix $R_1$ and the second row $R_2$.
Add the first row to the second row to make the first component in $R_2$ 0. $R_1+R_2 \rightarrow R_2$
$$\left(
\begin{array}{cc|cc}
-1 & \frac{3}{2} & 1 & 0 \\
 0 & \frac{1}{2} & 1 & 1
\end{array}
\right)
$$
Multiply the first row by -1 and the second by 2 to resemble the identity matrix.
$R_1*-1 \rightarrow R_1$ , $R_2 * 2 \rightarrow 