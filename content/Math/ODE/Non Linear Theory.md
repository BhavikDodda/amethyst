---
weight: 8
---
# General

$$
\begin{align*}
\frac{dx}{dt}=F(x,y)\\
\frac{dy}{dt}=G(x,y)
\end{align*}
$$

Solution to this is a directed curve. 

The critical points can be found by solving $F(x,y)=0,G(x,y)=0$

Types of critical points

1. Node
	1. Stable
	2. Unstable
2. Saddle point
3. Center
4. Spiral

# Critical Points and Stability for linear system

Depends on auxilary roots of [[Math/ODE/system of linear odes|system of linear odes]]

$$
\begin{align*}
\frac{dx}{dt}&= a_{1}x+b_{1}y\\
\frac{dy}{dt}&= a_{2}x+b_{2}y\\
\\
\text{Auxilary quadratic equation}\\
m^{2}-(a_{1}+b_{2})m+(a_{1}b_{2}-a_{2}b_{1})=0\\
x=Ae^{mt};y=Be^{mt}
\end{align*}
$$

Since it has (0,0) critical point which has to be isolated, $a_{1}b_{2}-a_{2}b_{1}\ne 0$

Implies that 0 cannot be root.

## Real

### Distinct

#### Same sign (Case A)

**Node**

##### Negative

Asymptotically stable

##### Positive

Unstable

#### Opposite sign (Case B)

**Saddle Point**

Unstable

### Same (Case D)

**Node**

m>0 : unstable
m<0 : asymptotically stable

## Complex

### Pure Im (Case E)

**Center**

Stable

### Mixed (Case C)

**Spiral**

Asymptotically stable


# Critical Points and Stability Proof

## Case A

If the roots $m_{1},m_{2}$ are real and distinct and of same sign

### Negative

Let $m_{1}<m_{2}<0$

$$
\begin{align*}
\text{Solution:}\\
x&= c_{1}A_{1}e^{m_{1}t}+c_{2}A_{2}e^{m_{2}t}\\
y&= c_{1}B_{1}e^{m_{1}t}+c_{2}B_{2}e^{m_{2}t}
\end{align*}
$$

If $c_{2}=0$, then the path has slope $\frac{B_{1}}{A_{1}}$, if $c_{1}=0$ it has slope $\frac{B_{2}}{A_{2}}$. Otherwise, since $m_{1}-m_{2}<0$

$$

\frac{y}{x}= \frac{\left(\frac{c_{1}B_{1}}{c_{2}}\right)e^{(m_{1}-m_{2})t}+B_{2}}{(\frac{c_{1}A_{1}}{c_{2}})e^{(m_{1}-m_{2})t}+A_{2}}

$$

Other paths approach slope $\frac{B_{2}}{A_{2}}$ as $t\rightarrow \infty$ and enter (0,0)

> Critical point: **Node**
> Asymptotically stable

### Positive

Consider $m_{1}>m_{2}>0$

Exact same situation but happens as $t\rightarrow -\infty$

> Critical point: **Node**
> unstable

## Case B

Roots are real, distinct and of opposite sign

Let $m_{1}<0,m_{2}>0$

$$
\begin{align*}
\text{Solution:}\\
x&= c_{1}A_{1}e^{m_{1}t}+c_{2}A_{2}e^{m_{2}t}\\
y&= c_{1}B_{1}e^{m_{1}t}+c_{2}B_{2}e^{m_{2}t}
\end{align*}
$$

If $c_{2}=0$ the half-line paths enter (0,0) as $t\rightarrow \infty$ (second line) and when $c_{1}=0$ they enter (0,0) as $t\rightarrow - \infty$ (first line)

Otherwise, none of the paths approach (0,0) as $t\rightarrow \pm \infty$ and when $t\rightarrow \infty$ they approach the first line and when $t\rightarrow - \infty$ they approach the second line

> Critical point: **Saddle**
> Unstable

## Case C

Roots are conjugate complex but not purely imaginary

Discriminant of the auxilary equation is negative
$$
\begin{align*}
(a_{1}+b_{2})^{2}-4(a_{1}b_{2}-a_{2}b_{1})\\
= (a_{1}-b_{2})^{2}+4a_{2}b_{1}<0
\end{align*}
$$

Roots: $a\pm i b$
[[Math/ODE/system of linear odes#imaginary|imaginary]]
$$
\begin{align*}
x&= e^{at}(c_{1}(A_{1}\cos bt-A_{2}\sin bt)+c_{2}(A_{1}\sin bt+A_{2}\cos bt))\\
y&= a^{at}(c_{1}(B_{1}\cos bt-B_{2}\sin bt)+c_{2}(B_{1}\sin bt+B_{2}\cos bt))
\end{align*}
$$

If $a<0\Leftrightarrow (a_{1}+b_{2})<0$ then they approach the origin, but not enter it but wind around it in like a spiral-like manner.

$$
\begin{align*}
\frac{d\theta}{dt}&= \frac{xy'-yx'}{x^{2}+y^{2}}\\
&= \frac{a_{2}x^{2}+(b_{2}-a_{1})xy-b_{2}y^{2}}{x^{2}+y^{2}}
\end{align*}
$$

The determinant of numerator is <0

Therefore it is always positive when $a_{2}>0$ and negative when $a_{2}<0$


> Critical point: **Spiral**
> Asymptotically stable

The spiral might tend off to infinity if $a>0$

## Case D

Two subcases

$a_{1}=b_{2}=a,a_{2}=b_{1}=0$

$$
\begin{align*}
x(t)=c_{1}e^{mt}\\
y(t)=c_{2}e^{mt}
\end{align*}
$$

Other cases

$$
\begin{align*}
x(t)=c_{1}Ae^{mt}+c_{2}(A_{1}+A)e^{mt}\\
y(t)=c_{1}Be^{mt}+c_{2}(B_{1}+B)e^{mt}
\end{align*}
$$

> Both these cases, it's easy to see that it's a node
> - m<0: node, stable
> - m>0: node, unstable

## Case E

Same as case C with real part = 0

Solution is an ellipse centered at origin

> Critical point: **Center**
> stable

# Stability Theorems

Asymptotically stable iff both the roots have non-postitive real parts and it is unstable iff both have positive real roots.

The critical point of the linear system is asymptotically stable iff the coefficients of auxiliary equation are both +ve

$$
-(a_{1}+b_{2}),(a_{1}b_{2}-a_{2}b_{1})>0
$$

## Lyapunovs Method

For studying the stability problem in a broader context

$$
\begin{align*}
\frac{dx}{dt}=F(x,y)\\
\frac{dy}{dt}
=G(x,y)
\end{align*}
$$

Let E(x,y) be a function that is continuous and has continuous first partial derivatives.
E can be regarded as a function of t along solution $(x(t),y(t))$

Rate of change of E wrt t

$$
\frac{dE}{dt}= \frac{\partial E}{\partial x} \frac{dx}{dt}+ \frac{\partial E}{\partial y} \frac{dy}{dt}= \frac{\partial E}{\partial x}F+ \frac{\partial E}{\partial y}G
$$

A function E(x,y) of positive type and with $\frac{\partial E}{\partial x}F+ \frac{\partial E}{\partial y}G$ of negative semi-definite type is called a Lyapunov function for the system.

> [!Theorem]
> If there exists a Lyapunov function, then critical point is stable
> If additionally that the $\frac{\partial E}{\partial x}F+ \frac{\partial E}{\partial y}G$ is negative, then the critical point is asymptotically stable

### types

- Positive: E is 0 at origin and E>0 otherwise
	- $E(x,y)=ax^{2m}+by^{2n};a,b>0$
- Negative: E is 0 at origin and E<0 otherwise
	- $E(x,y)=ax^{2m}+by^{2n};a,b<0$
- Positive semi-definite: E is 0 at origin and $E\ge 0$ otherwise
	- $E(x,y)=x^{2m},y^{2n}, (x-y)^{2m}$
- Negative semi-definite: E is 0 at origin and $E\le 0$ otherwise

# Simple Critical Points of Nonlinear systems

The process of replacing a general system by simpler linear system is called linearization

$$
\begin{align*}
\frac{dx}{dt}=a_{1}x+b_{1}y+f(x,y)\\
\frac{dy}{dt}=a_{2}x+b_{2}y+g(x,y)
\end{align*}
$$

Assume $a_{1}b_{2}-a_{2}b_{1}\ne0$

Linearization by considering f,g=0 can be possible when

$$
\begin{align*}
\lim_{(x,y)\rightarrow (0,0)} \frac{f(x,y)}{\sqrt{x^{2}+y^{2}}}=0\\
\lim_{(x,y)\rightarrow (0,0)} \frac{g(x,y)}{\sqrt{x^{2}+y^{2}}}=0
\end{align*}
$$

- Implies that (0,0) is a critical point of the original system.
- Would also be of same type as the same case it would with its corresponding linearized system
- If it's asymptotically stable in the linearized system, it's also asymptotically stable in the non-linear version.