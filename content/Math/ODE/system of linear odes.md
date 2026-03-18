---
weight: 7
---
$$
\begin{align*}
\frac{dx}{dt}=a_{1}(t)x+b_{1}(t)y+f_{1}(t)\\
\frac{dy}{dt}=a_{2}(t)x+b_{2}(t)y+f_{2}(t)
\end{align*}
$$

# Theorems

## General sol

If homogeneous system has 2 linearly independent solutions $x_{1}(t),y_{1}(t)$ and $x_{2}(t),y_{2}(t)$ then general solution: 
$c_{1}x_{1}(t)+c_{2}x_{2}(t),c_{1}y_{1}(t)+c_{2}y_{2}(t)$

If non homogeneous solution has also a particular solution $x_{p}(t),y_{p}(t)$, then general solution:
$c_{1}x_{1}(t)+c_{2}x_{2}(t)+x_{p}(t),c_{1}y_{1}(t)+c_{2}y_{2}(t)+y_{p}(t)$

## derivative of wronskian

$$
\begin{align*}
\frac{d}{dt}W[t]&= \\
\\
&= [a_{1}+b_{2}]W
\end{align*}
$$

It is either 0 or "nowhere vanishing".

# Solving

## constant coeff

We assume the solution of form $x(t)=Ae^{mt};y(t)=Be^{mt}$ and get an auxilary equation in terms of m

$$
\begin{align*}
A(a_{1}-m)+B(b_{1})=0\\
A(a_{2})+B(b_{2}-m)=0
\end{align*}
$$


$|Coeff-mI|=0 \Leftrightarrow m^{2}-(a_{1}+b_{2})m+(a_{1}b_{2}-a_{2}b_{1})=0$ for non-trivial solutions

### different auxilary roots

#### real

If the auxiliary roots $m_{1},m_{2}$ are inequal, then we find 2 linear independent solutions
$A_{1},B_{1}$ corresponding to $m_{1}$
$A_{2},B_{2}$ corresponding to $m_{2}$

#### imaginary

> If the auxilary root is imaginary, just consider one auxilary root and split the real and im parts to get 2 linearly independent solutions.

$$
\begin{align*}
x=(A_{1}+iA_{2})e^{(a+ib)t}\\
y=(B_{1}+iB_{2})e^{(a+ib)t}\\
\\
x&= e^{at}((A_{1}\cos bt-A_{2}\sin bt)+i(A_{1}\sin bt+A_{2}\cos bt))\\
y&= a^{at}((B_{1}\cos bt-B_{2}\sin bt)+i(B_{1}\sin bt+B_{2}\cos bt))
\end{align*}
$$

### same auxiliary roots

2nd solution would be of form

$\begin{cases}(A_{1}+A_{2}t)e^{mt} \\(B_{1}+B_{2}t)e^{mt}\end{cases}$

$$
\begin{align*}
(mA_{1}+A_{2}+mA_{2}t)e^{mt}=a_{1}(A_{1}+A_{2}t)e^{mt}+b_{1}(B_{1}+B_{2}t)e^{mt}\\
(mB_{1}+B_{2}+mB_{2}t)e^{mt}=a_{2}(A_{1}+A_{2}t)e^{mt}+b_{2}(B_{1}+B_{2}t)e^{mt}\\
\\
(a_{1}A_{2}+b_{1}B_{2}-mA_{2})t+(a_{1}A_{1}+b_{1}B_{1}-mA_{1}-A_{2})=0\\
(a_{2}A_{2}+b_{2}B_{2}-mB_{2})t+(a_{2}A_{1}+b_{2}B_{1}-mB_{1}-B_{2})=0\\
\\\\
A_{2}(a_{1}-m)+B_{2}(b_{1})=0\\
A_{2}(a_{2})+B_{2}(b_{2}-m)=0\\
\\
A_{2},B_{2}=A,B \text{ (same as coeffs of the first sol)}
\end{align*}
$$

## using matrix exponential

$$
\begin{align*}
\frac{dX}{dt}=AX\\
X: \text{col matrix }x(t),y(t)\\
A: \text{coeff matrix }\\
\\
S=e^{At}
\end{align*}
$$

S is a 2x2 matrix (C1 C2) where C1,C2 are the columns

It follows that:

$$
\begin{align*}
\frac{dC_{1}}{dt}=AC_{1}\\
\frac{dC_{2}}{dt}=AC_{2}\\
\end{align*}
$$
C1,C2 are 2 linearly independent solutions of X(t)