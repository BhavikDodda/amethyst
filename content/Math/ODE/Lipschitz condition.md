---
weight: 3
---

Let f be defined on a [[Math/ODE/topology stuff#Domain|Domain]] or closed domain D of the XY plane.

f is said to satisfy Lipschitz condition (wrt y) in D, if 

$$
\exists K(\forall (x,y_{1}),(x,y_{2})\in D(f(x,y_{1})-f(x,y_{2})\le K|y_{1}-y_{2}|))
$$

## Sufficient condition

By [[Mean Value Theorems#First Mean Value Theorem]] of two variable functions, if $\frac{\partial f}{\partial y}$ is bounded by M,

$$
\begin{align*}
\exists E\in[y_{1},y_{2}]: f(x,y_{1})-f(x,y_{2})=(y_{1}-y_{2}) \frac{\partial f(x,E)}{\partial y}\\
|f(x,y_{1})-f(x,y_{2})|<|y_{1}-y_{2}|M
\end{align*}
$$

Therefore, sufficient condition for Lipschitz condition is for $\frac{\partial f}{\partial y}$ to be bounded where lipscitz constant = 

$K=M=lub_{(x,y)\in D}(\frac{\partial f}{\partial y})$

# With vector valued functions