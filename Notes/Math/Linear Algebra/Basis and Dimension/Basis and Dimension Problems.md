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

$$\mathbf{A} = \begin{pmatrix}
1 & 0 & 2 \\
2 & 1 & 1 \\
0 & 3 & 1
\end{pmatrix}$$
#### Solution

A span of a matrix is the collection of the [[Column Vector]]s with a [[Linear Combination]].
$$\begin{array}{l}
Span(\mathbf{A}) = c_1 \begin{pmatrix}
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
Span(\mathbf{A}) = \begin{pmatrix}
c_1 + 2c_3 \\
2c_1 + c_2 + c_3 \\
3c_2 + c_1
\end{pmatrix}
\end{array}$$

## [[Linear Dependence]]

### Question 1

Check if the matrix $\mathbf{A}$ has linear dependent [[Vector]]s

#### Given

$$\mathbf{A} = \begin{pmatrix}
1 & 2 & 2 \\
2 & -1 & 0 \\
1 & 1 & 1
\end{pmatrix}$$
#### Solution