# Lecture 6

> Roadmap
> 1. recap
> 2. $E(X)$ and $VAR(X)$
> 3. independence of random variable
> 3. Bernoulli distribution  


**propriety of expectations**
- Linearity   $E(X+Y)=E(X)+E(Y)\ \forall r.v.\ X,Y$ <br/>
average of  the sum = sum of a average <br/>
*Note* this result does not dependent on whether X and Y
are independent or not

| x | f   |
|---|-----|
| 0 | 0.3 |
| 1 | 0.5 |
| 2 | 0.2 |

- $E[g(x)]=\sum_{x}g(x)f(x)$ <br/>
example 
$E(x^3)=0^3\cdot0.3+1^3\cdot0.5+2^3\cdot 0.2$ <br/>
*Note No need to find the PMF of $g(x)$*

Example
| x | f   |
|---|-----|
| 1 | 1/3 |
| 0 | 1/3 |
| 1 | 1/3 |
$E(x^2)=-1^2\times \frac 1 3+1^2\times \frac 1 3$

#### Variance and standard deviation 
$Var(x)=E(x-E(x)]^2$
$Sd(x)=\sigma=|\sqrt{Var(x)}|$

**Propriety**  
1. $Var(K)=0$ where K is a constant
2. $Var(x)=E(x^2)-E(x)^2$
3. $Var(aX+b)=a^2\times Var(x)$
4. $Var(x+y)=Var(x)+Var(y)$ if X and Y are independent

**Independence of random variables** 
X and Y are independent random variables, if $P(X=x,Y=y)= P(X=x)\times P(Y=y)\ \ \forall x,y$

> example
> roll of a fair dice are X is the face of the first dice and Y is the face of the second dice <br/>
> Find if X+Y, X-Y are independent 
> Counterexample  
> $P(X+Y=12,X-Y=2)\ne P(X+Y=12)+P(X-Y)$

**independent and identically distributed** 
Independence and identically distributed random variable are two different thing.
#### Distributions
**Bernoulli distribution**
- Support
- PMF
- $E(X)\And Var(X)$

*Definition*
X is a Bernoulli distribution if $X=\{0,1\}, X \backsim Ber(p)$ 
| x | f   |
|---|-----|
| 0 | 1-p |
| 1 | p   |

$E(X)=0\times (1-p)+1\times p=p$
$Var(X)=E(X^2)-E(X)^2=p-p^2=p(1-p)$

Importance of Bernoulli distribution
- gateway to other Distributions 
- indicator variables and transition bridge

Indicator  

| $I_A$ | g   |
|---|-----|
| 0 | $1-P(A)$ |
| 1 | $P(A)$   |

Therefore 
$E[I_A]=P(A)$ transition bridge 

