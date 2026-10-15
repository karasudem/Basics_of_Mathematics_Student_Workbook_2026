# Exercise 10. Columns of a Matrix Product – Solution

## 1. Problem Statement

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

## 2. Theoretical Background and Concepts

- If $B=(b_1\ b_2\ \cdots\ b_q)$ is written by columns, then $AB=(Ab_1\ \ Ab_2\ \cdots\ Ab_q)$: **each column of $AB$ is $A$ times the corresponding column of $B$**.
- Combined with the column view of $Ax$, every column of $AB$ is a linear combination of the columns of $A$.

## 3. Detailed Step-by-Step Solution

The columns of $B$ are

$$
b_1=\begin{pmatrix} 1 \\
-1 \\
3 \end{pmatrix},\qquad b_2=\begin{pmatrix} 2 \\
0 \\
1 \end{pmatrix}.
$$

**1. Matrix-vector products**

$$
Ab_1=\begin{pmatrix} 1\cdot1+2\cdot(-1)+0\cdot3 \\
0\cdot1+1\cdot(-1)+1\cdot3 \end{pmatrix}=\begin{pmatrix} -1 \\
2 \end{pmatrix},
\qquad
Ab_2=\begin{pmatrix} 1\cdot2+2\cdot0+0\cdot1 \\
0\cdot2+1\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} 2 \\
1 \end{pmatrix}.
$$

**2. Full product $AB$** ($2\times3$ times $3\times2$ gives $2\times2$)

$$
AB=\begin{pmatrix} 1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1 \\
0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} -1 & 2 \\
2 & 1 \end{pmatrix}.
$$

**3. Comparison and explanation**

The first column of $AB$ is $(-1,\,2)^T=Ab_1$ and the second column is $(2,\,1)^T=Ab_2$ ✓. Hence

$$
AB=A\,(b_1\ \ b_2)=(Ab_1\ \ Ab_2).
$$

Why: entry $(i,j)$ of $AB$ is (row $i$ of $A$) $\cdot$ (column $j$ of $B$). For a fixed $j$, these numbers for $i=1,2$ are exactly the entries of $Ab_j$. So column $j$ of $AB$ only depends on column $j$ of $B$, and it equals $Ab_j$.

Combined with Exercise 5, each column of $AB$ is a linear combination of the columns of $A$, e.g.

$$
Ab_1=1\begin{pmatrix} 1 \\
0 \end{pmatrix}-1\begin{pmatrix} 2 \\
1 \end{pmatrix}+3\begin{pmatrix} 0 \\
1 \end{pmatrix}=\begin{pmatrix} -1 \\
2 \end{pmatrix}\ ✓.
$$

## 4. Verification and Consistency Checks

- **Size check:** $A$ is $2\times3$ and $B$ is $3\times2$, so $AB$ is $2\times2$, and each $Ab_j$ is a vector in $\mathbb{R}^2$ ✓.
- **Entry check:** $(AB)_{21}=0\cdot1+1\cdot(-1)+1\cdot3=2$, the second entry of $Ab_1$ ✓; $(AB)_{12}=1\cdot2+2\cdot0+0\cdot1=2$, the first entry of $Ab_2$ ✓.
