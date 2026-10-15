### Exercise 3. When Can Matrices Be Multiplied?
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

### Solution – Exercise 3. When Can Matrices Be Multiplied?

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
