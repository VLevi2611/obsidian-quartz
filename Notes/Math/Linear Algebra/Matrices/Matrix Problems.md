---
tags:
  - problem
  - easy
  - medium
  - hard
  - exam-level
---
## [[Matrix Vector Multiplication]]

### Question 1

Whats the product of $\mathbf{Ax}$
#### Given

$$\begin{array}{l}
\mathbf{A} = \begin{pmatrix}
1 & 3 & 2 \\
2 & 2 & 1 \\
0 & 2 & 4
\end{pmatrix} \\
\mathbf{x} = (1,0,1)^T
\end{array}$$
#### Solution

To multiply a [[Matrix]] and a [[Vector]], do a [[Dot Product]] for each row with the vector
$$\mathbf{Ax}=\begin{pmatrix}
1 \times 1 + 3 \times 0 + 2 \times 1 \\
2 \times 1 + 2 \times 0 + 1 \times 1 \\
0 \times 1 + 2 \times 0 + 4 \times 1
\end{pmatrix}=
\begin{pmatrix}
3 \\
3 \\
4
\end{pmatrix}$$

## [[Matrix Multiplication]]

### Question 1

Whats the product of $\mathbf{AB}$

#### Given

$$\begin{array}{l}
\mathbf{A} = \begin{pmatrix}
1 & 3 \\
2 & 1
\end{pmatrix} \\
\mathbf{B} = \begin{pmatrix}
2 & 2 \\
0 & 1
\end{pmatrix}
\end{array}$$
#### Solution

To multiply 2 matrix, multiply $\mathbf{