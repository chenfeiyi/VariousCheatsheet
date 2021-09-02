# Matrix Calculus



## Section 3: rules



## Section 2: example

**y** : m by 1,             **x** : n by 1;        **A** :  m by n

| convention                             | variable                      | partial differentiation                                      |
| -------------------------------------- | ----------------------------- | ------------------------------------------------------------ |
| $ y =Ax$                               | $\partial y/ \partial x$      | $A$                                                          |
| $ y =Ax,x=f(z)$                        | $\partial y/ \partial z$      | $\partial y/ \partial x * \partial x/ \partial z = A*\partial x/ \partial z$ |
| $\alpha =y^TAx$                        | $\partial \alpha/ \partial y$ | $x^TA^T$                                                     |
| $\alpha = x^TAx$ , $m=n$               | $\partial \alpha/ \partial x$ | $x^T (A+A^T)$                                                |
| $\alpha = x^TAx$ , $m=n$, $A^T = A$    | $\partial \alpha/ \partial y$ | $2x^TA$                                                      |
| $\alpha=y^Tx, x =f(z) y=f(z)\quad m=n$ | $\partial \alpha/ \partial z$ | $x^T\frac{\partial y}{\partial z}+y^T\frac{\partial x}{\partial z}$ |
| $\alpha = y^TAx, y=f(z),x=f(z)$        | $\partial \alpha/ \partial z$ | $x^TA^T\frac{\part y}{\part z}+y^TA^\frac{\part x}{\part z}$ |
|                                        |                               |                                                              |
|                                        |                               |                                                              |

 



