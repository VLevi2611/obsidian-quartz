---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

Cramer's rule is a formula for the solution of a [[Linear System Of Equations]] with as many variables as unknowns.

In the general case, a system of $n$ linear equations for $n$ unknowns, represented in [[Matrix Multiplication]] form:
$$Ax=b$$
where the $n$x$n$ [[Matrix]] $A$ has a non 0 [[Determinant]].
$$x_i=\frac{\det A_i}{\det A}$$
where $A_i$ is the matrix formed by replacing the $i$ column of $A$ with the [[Vector]] $b$.