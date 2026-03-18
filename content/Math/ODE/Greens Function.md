---
weight: 10
---
#  Green's Function

L(y)=f(x)


A function G(x,t) defined for $a\le x\le t$, $t\le x \le b$ is called green's function of L(y) if it satisfies:

1. G(x,t) has derivatives upto order n.
	1. $$ \frac{\partial ^{k}G}{\partial x^{k}}|_{t^{-}}^{t^{+}}=0,k=0,1,2,...n-2 $$
	2. $$\frac{\partial ^{k}G}{\partial x^{k}}|_{t^{-}}^{t^{+}}= 1/c_0(t) ,k=n-1$$
2. G(x,t) considered as a function of x, is a solution of L(y)=0. L(G)=0 on each of the intervals. It satisfies linear homogeneous boundary conditions 

# Theorem of unique green function

> [!Theorem]
> If y(x)=0 is the only solution of the BVP $L(y)=0,V_{k}(y)=0$
> Then, L(y) has one and only one Green function

Let the basis solutions be $y_{1}...y_{n}$

$$
\begin{align*}
G(x,t)&= a_{1}y_{1}+a_{2}y_{2}+...a_{n}y_{n},a<x<t\\
G(x,t)&= b_{1}y_{1}+b_{2}y_{2}+...b_{n}y_{n},t<x<b\\
\end{align*}
$$

The derivative conditions are used to create n equations with n unknowns $p_{k}=b_{k}-a_{k}$. Find $p_{k}$ using cramer's rule

Applying boundary conditions 
$$
\begin{align*}
V_{k}(y)&= A_{k}(y)+B_{k}(y)\\
V_{k}(G)&= 0\\
(a_{1}A_{k}(y_{1})+a_{2}A_{k}(y_{2})+...+a_{n}A_{k}(y_{n})) +(b_{1}B_{k}(y_{1})+b_{2}B_{k}(y_{2})+...+b_{n}B_{k}(y_{n}))&= 0
\end{align*}
$$
Substitute $a_{k}=b_{k}-p_{k}$ and solve n equations for $b_{k}$ using cramer's rule

Therefore, we have the unique Green's function G(x,t) of L(y).

# Construction of Green's Function for second order equations

$$
\begin{align*}
L(y)&= c_{0}(x) y''+c_{1}(x) y'+c_{2}(x)y=0\\
G(x,t)&= \begin{cases}G_{1}(x,t),a\le x<t\\G_{2}(x,t),t<x\le b\end{cases}\\
G_{2}|_{x=t^{+}}-G_{2}|_{x=t^{-}}&= 0\\
\frac{\partial G_{2}}{\partial x}|_{x=t^{+}}-\frac{\partial G_{1}}{\partial x}|_{x=t^{-}}&= \frac{1}{c_{0}(t)} 
\end{align*}
$$

Let $y_{1},y_{2}$ be two linearly independent solution of 2nd order DE

Let $G_{1}(x,t)= a_{1}y_{1}(x),G_{2}(x,t)=a_{2}y_{2}(x)$

$$
\begin{align*}
a_{2}y_{2}(t)-a_{1}y_{1}(t)&= 0\\
a_{2} \frac{dy_{2}}{dt}- a_{1} \frac{dy_{1}}{dt}&= \frac{1}{c_{0}(t)}\\
a_{1},a_{2}\text{ satisfying this would be}\\
a_{1}&= \frac{-y_{2}(t)}{c_{0}(t)W(t)}\\
a_{2}&= \frac{-y_{1}(t)}{c_{0}(t)W(t)}\\
\end{align*}
$$

where W is the Wronskian of (y1,y2)

Therefore, G1, G2 have been found and therefore the green function.

Could also be given by

$$
G(x,t)= \frac{1}{c_{0}(t)W(t)}\begin{vmatrix}y_{1}(t) & y_{2}(t)\\y_{1}(x) & y_{2}(x)\end{vmatrix}
$$

In general, the first n-1 rows will contain upto (n-2) derivatives of $y_{k}(t)$

# Theorem of particular solution

General solution of $L(y)=f(x)$

$$
\begin{align*}
y(x)=a_{1}y_{1}(x)+a_{2}y_{2}(x)+...+a_{n}y_{n}(x)+\int_{x_{0}}^{x}G(x,t)f(t)dt
\end{align*}
$$