---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

A **change of basis** is the [[Linear Transformation]] that converts the [[Coordinates]] of a [[Vector]] from one [[Basis]] to another. The vector remains unchanged, only its [[Coordinates]] depend on the chosen basis.

Let $\mathbf{B=b_1,b_2,...,b}_n$ be a basis for $\mathbb{R}^n$.
Any vector $\mathbf{v} \in \mathbb{R}^n$ can be written as a [[Linear Combination]]:
$$
\mathbf{v}=c_1\mathbf{v}_1+c_2\mathbf{v}_2+...+c_n\mathbf{v}_n
$$
The coordinate vector of $\mathbf{v}$ in basis $\mathbf{B}$ is:
$$
\begin{bmatrix}
\mathbf{v}
\end{bmatrix}_\mathbf{B}=
\begin{bmatrix}
c_1 \\ c_2 \\ ... \\ c_n
\end{bmatrix}
$$
Let $\mathbf{P_B}$ be a matrix whose columns are the vectors of $\mathbf{B}$ written in the standard basis.
$$
\begin{aligned}
\mathbf{v} &= \mathbf{P_B}\begin{bmatrix}\mathbf{v}\end{bmatrix}_\mathbf{B} \\
\begin{bmatrix}\mathbf{v}\end{bmatrix}_\mathbf{B} &= \mathbf{P_B}^{-1}\mathbf{v}
\end{aligned}
$$
Let $\mathbf{C}$ be a basis for $\mathbb{R}^n$. To convert coordinates from $\mathbf{B}$ to $\mathbf{C}$:
$$
\begin{aligned}
\begin{bmatrix}
\mathbf{v}
\end{bmatrix} _\mathbf{C} &=
\mathbf{P_C}^{-1} \mathbf{v} \\
\begin{bmatrix}
\mathbf{v}
\end{bmatrix} _\mathbf{C}=
\mathbf{P_C}^{-1} \mathbf{P_B[v]} \\
\mathbf{P_{C \leftarrow B}} = \mathbf{P_C}^{-1} \mathbf{P_B}
\end{aligned}
$$
$\mathbf{P_{C \leftarrow B}}$ is the change of basis [[Matrix]].

## Properties

- Change of basis matrices are invertible. (have inverse)
- The [[Inverse Matrix]] corresponds to reversing the direction of change.
- Basis change is linear.
- The same vector has different coordinates in different bases.