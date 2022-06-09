# Lecture 5
> Road map
> - recap
> - intro to random variables
> - the expected value and variances and probability mass function
### Random Variable
Random variable X,Y.
- x is a function that maps event to numbers
> example <br/>
> x = number of head you toss a fair coin twice

Discrete random variable <br/>
random variable only take integer value <br/>
continuous variable only take values in an interval  

Probability mass function  
$f(x)=p(X=x)\forall x$

x = number of head in two fair tosses  
f is called the probability mass function of X
$\{HH,HT,TH,TT\} = \{2,1,1,0\}$
> Frequent interpretation  
if the experiment was repeated many times,
$f(x)$ stand for the relevant frequency of x occurring   

> propriety of the Probability mass function   <br/>
$(i)f(x)\geq 0$
$(ii)\displaystyle\sum_{x\in X} f(x) = 1$

>example  
a random bridge card is dealt <br/>
x = the number of aces <br/>
find PMF of X <br/>

Two random variable that have the same Probability mass function
may not equal to each other

### CDF (cumulative distribution function )
**Defintion** <br/>
$F(x)=p(X\leq x), \forall x$

*property of the CDF*

- $0\leq F(x)\leq 1$
- F is non decreasing  $x<y,F(x)\leq F(y)$
- $lim_{x-> -\infin} F(x)=0$
- $lim_{x-> \infin} F(x)=1$
- F is right continuous

Given $f$ and we find $F$ <br/>
$F(x)=\displaystyle\sum_{y\leq x}f(y)$ <br/>
Given $F$ and we find $f$ <br/>
$F(x)=F(x)-F(x-1)$

### expectations E(X) $\mu$ and variance V(x) $\sigma ^ 2$
**Definition**
X is a random variable

$E(X) = \displaystyle \sum_{x\in X}x\cdot f(x)$

> expectation is the weighted value of the probabilities  

### law of expectations
