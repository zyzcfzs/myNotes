# Lecture 7

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

$\sum_{e\in \delta(W)} x_e\geq 1,\forall s,t-cuts \delta(W)$

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

A certificate  indicate our result is correct, so our algorithms  terminates

Possible outcome for linear program:
1. Infeasible
2. feasible but unbounded 
3. feasible and bounded

*example Infeasible linear programs* <br/>
$max 3x_1+x_2-7x_3+4x_4$ <br/>
subject to:  <br/>
$e1: -5x_1+4x_2+3x_3-x_4=3$ <br/>
$e2: 2x_1+x_2-5x_3+3x_4=-2$ <br/>
$e3: -x_1-3x_2+x_3-2x_4=1$

Solution : <br/>
$e1 \times 2 +e2 \times3+e3 \times 4$ <br/>
$-8x_1-x_2-5x_3-x_4=4$
Infeasible  :
$y=(2,3,4)^T$ certificate it gives an quick proof that LP is Infeasible

Proprieties : <br/>
The system $Ax=b,x\geq 0$ is Infeasible if there exists
a vector y such that <br/>
$y^T A \leq 0^T , y^Tb\gt 0$ <br/>
$y^T A \geq 0^T , y^Tb\lt 0$
**proof** <br/>
suppose $Ax=b,x\geq 0$ has a feasible solution x <br/>
$Ax=b$ <br/>
$y^TAx=y^Tb$ <br/>
$\geq 0 <0$
 so it must be Infeasible

Is the lemma true  
does that always exists an certificate for an Infeasible linear program.
yes Farkas lemma
