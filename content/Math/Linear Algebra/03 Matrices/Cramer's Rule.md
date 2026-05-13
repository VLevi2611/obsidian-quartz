---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

**Cramer's rule** is a formula for the solution of a [[Linear System Of Equations]] with as many variables as unknowns.

In the general case, a system of $n$ linear equations for $n$ unknowns, represented in [[Matrix Multiplication]] form:
$$
\mathbf{A} \vec x = \mathbf{b}
$$
where the $n$x$n$ [[Matrix]] $A$ has a non 0 [[Determinant]].
$$
x_i=\frac{\det \mathbf{A}_i}{\det \mathbf{A}}
$$
where $\mathbf{A}_i$ is the matrix formed by replacing the $i$ column of $\mathbf{A}$ with the [[Vector]] $\mathbf{b}$.