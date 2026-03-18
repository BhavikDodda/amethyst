---
title: Convergence of functions
weight: 1
---

[[Uniform Convergence]]

A sequence of functions {$f_n$} can be pointwise convergence to $f$ or uniformly continuous to $f$

If it's **uniformly continuous**, it carries over some interesting properties:
- if $\forall n,f_{n}$ is continuous, then $f$ is also continuous
- $\lim_{n\rightarrow \infty}\int_{a}^{b}f_{n}dx=\int_{a}^{b}fdx$

# series of functions
> [!Definition]
> The infinite series $\sum\limits u_{n}(x)$ is said to be convergent uniformly if the sequence of partial sums {$f_{n}$} defined by $f_{n}(x)=\sum\limits_{i=1}^{n}u_{i}(x)$ is convergent uniformly on some interval for x

## Weierstrass M-test

Series $\sum\limits u_{n}(x)$ converges uniformly on interval if it satisfies

> [!conditions]
> 1. $|f_{n}|<M_{n}$
> 2. $\sum\limits^{\infty} M_{n}$ converges

It can be shown that the partial sums are uniformly convergent utilizing convergence of $M_{n}$ and [[Uniform Convergence#Cauchy Criterion]] ([Weierstrass M-test - Wikipedia](https://en.wikipedia.org/wiki/Weierstrass_M-test))