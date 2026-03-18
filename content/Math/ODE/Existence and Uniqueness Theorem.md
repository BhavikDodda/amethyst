---
weight: 5
---
## Sufficient condition for existence of solution

Consider a [[Math/ODE/DE in two var|DE in two var]]:
$$
\frac{d y}{d x}=f(x,y)
$$

- Let f 
	- be continuous on D
	- satisfies [[Math/ODE/Lipschitz condition|Lipschitz condition]] (wrt y) in D
- Let $(x_{0},y_{0})$ be an interior point in D and $a,b$ such that rectangle $|x-x_{0}|\le a,|y-y_{0}|\le b$ lies in D
- Let $M=\max(f(x,y))$ and $h=\min\left(a, \frac{b}{M}\right)$

If these are met, there exists a unique solution $\phi$ of the IVP on $|x-x_{0}|\le h$



## uniqueness

We assume there are $\phi(x),\psi(x)$ satisfying the IVP, and prove that they must be equal

we will bisect the interval and first prove for the right half $x_{0}\le x\le x_{0}+h$

$$
\begin{align*}
|\phi(x)-\psi(x)|&\le \left|\int_{x_{0}}^{x}f[t,\phi(t)]-f[t,\psi(t)]dt\right| \\
&\le \int_{x_{0}}^{x}|f[t,\phi(t)]-f[t,\psi(t)]|dt\\
\\\\
\text{because it follows Lipschitz condition}\\
f[t,\phi(t)]-f[t,\psi(t)]&\le K |\phi(t)-\psi(t)|\\
\\
|\phi(x)-\psi(x)|&\le  K\int_{x_{0}}^{x}|\phi(t)-\psi(t)|dt\\
\\
\text{Let }U(x)&= \int_{x_{0}}^{x}|\phi(t)-\psi(t)|dt\\
\text{So, }U'(x)&\le kU(x)\\
U'(x)-kU(x)&\le 0\\
(U'(x)-kU(x))e^{-K(x-x_{0})}&\le 0\\
\frac{d}{dx}(U(x)e^{-K(x-x_{0})})\le 0\\
\text{By integrating, we get}\\
U(x)e^{-K(x-x_{0})}-U(x_{0})e^{-K(x_{0}-x_{0})}&\le 0\\
U(x_{0})=0, \text{so }U(x)e^{-K(x-x_{0})}&\le 0\\
U(x)&\le 0\\
\\
\text{But we know }U(x)&\ge 0\\
\therefore U(x)=0\\
\end{align*}
$$

Since integrand is continuous, the only possible way for that to happen is $\phi(x)=\psi(x)$ for $x\ge x_{0}$

Similarly, we can prove for $x_{0}-h\le x\le x_{0}$

# Picards iteration convergence

[[ODE Methods#Picard's Method]]

Iteration on g, let us name that $T_{g}(x)=y_{0}+\int_{x_{0}}^{x}f[t,g(t)]dt$

## Bounding iterations

In the interval $|x-x_{0}|\le h$, if $|g(x)-y_{0}|\le b$, then $|T_{g}(x)-y_{0}|\le b$

$h\le \frac{b}{M}$ will be used here

$$
\begin{align*}
|T_{g}(x)-y_{0}|&\le  |\int_{x_{0}}^{x}f[t,g(t)]dt|\\
&\le \int_{x_{0}}^{x}|f[t,g(t)]|dt\\
&\le M\int_{x_{0}}^{x}dt\\
&\le M|x-x_{0}|\\
&\le Mh\\
&\le b
\end{align*}
$$

## Convergence to solution

> $\phi_{n}$ converges to solution $\phi(x)$

$$
\begin{align*}
M_{0}&= \max_{|t-x_{0}|\le h}|f(t,y_{0})|\\
\phi_{n}(x)&= y_{0}+\int_{x_{0}}^{x}f[t,\phi_{n-1}(t)]dt\\
\\
\text{The following estimate holds:}\\
|\phi_{n+1}(x)-\phi_{n}(x)|&\le M_{0}K^{n} \frac{|x-x_{0}|^{n+1}}{(n+1)!}\\
\\
|\phi(x)-\phi_{n}(x)|&\le M_{0}K^{n} \frac{|x-x_{0}|^{n+1}}{(n+1)!}e^{K|x-x_{0}|}
\end{align*}
$$

We can prove the first estimate using induction. 

