# Exercise 9. Composing Transformations – Solution

## 1. Problem Statement

Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

> **Why this exercise:** interprets matrix multiplication as composition of transformations.

## 2. Theoretical Background and Concepts

- A $2\times2$ matrix describes a **linear transformation** of the plane: $x\mapsto Mx$.
- $S=\operatorname{diag}(2,1)$ is a **non-uniform scaling** (stretches the horizontal direction by 2); $R$ is the **rotation by $90^\circ$** counterclockwise: $(x,y)\mapsto(-y,x)$.
- The product $RS$ represents the **composition** "first $S$, then $R$": $(RS)x=R(Sx)$. Since matrix multiplication is not commutative, the order of transformations matters.

## 3. Detailed Step-by-Step Solution

In a product the transformation written **closest to $x$ acts first**: $RSx=R(Sx)$ means "first $S$, then $R$".

**1. $RSx$ (scale first, then rotate)**

$$
Sx=\begin{pmatrix} 2\cdot1 \\
1\cdot2 \end{pmatrix}=\begin{pmatrix} 2 \\
2 \end{pmatrix},\qquad RSx=R\begin{pmatrix} 2 \\
2 \end{pmatrix}=\begin{pmatrix} 0\cdot2-1\cdot2 \\
1\cdot2+0\cdot2 \end{pmatrix}=\begin{pmatrix} -2 \\
2 \end{pmatrix}.
$$

**2. $SRx$ (rotate first, then scale)**

$$
Rx=\begin{pmatrix} -2 \\
1 \end{pmatrix},\qquad SRx=S\begin{pmatrix} -2 \\
1 \end{pmatrix}=\begin{pmatrix} -4 \\
1 \end{pmatrix}.
$$

**3. Comparison**

$$
RSx=\begin{pmatrix} -2 \\
2 \end{pmatrix}\neq\begin{pmatrix} -4 \\
1 \end{pmatrix}=SRx.
$$

**Geometric explanation**

$S$ stretches only the **horizontal** direction by a factor of 2. 

- In $RSx$ we stretch first: the $x$-component $1$ becomes $2$, and then the whole picture is rotated by $90^\circ$.
- In $SRx$ we rotate first: the vector becomes $(-2,1)$, so its original *vertical* part now lies horizontally, and it is this part that gets doubled to $-4$.

So the stretching acts on different parts of the vector depending on the order. A rotation and a non-uniform scaling do not commute, which is the geometric meaning of $RS\neq SR$.

## 4. Verification and Consistency Checks

**Check with the product matrices**

$$
RS=\begin{pmatrix} 0 & -1 \\
2 & 0 \end{pmatrix},\quad RS\,x=\begin{pmatrix} -2 \\
2 \end{pmatrix}\ ✓;\qquad SR=\begin{pmatrix} 0 & -2 \\
1 & 0 \end{pmatrix},\quad SR\,x=\begin{pmatrix} -4 \\
1 \end{pmatrix}\ ✓.
$$
