# Exercise 2. Addition and Scalar Multiplication – Solution

## 1. Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

> **Why this exercise:** reinforces entry-by-entry operations and the importance of compatible dimensions.

## 2. Theoretical Background and Concepts

- Two matrices can be **added or subtracted** only if they have the same size; the operation is done entry by entry: $(A\pm B)_{ij}=a_{ij}\pm b_{ij}$.
- **Scalar multiplication** multiplies every entry by the number: $(kA)_{ij}=k\,a_{ij}$.
- These operations behave like the corresponding operations on numbers (commutative, associative, distributive), so linear combinations such as $3A-2B$ are computed entry by entry.

## 3. Detailed Step-by-Step Solution

Both operations are performed **entry by entry**: $(A\pm B)_{ij}=a_{ij}\pm b_{ij}$ and $(kA)_{ij}=k\,a_{ij}$.

**1. Sum**

$$
A+B=\begin{pmatrix} 1+4 & 2+(-2) \\
-1+0 & 3+5 \end{pmatrix}=\begin{pmatrix} 5 & 0 \\
-1 & 8 \end{pmatrix}.
$$

**2. Difference**

$$
A-B=\begin{pmatrix} 1-4 & 2-(-2) \\
-1-0 & 3-5 \end{pmatrix}=\begin{pmatrix} -3 & 4 \\
-1 & -2 \end{pmatrix}.
$$

**3. Linear combination $3A-2B$**

$$
3A=\begin{pmatrix} 3 & 6 \\
-3 & 9 \end{pmatrix},\qquad 2B=\begin{pmatrix} 8 & -4 \\
0 & 10 \end{pmatrix},
$$

$$
3A-2B=\begin{pmatrix} 3-8 & 6+4 \\
-3-0 & 9-10 \end{pmatrix}=\begin{pmatrix} -5 & 10 \\
-3 & -1 \end{pmatrix}.
$$

**Why addition requires the same size**

Addition is defined by adding entries in the same position $(i,j)$. If $A$ and $B$ had different sizes, some positions would exist in one matrix but not in the other, so there would be no partner entry to add. Therefore $A+B$ is defined only when both matrices are $m\times n$, and the result is again $m\times n$.

## 4. Verification and Consistency Checks

$$
(A+B)+(A-B)=\begin{pmatrix} 2 & 4 \\
-2 & 6 \end{pmatrix}=2A\ ✓
$$

and $3A-2B=(A+B)+2A-3B$ can be checked entrywise, e.g. entry $(1,2)$: $3\cdot2-2\cdot(-2)=10$ ✓.
