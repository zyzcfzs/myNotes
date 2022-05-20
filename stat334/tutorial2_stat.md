# Tutorial 2 of stat 334

### assignment go through
> question 6
> define $A_1$ = none of the eight people were born in $s_1$
>$A_2$ = none of the eight people were born in $s_2$
>$A_3$ = none of the eight people were born in $s_3$
>$A_4$ = none of the eight people were born in $s_4$  

**Result is $1 - p(A_1\cup A_2\cup A_3\cup A_4)$**

#### Example 
a fair 5 sided dice is rolled twice
define event D = sum is 7
E = difference between the roll is 1
F = second roller have higher number than first  

*is E and F independent?* <br/>
$p(F)=\{12,13,14,15,23,24,25,34,35,45\}$ <br/>
$p(E)=\{12,21,23,32,34,43,45,54\}$ <br/>

$p(F)=\frac {10}{25}$ <br/>
$p(E)=\frac {8}{25}$ <br/>
$p(F|E)=\frac{1}{2} \ne p(F)$

are E and F independent given D <br/>
$P(E\cap F|D)=P(E|D)\cdot P(F|D)$

| X    | f                                   |
|------|-------------------------------------|
| 0    | $0.7^2$                             |
| 400  | $2\times 0.3\times 0.7\times 0.4$   |
| 750  | $2\times0.3\times0.7\times0.6$                                 |
| 800  | ?                                 |
| 1150 | $2\times 0.3^2 \times 0.6 \times 0.4$ |
| 1500 | $0.3^2\times 0.6^2$                                 |

$E(X)=2xf(x)=366$

> Example
> 1 red , 3 blue dice you roll all 4 simultaneously   <br/>
> No blue die matches = lose $1 <br/>
> exact K matches , win $k+1
> exact 1 match, then additional 50 cents for other blue die match

Define x = gross payoff

| X   | f(x)                                  |
|-----|---------------------------------------|
| 0   | $\frac{6\cdot5^3}{6^4}$               |
| 2   | $\frac{6\times3\times5\times4} {6^4}$ |
| 2.5 | $\frac{6\times3\times5}{6^4}$   |
| 3   | $\frac{6\times3\times5}{6^4}$         |
| 4   | $\frac{6}{6^4}$                       |

$E(X)=0.956$
