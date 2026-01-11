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
\begin{pmatrix}
c_1 + 2c_3 \\

\end{pmatrix}
\end{array}$$