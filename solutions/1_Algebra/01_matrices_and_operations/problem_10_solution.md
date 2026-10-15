### Exercise 10. Columns of a Matrix Product
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

> **Why this exercise:** extends the interpretation of matrix-vector multiplication to a full product of two matrices instead of simply repeating another $Ax$ exercise.

### Solution – Exercise 10. Columns of a Matrix Product

The columns of $B$ are

$$
b_1=\begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix},\qquad b_2=\begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}.
$$

**1. Matrix-vector products**

$$
Ab_1=\begin{pmatrix} 1\cdot1+2\cdot(-1)+0\cdot3 \\ 0\cdot1+1\cdot(-1)+1\cdot3 \end{pmatrix}=\begin{pmatrix} -1 \\ 2 \end{pmatrix},
\qquad
Ab_2=\begin{pmatrix} 1\cdot2+2\cdot0+0\cdot1 \\ 0\cdot2+1\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} 2 \\ 1 \end{pmatrix}.
$$

**2. Full product $AB$** ($2\times3$ times $3\times2$ gives $2\times2$)

$$
AB=\begin{pmatrix} 1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1 \\ 0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}.
$$

**3. Comparison and explanation**

The first column of $AB$ is $\begin{pmatrix} -1 \\ 2 \end{pmatrix}=Ab_1$ and the second column is $\begin{pmatrix} 2 \\ 1 \end{pmatrix}=Ab_2$ ✓. Hence

$$
AB=A\,(b_1\ \ b_2)=(Ab_1\ \ Ab_2).
$$

Why: entry $(i,j)$ of $AB$ is (row $i$ of $A$) $\cdot$ (column $j$ of $B$). For a fixed $j$, these numbers for $i=1,2$ are exactly the entries of $Ab_j$. So column $j$ of $AB$ only depends on column $j$ of $B$, and it equals $Ab_j$.

Combined with Exercise 5, each column of $AB$ is a linear combination of the columns of $A$, e.g.

$$
Ab_1=1\begin{pmatrix} 1 \\ 0 \end{pmatrix}-1\begin{pmatrix} 2 \\ 1 \end{pmatrix}+3\begin{pmatrix} 0 \\ 1 \end{pmatrix}=\begin{pmatrix} -1 \\ 2 \end{pmatrix}\ ✓.
$$
