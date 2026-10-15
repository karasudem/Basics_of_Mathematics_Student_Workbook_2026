# Exercise 7. Identity Matrix, Zero Matrix, and Powers – Solution

## 1. Problem Statement

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

> **Why this exercise:** organizes the roles of neutral elements and reveals regularity in successive powers of a matrix.

## 2. Theoretical Background and Concepts

- The **identity matrix** $I$ has ones on the diagonal and zeros elsewhere; it is the neutral element of multiplication: $AI=IA=A$.
- The **zero matrix** $0$ has all entries equal to $0$; it is the neutral element of addition: $A+0=A$.
- **Powers** of a square matrix are defined by repeated multiplication: $A^2=AA$, $A^3=A^2A$, … A general formula for $A^n$ can be proved by induction.

## 3. Detailed Step-by-Step Solution

Here

$$
I=\begin{pmatrix} 1 & 0 \\
0 & 1 \end{pmatrix},\qquad 0=\begin{pmatrix} 0 & 0 \\
0 & 0 \end{pmatrix}.
$$

**1. Neutral elements**

$$
AI=\begin{pmatrix} 2\cdot1+1\cdot0 & 2\cdot0+1\cdot1 \\
0\cdot1+2\cdot0 & 0\cdot0+2\cdot1 \end{pmatrix}=\begin{pmatrix} 2 & 1 \\
0 & 2 \end{pmatrix}=A,\qquad IA=A,\qquad A+0=A.
$$

- $I$ is the neutral element of **multiplication** (like the number 1): $AI=IA=A$.
- $0$ is the neutral element of **addition** (like the number 0): $A+0=A$.

**2. Powers**

$$
A^2=\begin{pmatrix} 2 & 1 \\
0 & 2 \end{pmatrix}\begin{pmatrix} 2 & 1 \\
0 & 2 \end{pmatrix}=\begin{pmatrix} 4 & 4 \\
0 & 4 \end{pmatrix},
$$

$$
A^3=A^2A=\begin{pmatrix} 4 & 4 \\
0 & 4 \end{pmatrix}\begin{pmatrix} 2 & 1 \\
0 & 2 \end{pmatrix}=\begin{pmatrix} 8 & 12 \\
0 & 8 \end{pmatrix}.
$$

**3. Pattern**

- The diagonal entries are $2,4,8$, i.e. $2^n$.
- The lower-left entry stays $0$ (upper triangular matrices stay upper triangular).
- The upper-right entry is $1,4,12$, i.e. $n\cdot2^{n-1}$.

Conjecture:

$$
A^n=\begin{pmatrix} 2^n & n\,2^{n-1} \\
0 & 2^n \end{pmatrix}.
$$

## 4. Verification and Consistency Checks

$n=1$: gives $A$ itself ✓; $n=2$: $(4,4)$ ✓; $n=3$: $(8,12)$ ✓. Moreover, if the formula holds for $n$, then

$$
A^{n+1}=A^nA=\begin{pmatrix} 2^{n+1} & 2^n+2\cdot n2^{n-1} \\
0 & 2^{n+1} \end{pmatrix}=\begin{pmatrix} 2^{n+1} & (n+1)2^{n} \\
0 & 2^{n+1} \end{pmatrix},
$$

so the pattern continues for all $n$. (Reason: $A=2I+N$, where $N$ has a single $1$ in the upper-right corner and $N^2=0$.)
