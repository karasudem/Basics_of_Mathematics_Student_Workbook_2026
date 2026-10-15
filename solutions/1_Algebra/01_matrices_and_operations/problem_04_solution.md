### Exercise 4. Matrix Multiplication and Noncommutativity
For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

> **Why this exercise:** shows one of the most important differences between matrix multiplication and multiplication of numbers.

### Solution – Exercise 4. Matrix Multiplication and Noncommutativity

Entry $(i,j)$ of a product = (row $i$ of the left matrix) $\cdot$ (column $j$ of the right matrix).

**1. Product $AB$**

$$
AB=\begin{pmatrix} 1\cdot2+2\cdot3 & 1\cdot0+2\cdot1 \\ 0\cdot2+1\cdot3 & 0\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}.
$$

**2. Product $BA$**

$$
BA=\begin{pmatrix} 2\cdot1+0\cdot0 & 2\cdot2+0\cdot1 \\ 3\cdot1+1\cdot0 & 3\cdot2+1\cdot1 \end{pmatrix}=\begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}.
$$

**3. Comparison**

$$
AB=\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}\neq\begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}=BA.
$$

**Verification**

The traces agree, $\operatorname{tr}(AB)=9=\operatorname{tr}(BA)$, and the determinants agree, $\det(AB)=8-6=2=14-12=\det(BA)$, as they must (since $\operatorname{tr}(XY)=\operatorname{tr}(YX)$ and $\det(XY)=\det X\det Y$). Yet the matrices themselves differ.

**What noncommutativity means**

For real numbers $ab=ba$ always. For matrices this is **not** true in general: even when both $AB$ and $BA$ are defined and have the same size, they can be different. In $AB$ we combine rows of $A$ with columns of $B$, while in $BA$ we combine rows of $B$ with columns of $A$ – these are different computations. Geometrically, $AB$ means "apply $B$ first, then $A$", and changing the order of two transformations usually changes the result.
