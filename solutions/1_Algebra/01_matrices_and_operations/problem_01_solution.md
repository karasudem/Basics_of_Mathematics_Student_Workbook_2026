# Exercise 1. Matrix Size and Entries – Solution

## 1. Problem Statement

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

> **Why this exercise:** builds basic fluency with matrix notation, indices, rows, and columns.

## 2. Theoretical Background and Concepts

- A **matrix** of size $m\times n$ is a rectangular array of numbers with $m$ rows and $n$ columns.
- The entry in row $i$ and column $j$ is denoted $a_{ij}$: the **first index is the row**, the **second index is the column**.
- A single row of a matrix is a **row vector** ($1\times n$), and a single column is a **column vector** ($m\times1$).

## 3. Detailed Step-by-Step Solution

**1. Matrix sizes**

The size of a matrix is written as (number of rows) $\times$ (number of columns).

- Matrix $A$ has 2 rows and 3 columns, so its size is $2\times3$.
- Matrix $B$ has 3 rows and 2 columns, so its size is $3\times2$.

**2. Reading entries**

The entry $a_{ij}$ lies in row $i$ and column $j$.

$$
a_{12}=-1,\qquad a_{23}=5,\qquad b_{21}=-2,\qquad b_{32}=1.
$$

- $a_{12}$: row 1 of $A$ is $(2,-1,3)$, column 2 gives $-1$.
- $a_{23}$: row 2 of $A$ is $(0,4,5)$, column 3 gives $5$.
- $b_{21}$: row 2 of $B$ is $(-2,3)$, column 1 gives $-2$.
- $b_{32}$: row 3 of $B$ is $(4,1)$, column 2 gives $1$.

**3. Row and column vectors**

The second row of $A$ is

$$
\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}.
$$

The first column of $B$ is

$$
\begin{pmatrix} 1 \\
-2 \\
4 \end{pmatrix}.
$$

**Method used:** index notation $a_{ij}$ (first index = row, second index = column).

## 4. Verification and Consistency Checks

The row vector has 3 entries (= number of columns of $A$), and the column vector has 3 entries (= number of rows of $B$), which agrees with the sizes found in part 1.
