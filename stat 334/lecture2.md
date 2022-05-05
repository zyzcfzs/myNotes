# Lecture 2
### recaps
$\Omega $ = sample space <br/>
P is an event satisfing two axioms <br/>
with $p(\Omega) = 1, p(\empty) = 0$ <br/>
if $A\cap B=\empty, P(A \cup B) = P(A) + P(B)$ <br/>
how do we add up two events <br/>
$P(A \cup B) = P(A) + P(B) - P(A \cap B)$ <br/>
$$
P(a1\cup a2 \cup a3 \cup a4)
= 
p(a1) + p(a2) .. p(a4)
- p( a1 \cap a2 )  - ... p( a3 \cap a4)  
+ p( a1 \cap a2 \cap a3 )  - ...
P(a1\cap a2 \cap a3 \cap a4)
$$
final answer <br/>
$1 - { 4 \choose 2 } \times \frac {1} {12} ,
{ 4 \choose 3 } \times \frac {1} {24 } ... $
as n approach $\infin$ 
the probability will be
$1 - \frac 1 e $
### conditional probability
two event A and B <br/>
$P(A) = $ unconditional probability <br/>
we have the info that event B happened <br/>
$P(A | B) =$ probability of A given that B occurred <br/>
* conditional probability help us update our beliefs on logical way
* solving complicated problem is easier
* foundation of bayersian statistics

###### $P(A|B) = \frac {P(A \cap B)}{ P(B)}$
> example
>> Two card is  drawn without replacement from the deck one by one
>> A is the event that first card is a heart
>> B is the event that second card is red <br/>
>> Try to get $P(A|B), P(B|A)$
to get $P(A|B)$, we need to get $P(A\cap B) = \frac { 13} {52} \times \frac { 25 } { 51} $
$P(B) = \frac 1 2$
$P(A|B) =  \frac {\frac { 13} {52} \times \frac { 25 } { 51} } { 0.5 } = \frac { 25 } { 102}$ <br/>
$P(B|A) =  \frac {\frac { 13} {52} \times \frac { 25 } { 51} } { 0.25 } = \frac { 25 } { 51 }$ <br/>
the probability of p(a|b) and p(b|a) canbe calculated and they normally not equal <br/>
**the sequence of event does not matter, the information we have is**

**conditional probability are probabilities and it follow all the laws of probability**


> example
$p(a^ \complement) = 1 - p(a)$
$p(a^ \complement | b ) = 1 - p(a|b)$
$p(a \cup b|c) = p(a | c) + p(b|c) - p(a \cap b|c)$ <br/>

> example
suppose we have two coins, one is unbiased coin, the other is 
a biased coins with probability of a head to be a third, we toss it three times, find the probaility of the three tosses are all heads <br/>
event a = all three tosses are heads
p(A) = ?
event b1 first coin is selected
event b2 second coin is selected <br/>
$P(A) = P(A|B1) * P(B1) + P(A|B2) P(B2)$
$(1/2)^ 3 \times 1/2 + ( 3/4) ^ 3 \times 1/2$

> Monte Hall Problem
