---
tags:
  - problem
  - easy
  - medium
  - hard
  - exam-level
---
## [[Span]]

### Question 1

What is the span of [[Matrix]] $\mathbf{A}$ 

#### Given

$$
\mathbf{A} = \begin{pmatrix}
1 & 0 & 2 \\
2 & 1 & 1 \\
0 & 3 & 1
\end{pmatrix}
$$
#### Solution

A span of a matrix is the collection of the [[Column Vector]]s with a [[Linear Combination]].
$$
\begin{aligned}
Span(\mathbf{A}) &= c_1 \begin{pmatrix}
1 \\
2 \\
0
\end{pmatrix} + c_2 \begin{pmatrix}
0 \\
1 \\
3 
\end{pmatrix} + c_3 \begin{pmatrix}
2 \\
1 \\
1
\end{pmatrix} \\
Span(\mathbf{A}) &= \begin{pmatrix}
c_1 + 2c_3 \\
2c_1 + c_2 + c_3 \\
3c_2 + c_1
\end{pmatrix}
\end{aligned}
$$

## [[Linear Dependence]]

### Question 1

Check if the matrix $\mathbf{A}$ has linear dependent [[Vector|Vectors]]

#### Given

$$
\mathbf{A} = \begin{pmatrix}
1 & 2 & 2 \\
2 & -1 & 0 \\
1 & 1 & 1
\end{pmatrix}
$$
#### Solution

Preform gaussian elimination
$$
\begin{aligned}
\begin{pmatrix}
1 & 2 & 2 \\
2 & -1 & 0 \\
1 & 1 & 1
\end{pmatrix} &\rightarrow
\begin{pmatrix}
1 & 2 & 2 \\
0 & -5 & -4 \\
0 & -1 & -1
\end{pmatrix} \\
\begin{pmatrix}
1 & 2 & 2 \\
0 & -5 & -4 \\
0 & -1 & -1
\end{pmatrix} &\rightarrow 
\begin{pmatrix}
1 & 2 & 2 \\
0 & -1 & -1 \\
0 & -5 & -4
\end{pmatrix} \\
\begin{pmatrix}
1 & 2 & 2 \\
0 & -1 & -1 \\
0 & -5 & -4
\end{pmatrix} &\rightarrow
\begin{pmatrix}
1 & 2 & 2 \\
0 & -1 & -1 \\
0 & 0 & 1
\end{pmatrix}
\end{aligned}
$$
No 2 [[Row Vector|Row Vectors]] are the same so the matrix $\mathbf{A}$ has [[Linear Independence]].

## [[Basis]] 

### Question 1

What is the basis of matrix $\mathbf{A}$

#### Given

$$
\mathbf{A} = \left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
2 & 0 & 0 & 1 & 0 \\
1 & 2 & 2 & 1 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right)
$$
#### Solution

Solve the matrix to row reduced form
$$
\begin{aligned}
\mathbf{A} = \left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
2 & 0 & 0 & 1 & 0 \\
1 & 2 & 2 & 1 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right) &\rightarrow 
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & -2 & -6 & -1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right) \\
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & -2 & -6 & -1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right) &\rightarrow
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & -2 & -6 & -1 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right) \\
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & -2 & -6 & -1 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right) &\rightarrow
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & -8 & -1 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right) \\
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & -8 & -1 & 0 \\
0 & 0 & 1 & 2 & 0
\end{array}
\right) &\rightarrow
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & 1 & 2 & 0 \\
0 & 0 & -8 & -1 & 0
\end{array}
\right) \\
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & 1 & 2 & 0 \\
0 & 0 & -8 & -1 & 0
\end{array}
\right) &\rightarrow
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & 1 & 2 & 0 \\
0 & 0 & 0 & 15 & 0
\end{array}
\right) \\
\left(
\begin{array}{cccc|c}
1 & 1 & 3 & 1 & 0 \\
0 & 1 & -1 & 0 & 0 \\
0 & 0 & 1 & 2 & 0 \\
0 & 0 & 0 & 15 & 0
\end{array}
\right) &\rightarrow 
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 0
\end{array}
\right)
\end{aligned}
$$

After some long algebra, we get the [[Identity Matrix]] $\mathbf{I}_4$, and the basis is 
$$
Col(\mathbf{A})=\mathbb{R}^4
$$
And the [[Dimension]] 
$$
\dim(\mathbf{A})=4
$$