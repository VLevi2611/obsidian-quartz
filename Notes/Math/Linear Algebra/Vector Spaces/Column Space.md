---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

A column space of a [[Matrix]] is a [[Span]] of its [[Column Vector]]s. 
The column space is also called the [[Rank]] of a matrix.
Let $K$ be a [[Field]] of [[Scalar]]s. Let $\mathbf{A}$ be an $m \times n$ matrix, with column vectors $\mathbf{v_1,v_2,...,v}_n$.
A [[Linear Combination]] of these vectors is any vector of the form
$$c_1\mathbf{v}_1+c_2\mathbf{v}_2+...+c_n\mathbf{v}_n$$ The [[Set]] of all possible linear combination is called the column space of $\mathbf{A}$.
$$\mathbf{A}
\begin{bmatrix}
c_1 \\ c_2 \\ ... \\ c_n 
\end{bmatrix}=
\begin{bmatrix}
a_{11} & ... & a_{1n} \\
... & ... & ... \\
a_{m1} & ... & a_{mn}
\end{bmatrix}
\begin{bmatrix}
c_1 \\ c_2 \\ ... \\ c_n 
\end{bmatrix}=
\begin{bmatrix}
c_1a_{11} & ... & c_na_{1n} \\
... & ... & ... \\
c_1a_{m1} & ... & c_na_{mn}
\end{bmatrix}=c_1
\begin{bmatrix}
a_{11}  \\ ... \\ a_{m1} 
\end{bmatrix}+ ...+
c_n
\begin{bmatrix}
a_{1n}  \\ ... \\ a_{mn}
\end{bmatrix}=
$$ $$=c_1\mathbf{v}_1+c_2\mathbf{v}_2+...+c_n\mathbf{v}_n$$
## Example

Given $\mathbf{A}$,
$$\mathbf{A}=\begin{bmatrix}
1 & 0 \\ 0 & 1 \\ 2 & 0 
\end{bmatrix}$$
The column vectors are $\mathbf{v_1}=\begin{bmatrix}1 & 0 & 2 \end{bmatrix}^T$ and $\mathbf{v_2}=\begin{bmatrix}0 & 1 & 0 \end{bmatrix}^T$. A linear combination of them is any vector of the form
$$c_1\begin{bmatrix}1 \\ 0 \\ 2 \end{bmatrix}+
c_2\begin{bmatrix}0 \\ 1 \\ 0 \end{bmatrix}=
$$