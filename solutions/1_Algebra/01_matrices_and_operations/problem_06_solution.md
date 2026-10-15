# Exercise 6. Transpose – Solution

## 1. Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

> **Why this exercise:** teaches transposition and an important property that reverses the order of factors.

## 2. Theoretical Background and Concepts

- The **transpose** $A^T$ is obtained by swapping rows and columns: $(A^T)_{ij}=a_{ji}$; an $m\times n$ matrix becomes $n\times m$.
- Properties: $(A^T)^T=A$, $(A+B)^T=A^T+B^T$ and $(AB)^T=B^TA^T$ (the **order of factors is reversed**).

## 3. Detailed Step-by-Step Solution

The transpose swaps rows and columns: $(A^T)_{ij}=a_{ji}$. An $m\times n$ matrix becomes $n\times m$.

**1. Transposes**

$$
A^T=\begin{pmatrix} 1 & 4 \\
2 & 5 \\
3 & 6 \end{pmatrix}\ (3\times2),\qquad B^T=\begin{pmatrix} 1 & 2 & -1 \\
0 & 1 & 3 \end{pmatrix}\ (2\times3).
$$

**2. Product $AB$** ($2\times3$ times $3\times2$ gives $2\times2$)

$$
AB=\begin{pmatrix} 1\cdot1+2\cdot2+3\cdot(-1) & 1\cdot0+2\cdot1+3\cdot3 \\
4\cdot1+5\cdot2+6\cdot(-1) & 4\cdot0+5\cdot1+6\cdot3 \end{pmatrix}=\begin{pmatrix} 2 & 11 \\
8 & 23 \end{pmatrix}.
$$

**3. Verification of $(AB)^T=B^TA^T$**

Left side:

$$
(AB)^T=\begin{pmatrix} 2 & 8 \\
11 & 23 \end{pmatrix}.
$$

Right side ($2\times3$ times $3\times2$):

$$
B^TA^T=\begin{pmatrix} 1\cdot1+2\cdot2+(-1)\cdot3 & 1\cdot4+2\cdot5+(-1)\cdot6 \\
0\cdot1+1\cdot2+3\cdot3 & 0\cdot4+1\cdot5+3\cdot6 \end{pmatrix}=\begin{pmatrix} 2 & 8 \\
11 & 23 \end{pmatrix}.
$$

Both sides are equal ✓.

**Explanation**

Entry $(i,j)$ of $(AB)^T$ is entry $(j,i)$ of $AB$, i.e. row $j$ of $A$ times column $i$ of $B$. That is the same as row $i$ of $B^T$ times column $j$ of $A^T$ – which is entry $(i,j)$ of $B^TA^T$. The order of the factors must be reversed; note that $A^TB^T$ would even be a $3\times3$ matrix, so it cannot be equal to $(AB)^T$.

## 4. Verification and Consistency Checks

- **Size check:** $A$ is $2\times3$, $B$ is $3\times2$, so $AB$ is $2\times2$; $B^T$ is $2\times3$, $A^T$ is $3\times2$, so $B^TA^T$ is $2\times2$ ✓.
- **Entry check:** entry $(1,2)$ of $(AB)^T$ equals entry $(2,1)$ of $AB$, i.e. $8$, and entry $(1,2)$ of $B^TA^T$ is $1\cdot4+2\cdot5+(-1)\cdot6=8$ ✓.
