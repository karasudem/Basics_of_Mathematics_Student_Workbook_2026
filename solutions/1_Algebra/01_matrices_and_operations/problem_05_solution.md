# Exercise 5. Matrix Times Vector – Solution

## 1. Problem Statement

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

> **Why this exercise:** shows that multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

## 2. Theoretical Background and Concepts

- For an $m\times n$ matrix $A$ and a vector $x\in\mathbb{R}^n$, the product $Ax$ is a vector in $\mathbb{R}^m$.
- **Row view:** the $i$-th entry of $Ax$ is (row $i$ of $A$) $\cdot\, x$.
- **Column view:** $Ax=x_1a_1+x_2a_2+\dots+x_na_n$, a linear combination of the columns $a_j$ of $A$ with coefficients from $x$.

## 3. Detailed Step-by-Step Solution

**1. Computing $Ax$ (row by row)**

$$
Ax=\begin{pmatrix} 2\cdot4+(-1)\cdot2 \\
1\cdot4+3\cdot2 \end{pmatrix}=\begin{pmatrix} 6 \\
10 \end{pmatrix}.
$$

**2. $Ax$ as a linear combination of columns**

The columns of $A$ are

$$
a_1=\begin{pmatrix} 2 \\
1 \end{pmatrix},\qquad a_2=\begin{pmatrix} -1 \\
3 \end{pmatrix},
$$

and the coefficients are the entries of $x$: $x_1=4$, $x_2=2$.

$$
Ax=4\begin{pmatrix} 2 \\
1 \end{pmatrix}+2\begin{pmatrix} -1 \\
3 \end{pmatrix}=\begin{pmatrix} 8 \\
4 \end{pmatrix}+\begin{pmatrix} -2 \\
6 \end{pmatrix}=\begin{pmatrix} 6 \\
10 \end{pmatrix}.
$$

**Explanation**

In general, for $A=(a_1\ a_2\ \cdots\ a_n)$ and $x=(x_1,\dots,x_n)^T$:

$$
Ax=x_1a_1+x_2a_2+\dots+x_na_n.
$$

So $Ax$ always lies in the span of the columns of $A$, and $x$ tells us "how much" of each column to take. The row-by-row method and the column method are two views of the same calculation.

## 4. Verification and Consistency Checks

Both methods give the same vector $(6,\,10)^T$ ✓.
