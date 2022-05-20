# Lecture 8 of CO 250
#### unbounded linear programs (feasible )
$\max x$
$s.t\ x\geq 1$ <br/>
or we can write it as<br/>
$\max x'$
$s.t\ x-y=1,x\geq 0 \And y\geq 0$

Object value  is $+\infin$ and it is unbounded

**Definition of unbounded linear programs**  <br/>
A **maximum** linear programs is unbounded if there exists a 
series of feasible solutions $X(t)$ such that the objective value approach 
$+\infin$ as $t\rightarrow+\infin$
*example*
$(1+t,0+t)^T=(1,0)^T+t\times (1,1)^T, t\geq 0$

If an linear programs is unbounded, then its feasible region is also unbounded.

$$
    Ax\leq b \\
    Ax+y \lt b \\
    y\geq 0
$$
$$
    A = 
    \begin{bmatrix}
    A & I \\
    -I & 0
    \end{bmatrix}
    \times 
    \begin{bmatrix}
    x \\
    y 
    \end{bmatrix}
\leq 
    \begin{bmatrix}
    b \\
    0 
    \end{bmatrix}
$$
$-Ax\leq -b$ <br/>
$Ax \leq b$ <br/>
$-x\leq 0$

*Example* 
$\max (-1,2,3,4)x$
such that
$$
    \begin{bmatrix}
    3,0,2,-5 \\
    -2,3,-4,4 
    \end{bmatrix}
     x = 
    
    \begin{bmatrix}
    4 \\
    1 
    \end{bmatrix} \\ 
   x \geq 0 
$$
$$
    d=
    
    \begin{bmatrix}
    0 & 4 & 5 & 2
    \end{bmatrix} \\ 
$$
check :
$$
    c^Td=31\gt 0 \\
\overline x = 
    \begin{bmatrix}
    3 & 1 & 0 & 1
    \end{bmatrix} \\ 
$$
$(\overline x,d)$ is a certificate of unbounded linear programs


find $X(t)$ such that $Ax(t)=b,x(t)\geq 0$

We need: <br/>
1. feasible region is unbounded 
2. the object value can be bounded or unbounded 
---  

1. $A\overline x=b,\overline x\geq 0$
2. $Ad=0,d\geq 0$
3. $c^Td\gt 0$

$$
    x=\overline x + dt \\
    A(x) = A \overline x + Adt \\
    \overline x +dt \geq 0 \\
    cx=(\overline x) + t c^Td\rightarrow \infin\ as\ t\rightarrow \infin
$$

**Proposition**  
the Linear programs $max \{c^Tx:Ax=b,x\geq0\}$
is unbounded if there exists feasible solution
$\overline x$ and a vector d such that $Ad=0, d\geq 0,c^Td\lt 0$
*Note* the converse of that statement is true  

1. linear programs with optimal solution <br/>
*example* 
$$
    \max 
    \begin{bmatrix}
   1 & 3 & -5 & 0\\
   0 & -1 & 2 & 1\\
\end{bmatrix}x = 
    \begin{bmatrix}
    6 \\
    9
    \end{bmatrix}
x\geq 0 \\
    x = 
    \begin{bmatrix}
    x_1 \\
    x_2 \\
    x_3 \\
    x_4 \\
    \end{bmatrix}
    = 
    \begin{bmatrix}
    6 \\
    0 \\
    0 \\
    9 \\
    \end{bmatrix}
is\ feasible \\
$$ 
The object value is 7 since 
$-2x_2+-3x_3+7\leq7$ <br/>
since $x_2,x_3\geq0$
**summary**  
fundamental  theorem  of linear programs 
for ant linear programs, exactly one of the three thing hold
1.infeasible 
2. is unbounded (feasible )
3. has an optimal solution
