# 10-22-26

# Class XIV: Midterm Review

A set $X$ and a function

$
d:X\times X\to\mathbb{R}
$

is called a **metric space** if:

1. $d(x,y)\geq 0$, with $d(x,y)=0$ iff $x=y$.
2. $d(x,y)=d(y,x)$.
3. $d(x,z)\leq d(x,y)+d(y,z)$. ⭐ **Triangle Inequality**

## Examples

(i) $\mathbb{R}^n$ with Euclidean metric

$
d\big((x_1,\ldots,x_n),(y_1,\ldots,y_n)\big)
=
\sum_{i=1}^{n}\sqrt{(x_i-y_i)^2}
$

For $n=1$:

$
|x-y|.
$

(ii) Discrete metric

$$
d_d(x,y)=
\begin{cases}
0, & x=y,\\
1, & x\neq y.
\end{cases}
$$

## Open and Closed Sets

**Definition.** $A\subseteq X$ is **open** if every $x\in A$ is an interior point of $A$.

Example:

$$
(a,b)\in\mathbb{R}.
$$

**Definition.** $A\subseteq X$ is **closed** if every limit point of $A$ is contained in $A$.

Example:

$$
[a,b]\in\mathbb{R}.
$$

**Remark.** Depends on $X$!

Sets can be both open and closed or neither.

$$
X\subseteq X
$$

is open and closed. So is $\{\emptyset\}$??

$$
(a,b]\in\mathbb{R}
$$

is not closed and not open.

⚠️ **Theorem**

$$
A\text{ is open}\iff A^c\text{ is closed}.
$$

⚠️ **Theorem**

If $A_\alpha$, $\alpha\in\mathcal A$, are open, then

$$
\bigcup_{\alpha\in\mathcal A}A_\alpha
$$

is open.

If $A_i$, $1\leq i\leq N$, are open, then

$$
\bigcap_{i=1}^{N}A_i
$$

is open.

## Compactness

**Definition.**

(i) $A\subseteq X$ is **compact** if every open cover has a finite subcover.

(ii) $A\subseteq X$ is **limit point compact** if every infinite set $E\subseteq A$ has a limit point in $E$; often

$$
E=\{x_n\mid n\in\mathbb N\}.
$$

(iii) $A\subseteq X$ is **sequentially compact** if every sequence

$$
\{x_n\}_{n\in\mathbb N}
$$

in $A$ has a convergent subspace.

⚠️ **Theorem**

(i), (ii), and (iii) are equivalent.

- (i) $\Rightarrow A\subseteq X$ is closed and bounded. If $X\in\mathbb{R}^n$, the reverse implication also holds. ⭐ **Heine–Borel Theorem**
- If $B\subseteq A$, $A$ is compact, and $B$ is closed, then $B$ is compact.

## Bolzano–Weierstrass Theorem

If

$$
\{x_n\}_{n\in\mathbb N}
$$

is a bounded sequence in $\mathbb{R}^n$, then

$$
\{x_n\}_{n\in\mathbb N}
$$

has a convergent subsequence.

## Sequences

**Definition.**

$$
\lim_{n\to\infty}x_n=x
$$

iff

$$
\forall\epsilon>0,\ \exists N\in\mathbb N,\ \forall n\geq N,
\qquad
d(x_n,x)<\epsilon.
$$

A sequence $\{x_n\}_{n\in\mathbb N}$ is **Cauchy** iff

$$
\forall\epsilon>0,\ \exists N\in\mathbb N,\ \forall n,m\geq N,
\qquad
d(x_n,x_m)<\epsilon.
$$

⚠️ **Theorem**

$$
\text{Convergent}\Rightarrow\text{Cauchy}\Rightarrow\text{bounded}.
$$

*(supremum exists)*

⚠️ **Theorem**

If $\{x_n\}_{n\in\mathbb N}$ is a sequence in $\mathbb{R}$ that is monotonically increasing and bounded, then it converges.

**Definition.** $X$ is called **complete** if all Cauchy sequences converge.
