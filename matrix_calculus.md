# Matrix Calculus



**y** : m by 1,             **x** : n by 1;        **A** :  m by n

## Section 1: rules



| rule                                       | variable                  | derivative                                                   |
| ------------------------------------------ | ------------------------- | ------------------------------------------------------------ |
| V to V                                     | $\frac{\part y}{\part x}$ | $\left[\begin{array}{cccc}\frac{\partial y_{1}}{\partial x_{1}} & \frac{\partial y_{2}}{\partial x_{1}} & \cdots & \frac{\partial y_{m}}{\partial x_{1}} \\\frac{\partial y_{1}}{\partial x_{2}} & \frac{\partial y_{2}}{\partial x_{2}} & \cdots & \frac{\partial y_{m}}{\partial x_{2}} \\\vdots & \vdots & \ddots & \vdots \\\frac{\partial y_{1}}{\partial x_{n}} & \frac{\partial y_{2}}{\partial x_{n}} & \cdots & \frac{\partial y_{m}}{\partial x_{n}}\end{array}\right]$ |
| S to V                                     | $\frac{\part y}{\part x}$ | $\left[\begin{array}{c}\frac{\partial y}{\partial x_{1}} \\\frac{\partial y}{\partial x_{2}} \\\vdots \\\frac{\partial y}{\partial x_{n}}\end{array}\right]$ |
| V to S                                     | $\frac{\part y}{\part x}$ | $\left[\begin{array}{llll}\frac{\partial y_{1}}{\partial x} & \frac{\partial y_{2}}{\partial x} & \ldots & \frac{\partial y_{m}}{\partial x}\end{array}\right]$ |
| S to M                                     | $\frac{\part y}{\part x}$ | $\left[\begin{array}{cccc}\frac{\partial y}{\partial x_{11}} & \frac{\partial y}{\partial x_{12}} & \ldots & \frac{\partial y}{\partial x_{1 n}} \\\frac{\partial y}{\partial x_{21}} & \frac{\partial y}{\partial x_{22}} & \cdots & \frac{\partial y}{\partial x_{2 n}} \\\vdots & \vdots & & \vdots \\\frac{\partial y}{\partial x_{m 1}} & \frac{\partial y}{\partial x_{m 2}} & \ldots & \frac{\partial y}{\partial x_{m n}}\end{array}\right]$ |
| Chain rule: $z=f(y),y=g(x)$                | $\frac{\part z}{\part x}$ | $\frac{\part y}{\part x} \frac{\part z}{\part y}$            |
| Chain rule: $w=h(z), z=f(y),y=g(x)$        | $\frac{\part w}{\part x}$ | $\frac{\part y}{\part x} \frac{\part z}{\part y} \frac{\part w}{\part z}$ |
| Trace $y= tr(X), X\in R^{n\times n}$       | $\frac{\part y}{\part X}$ | $I$                                                          |
| $X \quad and \quad Y$ are matrix           | -                         | $d(\mathbf{X Y})=(d \mathbf{X}) \mathbf{Y}+\mathbf{X}(d \mathbf{Y})d(\mathbf{X Y})=(d \mathbf{X}) \mathbf{Y}+\mathbf{X}(d \mathbf{Y})$ |
| $X$ are matrix                             | $d \mathbf{X^{-1}}$       | $d\left(\mathbf{X}^{-1}\right) \mathbf{X}+\mathbf{X}^{-1} d \mathbf{X}=\mathbf{0}$ $\rightarrow$ $d\left(\mathbf{X}^{-1}\right) =-\mathbf{X}^{-1} d \mathbf{X}\mathbf{X}^{-1}$ |
| $x$ is vector, $A$ is matrix $f = x^T A x$ | $df/dA$                   | $xx^T$                                                       |





## Section 2: example



| convention                             | variable                      | partial differentiation                                      |
| -------------------------------------- | ----------------------------- | ------------------------------------------------------------ |
| $ y =Ax$                               | $\partial y/ \partial x$      | $A^T$                                                        |
| $ y =Ax,x=f(z)$                        | $\partial y/ \partial z$      | $\partial y/ \partial x * \partial x/ \partial z = A^T*\partial x/ \partial z$ |
| $\alpha =y^TAx$                        | $\partial \alpha/ \partial y$ | $Ax$                                                         |
| $\alpha = x^TAx$ , $m=n$               | $\partial \alpha/ \partial x$ | $(A+A^T)x$                                                   |
| $\alpha = x^TAx$ , $m=n$, $A^T = A$    | $\partial \alpha/ \partial y$ | $2Ax$                                                        |
| $\alpha=y^Tx, x =f(z) y=f(z)\quad m=n$ | $\partial \alpha/ \partial z$ | $x\frac{\partial y}{\partial z}+y\frac{\partial x}{\partial z}$ |
| $\alpha = y^TAx, y=f(z),x=f(z)$        | $\partial \alpha/ \partial z$ | $Ax\frac{\part y}{\part z}+A^ty\frac{\part x}{\part z}$      |
|                                        |                               |                                                              |
|                                        |                               |                                                              |

 



