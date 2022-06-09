# Lecture 9
#### fundamental theorem  of LP
(1) infeasible $\Harr$ certificate  
(2) unbounded $\Harr$ certificate  
(3) it has an optimal solution $\Harr$ certificate  


> Definition (equivalent of LPs  )

Two linear programs $p$ and $p'$ are equivalent if  <br/>
(1) $p$ is infeasible $\Harr$ $p'$ is infeasible <br/>
(2) $p$ is unbounded $\Harr$ $p'$ is unbounded <br/>
(3) given any optimal solution to $p$, one can only construct an optimal solution to $p'$, and vice versa

1. $minimzation \rightarrow maximization$ <br/>
$\min -f(x) = -\max f(x)$ <br/>
Example  <br/>
$\min 2x-2y \Harr -\max -2x+2y$

2. Inequality  $\Rightarrow$ equality
Example: <br/>
$max Ax\leq b$ <br/>
$Ax+z=b, z\geq 0$

3. Free variables   <br/>
$max\ c^Tx$ <br/>
$Ax=b$ <br/>
x are free

#### Standard equality form
Any linear programs can be written as the following standard equality form <br/>
$max c^Tx+\epsilon$ <br/>
$subject\ to$
$Ax=b\ x\geq 0$

### A taste of simplex 
$max\ (3,-2,0,0,0)x$
$$
    s.t 
    \begin{pmatrix}
    4 & -1 & 1 & 0 & 0 \\
    3 & -3 & 0 & 1 & 0 \\
    -2 & 2 & 0 & 0 & 1 \\
    \end{pmatrix}
    \times x
= 

    \begin{pmatrix}
    8 \\
    9 \\
    1 \\
    \end{pmatrix} \\
x \geq 0
$$

Feasible solution: $\overline x = (0,0,8,9,1)^T$
objective value of $\overline x$ is 0
question: if $\overline x$ is optimal

