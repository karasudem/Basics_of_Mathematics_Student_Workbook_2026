# Exercise 3. When Can Matrices Be Multiplied? – Solution

## 1. Problem Statement

The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

> **Why this exercise:** forces an understanding of dimension compatibility before carrying out any calculation.

## 2. Theoretical Background and Concepts

- The product $XY$ of an $m\times n$ matrix $X$ and a $p\times q$ matrix $Y$ is **defined only when $n=p$** (number of columns of $X$ = number of rows of $Y$).
- The result $XY$ has size $m\times q$ (outer dimensions).
- Entry $(i,j)$ of $XY$ is the dot product of row $i$ of $X$ and column $j$ of $Y$, which requires both to have the same length.

## 3. Detailed Step-by-Step Solution

**Rule:** the product $X_{m\times n}\,Y_{p\times q}$ is defined only when $n=p$ (columns of the left factor = rows of the right factor). The result then has size $m\times q$.

| Product | Sizes | Inner dimensions | Defined? | Result size |
|---|---|---|---|---|
| $AB$ | $(2\times3)(3\times4)$ | $3=3$ | yes | $2\times4$ |
| $BA$ | $(3\times4)(2\times3)$ | $4\neq2$ | no | – |
| $BC$ | $(3\times4)(4\times2)$ | $4=4$ | yes | $3\times2$ |
| $CB$ | $(4\times2)(3\times4)$ | $2\neq3$ | no | – |
| $AC$ | $(2\times3)(4\times2)$ | $3\neq4$ | no | – |
| $CA$ | $(4\times2)(2\times3)$ | $2=2$ | yes | $4\times3$ |
| $AD$ | $(2\times3)(2\times2)$ | $3\neq2$ | no | – |
| $DA$ | $(2\times2)(2\times3)$ | $2=2$ | yes | $2\times3$ |

**Justification**

Each entry of $XY$ is the dot product of a row of $X$ with a column of $Y$. A row of $X$ has $n$ entries and a column of $Y$ has $p$ entries, so the dot product only makes sense when $n=p$.

**Observation:** $AB$ is defined but $BA$ is not – so the order of factors matters even before any computation is done.

## 4. Verification and Consistency Checks

- **Size check by the "outer dimensions" rule:** for each defined product the size of the result is (rows of the left factor) $\times$ (columns of the right factor), e.g. $(2\times\underline{3})(\underline{3}\times4)\to2\times4$ ✓.
- **Consistency:** $AB$ ($2\times4$) can be followed by $C$ ($4\times2$), so $(AB)C$ is defined with size $2\times2$; the same size comes out of $A(BC)=(2\times3)(3\times2)$ ✓. Likewise $DA$ ($2\times3$) has the same size as $A$, as expected when multiplying by a square matrix from the left.

