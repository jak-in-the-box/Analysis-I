# 10-22-26

# Class XIV: Midterm Review

A set $X$ and a function $d:X\times X\to\mathbb{R}$ is called a **metric space** if:

1. $d(x,y)\geq 0$, with $d(x,y)=0$ iff $x=y$.
2. $d(x,y)=d(y,x)$.
3. $d(x,z)\leq d(x,y)+d(y,z)$. ⭐ **Triangle Inequality**

## Examples

**(i) $\mathbb{R}^n$ with Euclidean metric**

$d\big((x_1,\ldots,x_n),(y_1,\ldots,y_n)\big)=\sqrt{\sum_{i=1}^{n}(x_i-y_i)^2}$.

For $n=1$, this is $|x-y|$.

**(ii) Discrete metric**

$d_d(x,y)=0$ if $x=y$, and $d_d(x,y)=1$ if $x\neq y$.

## Open and Closed Sets

**Definition.** $A\subseteq X$ is **open** if every $x\in A$ is an interior point of $A$.

Example: $(a,b)\subseteq\mathbb{R}$.

**Definition.** $A\subseteq X$ is **closed** if every limit point of $A$ is contained in $A$.

Example: $[a,b]\subseteq\mathbb{R}$.

**Remark.** Depends on $X$!

Sets can be both open and closed or neither.

$X$ is open and closed. So is $\emptyset$.

$(a,b]\subseteq\mathbb{R}$ is not closed and not open.

⚠️ **Theorem**

$A$ is open iff $A^c$ is closed.

⚠️ **Theorem**

If $A_\alpha$, $\alpha\in\mathcal A$, are open, then $\bigcup_{\alpha\in\mathcal A}A_\alpha$ is open.

If $A_i$, $1\leq i\leq N$, are open, then $\bigcap_{i=1}^{N}A_i$ is open.

## Compactness

**Definition.**

(i) $A\subseteq X$ is **compact** if every open cover has a finite subcover.

(ii) $A\subseteq X$ is **limit point compact** if every infinite set $E\subseteq A$ has a limit point in $E$; often $E=\{x_n\mid n\in\mathbb N\}$.

(iii) $A\subseteq X$ is **sequentially compact** if every sequence $\{x_n\}_{n\in\mathbb N}$ in $A$ has a convergent subsequence.

⚠️ **Theorem**

(i), (ii), and (iii) are equivalent.

- If $A$ is compact, then $A$ is closed and bounded. If $X\subseteq\mathbb{R}^n$, the reverse implication also holds. ⭐ **Heine–Borel Theorem**
- If $B\subseteq A$, $A$ is compact, and $B$ is closed, then $B$ is compact.

## Bolzano–Weierstrass Theorem

If $\{x_n\}_{n\in\mathbb N}$ is a bounded sequence in $\mathbb{R}^n$, then $\{x_n\}_{n\in\mathbb N}$ has a convergent subsequence.

## Sequences

**Definition.** $\lim_{n\to\infty}x_n=x$ iff for every $\epsilon>0$, there exists $N\in\mathbb N$ such that for every $n\geq N$, $d(x_n,x)<\epsilon$.

A sequence $\{x_n\}_{n\in\mathbb N}$ is **Cauchy** iff for every $\epsilon>0$, there exists $N\in\mathbb N$ such that for every $n,m\geq N$, $d(x_n,x_m)<\epsilon$.

⚠️ **Theorem**

Convergent $\Rightarrow$ Cauchy $\Rightarrow$ bounded.

*(supremum exists)*

⚠️ **Theorem**

If $\{x_n\}_{n\in\mathbb N}$ is a sequence in $\mathbb{R}$ that is monotonically increasing and bounded, then it converges.

**Definition.** $X$ is called **complete** if all Cauchy sequences converge.

⚠️ **Theorem**

(i) If $X$ is compact, then $X$ is complete.

(ii) $\mathbb{R}^n$ is complete. ⭐ **Cauchy Criterion**

## Series

**Definition.** Let $\{a_n\}_{n\in\mathbb N}$ be a sequence in $\mathbb{C}$. The series $\sum_{n=0}^{\infty}a_n$ converges iff the sequence of partial sums $S_N=\sum_{n=0}^{N}a_n$ converges.

### Examples

**Geometric Series:** $\sum_{n=0}^{\infty}x^n$ converges iff $|x|<1$.

**Harmonic Series:** $\sum_{n=1}^{\infty}\frac1n$ diverges.

These are powerful when combined with the **Comparison Test**.

⚠️ **Theorem**

If $\sum a_n$ converges, then $\lim_{n\to\infty}a_n=0$.

## Continuity

**Definition.** A function $f:X\to Y$ is **continuous at $x_0$** iff for every $\epsilon>0$, there exists $\delta>0$ such that $f(B_\delta(x_0))\subseteq B_\epsilon(f(x_0))$.

That is, $\lim_{x\to x_0}f(x)=f(x_0)$.

⚠️ **Theorem**

The following are equivalent:

(i) $f$ is continuous.

(ii) $\lim_{n\to\infty}f(x_n)=f(x)$ for every sequence $\{x_n\}_{n\in\mathbb N}$ such that $\lim_{n\to\infty}x_n=x$.

(iii) $f^{-1}(A)$ is open for every open $A\subseteq Y$.

⚠️ **Theorem**

If $f:X\to Y$ is continuous and $K\subseteq X$ is compact, then $f(K)$ is compact.

**Corollary.** If $f:X\to\mathbb{R}$ and $X$ is compact, then $f$ attains a maximum on $X$.

⚠️ **Theorem**

If $f:X\to Y$ is continuous and $X$ is compact, then $f$ is **uniformly continuous**.

In this case, $\delta$ does not depend on $x_0$.
