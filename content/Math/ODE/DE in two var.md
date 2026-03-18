---
title: Differential Equations in 2 variables
weight: 4
---

$$
\frac{dy}{dx}=f(x,y)
$$
where f is defined on a domain D and $(x_{0},y_{0})$ be an interior point of D.

$\phi(x)$ is a solution of this DE IVP (Initial Value Problem) if it satisfies

1. $[x,\phi(x)]\in D$ and thus $f[x,\phi(x)]$ is defined for $x\in [\alpha,\beta]$ containing $x_{0}$
2. $$\frac{d \phi(x)}{d x}=f(x,\phi(x))$$
3. $\phi(x_{0})=y_{0}$



# Necessary and sufficient condition

> $\phi(x)$ is a solution of the IVP over $[\alpha,\beta]$ if and only if it satisfies the integral equation: $$\phi(x)= y_{0}+\int_{x_{0}}^{x}f[t,\phi(t)]dt;\forall x\in [\alpha,\beta]$$

## necessary part

If it's a solution, then it has to satisfy the integral equation.

$$
\begin{align*}
\frac{d \phi(x)}{d x}=f(x,\phi(x))\\
\phi(x)=\int_{x_{0}}^{x}f(x,\phi(x))dx+c\\
\text{To satisfy }\phi(x_{0})=y_{0}\\
c=y_{0}\\
\end{align*}
$$

## sufficient part

$$
\begin{align*}
\phi(x)= y_{0}+\int_{x_{0}}^{x}f[x,\phi(x)]dt\\
\text{Clearly, it satisfies}\\
\frac{d \phi(x)}{d t}=f[x,\phi(x)]
\end{align*}
$$

