# Lecture 7
---  
#### shortest path problem

$min \sum_{e\in E} W_ex_e$  
$\sum_{e\in \delta(w)} x_e\geq 1,\forall \delta(w)$  
$x_e\in\{0,1\}$

**key**  

1. If an set of edges $C\in E$ intersect every st cut, then this set 
C must contain on st-path
2. we assumed $w_e\geq 0$, if we have a redundant  edge which
one not in an st path. we can remove them to get a better solution
3. By the same argument , we do not need $x_e\leq 1$ any higher 
value is not optimal

**Full IP (shortest path)**
$min:w^{T}x$  
*such that*

$\sum_{e\in \delta(W)} x_e\geq 1,\forall \delta(W)$
which $\delta(W)$ is the set of st cuts

$X_e\geq 0, X_e \in \Zeta, \forall e\in E$

#### Non linear programming

- general form  

$min f(x)$ <br/>
such that <br/>
$g_i(x)\leq 0, \forall i\in R$ <br/>
$f: R^n \rightarrow R$ <br/>
$g: R^n \rightarrow R$ <br/>

Note:
1. A linear program is always a  non linear program
2. Integer program unless otherwise stated refer integer program as linear integer program   
(integer program is a special case for non linear program)  
3. Non linear program is harder to solve than linear program 

#### Solve linear programs
Computer will generate a short proof to show that result
is correct so we can verify the correctness quickly <br/>
A certificate  indicate our result is correct, so our algorithms  terminates

Possible outcome for linear program:
1. Infeasible
2. feasible but unbounded 
3. feasible and bounded

*example Infeasible linear programs* <br/>
$max\ 3x_1+x_2-7x_3+4x_4$ <br/>
subject to:  <br/>
$e1: -5x_1+4x_2+3x_3-x_4=3$ <br/>
$e2: 2x_1+x_2-5x_3+3x_4=-2$ <br/>
$e3: -x_1-3x_2+x_3-2x_4=1$

Solution : <br/>
a short proof that this is infeasible, multiply 1st row By
-2, second by -3, and third row by -4, Then add them
altogether  we get: <br/>
$8x_1+x_2+5x_3+x_4=-4$ <br/>
$x_i \geq 0 \Rightarrow \sum x \geq 0$ <br/>
which contradict with the equation, therefore this system have no linear solution <br/>

Infeasible  :
$y=(2,3,4)^T$ certificate it gives an quick proof that LP is Infeasible

Proprieties : <br/>
The system $Ax=b,x\geq 0$ is Infeasible if there exists
a vector y such that <br/>
$y^T A \leq 0^T , y^Tb\gt 0$ <br/>
$y^T A \geq 0^T , y^Tb\lt 0$ <br/>
**Proof** <br/>
suppose $Ax=b,x\geq 0$ has a feasible solution X <br/>
$Ax=b$ <br/>
multiply both sides by $y^T$, we have 
$y^TAx=y^Tb$ <br/>
since $y^TA\geq 0 \And x\geq 0$ , we get $y^TAx\geq 0$, 
but $y^Tv \lt 0$, this is a contradiction therefore the 
system is infeasible <br/>


*strict inequality is bad for optimization*  <br/>
max $x$ <br/>
subject to  <br/>
$x<1$  <br/>
there can never be a solution for that optimization problem  

Is the converse true? <br/>
Yes, we will prove this later as Farkas' Lemma  <br/>
Later we will find out how to find y

#### Unbounded linear programs

$\max x$ <br/>
Subject to $x\geq 1$  <br/>
make the objective value as large as possible

**Definition** <br/>
A maximization linear program is unbounded if 
there exists a series of feasible solutions $x(t)$ 
with (parameter t) such that the objective value 
of $x(t)$ approach $\infin$ as $t\rightarrow\infin$

**example**
$$
    \max\ \ (-1,2,-3.4)x \\
    s.t. \\
    \begin{pmatrix}
    3 & 0 & 2 & -5 \\
    -2 & 3 & -4 & 4 \\
    \end{pmatrix} x
    = \begin{pmatrix}
    4 \\
    1
    \end{pmatrix} \\
x \geq 0
$$
consider vectors $\overline x=(3,1,0,1)^T$ and 
$d=(0,4,5,2)^T$ <br/>
Define $x(t)+t\cdot d, t\geq 0$
1. Feasibility  $x(t)\geq 0$ since $\overline x,d\geq 0$ and
$t\geq 0$. <br/>
$Ax(t)=A(\overline x+td)+t\cdot (Ad)$
$$
    \begin{pmatrix}
    3 & 0 & 2 & -5 \\
    -2 & 3 & -4 & 4 \\
    \end{pmatrix} \cdot (3,1,0,1)^T
    + t\cdot \begin{pmatrix}
    3 & 0 & 2 & -5 \\
    -2 & 3 & -4 & 4 \\
    \end{pmatrix} \cdot (0,4,5,2)^T \\
    = (4,1)^T + t \cdot (0,0)^T=(4,1)^T=b
$$
Notice: $A\overline x=b$ $\overline x$ is one solution
, $Ad=0$
2. Objective value  
$C^Tx(t)=C^T(\overline x+td)$
$=C^T\overline x +tC^Td$ <br/>
$=(-1,2,-3,4) (3,1,0,1)^T + (-1,,2,-3,4)(0,4,5,2)^T$ <br/>
$=3+t$ <br/>
$as\ t\rightarrow \infin,3+t\rightarrow \infin$ <br/>
**Our linear program is unbounded.**
