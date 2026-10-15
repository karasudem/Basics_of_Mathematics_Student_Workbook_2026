# Exercise 8. Row Operations and Their Reversibility – Solution

## 1. Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

> **Why this exercise:** prepares for elimination by showing that row operations are controlled and reversible transformations of a matrix.

## 2. Theoretical Background and Concepts

- **Elementary row operations:** (1) adding a multiple of one row to another, (2) swapping two rows, (3) multiplying a row by a non-zero number.
- Every elementary row operation is **reversible**, and its inverse is again an elementary row operation of the same type.
- Row operations are the basis of **Gaussian elimination**, whose goal is an upper triangular (row echelon) form.

## 3. Detailed Step-by-Step Solution

Starting matrix:

$$
A=\begin{pmatrix} 1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \end{pmatrix}.
$$

**Step 1: $R_2\leftarrow R_2-2R_1$**

$R_2-2R_1=(2,4,1)-(2,4,-2)=(0,0,3)$:

$$
A_1=\begin{pmatrix} 1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \end{pmatrix}.
$$

**Step 2: $R_3\leftarrow R_3+R_1$**

$R_3+R_1=(-1,1,3)+(1,2,-1)=(0,3,2)$:

$$
A_2=\begin{pmatrix} 1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \end{pmatrix}.
$$

**Step 3: $R_2\leftrightarrow R_3$**

$$
A_3=\begin{pmatrix} 1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \end{pmatrix}.
$$

The result is upper triangular (row echelon form) – this is exactly the goal of Gaussian elimination.

**Reverse operations**

| Operation | Reverse operation |
|---|---|
| $R_2\leftarrow R_2-2R_1$ | $R_2\leftarrow R_2+2R_1$ |
| $R_3\leftarrow R_3+R_1$ | $R_3\leftarrow R_3-R_1$ |
| $R_2\leftrightarrow R_3$ | $R_2\leftrightarrow R_3$ (a swap is its own inverse) |

To return from $A_3$ to $A$, the reverse operations are applied in **reverse order**: first swap $R_2,R_3$, then $R_3\leftarrow R_3-R_1$, then $R_2\leftarrow R_2+2R_1$.

**Explanation:** each elementary row operation can be undone, so it does not lose information (it corresponds to multiplying by an invertible elementary matrix). Row $R_1$ is never changed in steps 1–2, which is why we can use it to undo them.

## 4. Verification and Consistency Checks

From $A_3$: swap → $A_2$; $R_3-R_1=(0,3,2)-(1,2,-1)=(-1,1,3)$ → $A_1$; $R_2+2R_1=(0,0,3)+(2,4,-2)=(2,4,1)$ → $A$ ✓.
