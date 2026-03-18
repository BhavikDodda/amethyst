---
weight: 6
---

> [!Theorem]
> Let g(x) and h(x) be continuous functions defined for $x>x_{0}$ such that $g(x),h(x)\ge 0$
> Let k>0 be a constant such that $g(x)\le k+\int_{x_{0}}^{x}g(t)h(t)dt$
> Then: $$g(x)\le ke^{\int_{x_{0}}^{x}h(t)dt}$$

## Proof

$$
\begin{align*}
\frac{g(x)h(x)}{k+\int_{x_{0}}^{x}g(t)h(t)dt}&\le h(x)\\
\text{Integrating both sides}\\
\left. \left(\log \left(k+\int_{x_{0}}^{x} g(t)h(t)dt\right)\right) \right|\_{x_{0}}^{x}&\le \int_{x_{0}}^{x}h(t)dt\\
\log\left(k+\int_{x_{0}}^{x}g(t)h(t)dt\right)-\log(k)&\le \int_{x_{0}}^{x}h(t)dt\\
\\
\left(k+\int_{x_{0}}^{x}g(t)h(t)dt\right)k^{-1}&\le e^{\int_{x_{0}}^{x}h(t)dt}\\
\text{Using the given,}\\
g(x)&\le k e^{\int_{x_{0}}^{x}h(t)dt}
\end{align*}
$$

## Corollary

> If $g(x)\ge0$ and k is a constant such that $k>0$, then if $g(x)\le k\int_{x_{0}}^{x}g(t)dt$, 
> Then g(x)=0

We can use Gronwalls Integral Inequality with $g(x)=g(x);h(x)=k$

$$
\begin{align*}
\forall \epsilon>0\\
g(x)&\le \epsilon+\int_{x_{0}}^{x}g(t)kdt\\
g(x)&\le \epsilon e^{\int_{x_{0}}^{x}kdt}\\
&\le \epsilon e^{k(x-x_{0})}\\
g(x)&= 0
\end{align*}
$$