---
weight: 9
---
Linear differential equation:

$$
L(y)=c_{0}(x) \frac{d^{n}y}{dx^{n}}+c_{1}(x) \frac{d^{n-1}y}{dx^{n-1}}+...+c_{n}y=f(x)
$$

where $c_{i}$ are real or complex valued continuous functions on an interval I=$[a,b]$

Periodic boundary conditions

$$
y(a)=y(b),y'(a)=y'(b),...,y^{n-1}(a)=y^{n-1}(b)
$$

Linear forms stated at 'a' and 'b'

$$
v_{k}(y)= \left(\alpha_{k}^{0}y(a)+ \alpha_{k}^{1} \frac{dy}{dx}(a)+...+ \alpha_{k}^{n-1} \frac{d^{n-1}}{dx^{n-1}}(a)\right)+\left(\beta_{k}^{0}y(b)+ \beta_{k}^{1} \frac{dy}{dx}(b)+...+ \beta_{k}^{n-1} \frac{d^{n-1}}{dx^{n-1}}(b)\right)
$$

Homogeneous linear forms if $\forall k(v_{k}(y)=0)$

### Classification


#### Linear homogeneous BVP

L(y)=0 satisfying homogeneous linear forms $v_{k}(y)=0$

#### Linear non-homogenous BVP

If the linear forms are linearly independent, then finding a solution to $L(y)=f(x)$ is called a linear non-homogeneous BVP

### Regular BVP

A linear BVP (homogeneous or non-homogeneous) is called a regular BVP if

1. a,b are finite
2. $c_{0}(x)\ne0$ on $[a,b]$

### Singular BVP

A linear BVP is singular if it's not regular.

# Vital BVPs

$$
\frac{d^{2}y}{dx^{2}}=f(x,y,\frac{dy}{dx})
$$

## First BVP

Solving the Vital BVP with boundary conditions

$$
y(a)=\alpha,y(b)=\beta
$$

Equation has preassigned values at a,b

## Second BVP

Solving the Vital BVP with boundary conditions

$$
\begin{align*}
y(a)=\alpha_{1},y'(b)=\alpha_{2}\\
\text{OR}\\
y'(a)=\beta_{1},y(b)=\beta_{2}
\end{align*}
$$

Equation with preassigned value at one point and a prescribed slope at the other

## Third BVP

Solving the Vital BVP with boundary conditions

$$
y'(a)=\alpha,y'(b)=\beta
$$

Equation that has prescribed slopes at a and b.

# Strum Liouville Problems SLP

$$
\frac{d}{dx}(r(x) \frac{dy}{dx})+(q(x)+\lambda p(x))y=0
$$

r,q,p,r' are real-valued continuous functoins defined on interval I.

$\lambda$ is a real parameter.

## Boundary Conditions

$$
\begin{align*}
k_{1}y(a)+k_{2} \frac{dy}{dx}(a)=0\\
\text{OR}\\
k_{3}y(b)+k_{4} \frac{dy}{dx}(b)=0\\
\\
\text{Periodic boundary conditions}\\
y(a)=y(b),y'(a)=y'(b),r(a)=r(b)
\end{align*}
$$

## Eivenvalue and Eigenfunction

y(x)=0 is a trivial solution for Strum Lioville.

$\lambda$ for which it has a non-trivial solution is called **eigenvalue** and non-trivial solution associated with it is called **eigenfunction**

## Representation of other DE in SLP

### Legendre equation

$$
\begin{align*}
(1-x^{2}) \frac{d^{2}y}{dx^{2}}-2x \frac{dy}{dx}+ n(n+1)y=0\\
\frac{d}{dx}((1-x^{2}) \frac{dy}{dx})+ \lambda y=0\\
\lambda=n(n+1)
\end{align*}
$$

### Bessel's equation

## Example

$$
\begin{align*}
\frac{d^{2}y}{dx^{2}}+ \lambda y=0\\
y(0)=0,y(\pi)=0\\
\\
\text{Eigenvalues: }\lambda=n^{2} \text{ where }n\in \mathbb{N}\\
\text{Eigenfunctions: }a_{n}\sin (\sqrt \lambda x)
\end{align*}
$$

## Theorem

The differential equation:

[[#Strum Liouville Problems SLP|Strum Liouville Problems SLP]]

With the conditions:

$$
\begin{align*}
k_{1}y(a)+k_{2}y'(a)=0\\
k_{3}y(b)+k_{4}y'(b)=0
\end{align*}
$$

Conclusion: 
- There exists an infinite number of eigenvalues $\lambda_{n}$ and it can be arranged in monotonic increasing sequence. 
- For each $\lambda_{n}$ there exists one-parameter family of eigenfunctions $\phi_{n}$ and any 2 eigenfunctions corresponding to the same eigenvalue are nonzero constant multiples of each other. 
- Each eigenfunction $\phi_{n}$ has exactly (n-1) zeroes in the interval (a,b)

# Characteristic Value and Characteristic function

> Characteristic value, function = eigen value, function

Proof:

Consider $\lambda= \alpha+ i \beta$ and corresponding eigenfunction $y(x)+u(x)+iv(x)$

Substituting in the SLP and then equating the real and imaginary parts of the DE to 0, we obtain that $\beta=0$. Therefore, $\lambda$ is real.

## Existence 

> [!Theorem]
> Eigenvalues $\lambda$ are real valued

## Orthogonality of eigenfunctions


### Definition

$\phi_{1},\phi_{2}$ are orthogonal with respect to weight function $p(x)>0$ if

$$
\int_{a}^{b} p(x)\phi_{1}(x)\phi_{2}(x)dx=0
$$

Norm of $\phi_{1}$

$$
||\phi_{1}||=\sqrt{\int p(x) \phi_{1}^{2}(x)dx}
$$

Orthonormal: if the functions are orthogonal and the norm of each one = 1 

## Theorem

> [!Theorem]
> Eigen functions of SLP ([[#Strum Liouville Problems SLP|Strum Liouville Problems SLP]]) $\phi_{m},\phi_{n}$ are orthogonal with respect to p(x)

Boundary conditions that can be dropped
1. If r(a)=0
	1. $k_{1}y(a)+k_{2}y'(a)=0$ can be dropped
2. If r(b)=0
	1. $k_{3}y(b)+k_{4}y'(b)=0$ can be dropped
3. If r(a)=r(b)
	1. Boundary conditions can be replaced by periodic $y(a)=y(b),y'(a)=y'(b)$
	2. called Periodic Strum-Liouville problem

### Proof

Let $\phi_{m},\phi_{n}$ be the eigenfunctions satisfying SLP for eigenvalues $\lambda_{m},\lambda_{n}$

$$
\begin{align*}
\frac{d}{dx}(r(x) \frac{d \phi_{m}}{dx})+(q(x)+\lambda_{m}p(x))\phi_{m}(x)=0\\
\frac{d}{dx}(r(x) \frac{d \phi_{n}}{dx})+(q(x)+ \lambda_{n}p(x))\phi_{n}(x)=0\\
\\
(\lambda_{m}-\lambda_{n})\int_{a}^{b}p(x)\phi_{m}(x)\phi_{n}(x)dx&= [r(x)(\frac{d \phi_{n}}{dx}\phi_{m}(x)- \frac{d \phi_{m}}{dx}\phi_{n}(x))]_{a}^{b}
\end{align*}
$$

#### If r(a) and r(b) = 0

RHS automatically becomes 0.

LHS=0, therefore the eigenfunctions are orthogonal

#### If r(a)=0 only

Utilize the following to make the RHS=0

$$
\begin{align*}
k_{3}\phi_{n}(b)+k_{4}\phi_{n}'(b)=0\\
k_{3}\phi_{m}(b)+k_{4}\phi_{m}'(b)=0
\end{align*}
$$


#### If r(b)=0 only

Utilize the following to make the RHS=0

$$
\begin{align*}
k_{1}\phi_{n}(a)+k_{2}\phi_{n}'(a)=0\\
k_{1}\phi_{m}(a)+k_{2}\phi_{m}'(a)=0
\end{align*}
$$


#### If both are non zero

We use both the boundary conditions and proceed.

### Examples

