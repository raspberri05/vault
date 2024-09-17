---
tags:
  - math161a
---
## 3.1, 3.2 - Random Variables (rv)

> [!info] Definition
> For a given sample space $S$ of an experiment, a rv $X$ is a function that assigns every outcome in $S$ to exactly $1$ real number

![[rv|500]]

>[!example] Example 6
>Left ($L$), Right ($R$), Straight ($A$)
>Experiment terminates when car turns left
>Let $X=$ the number of cars observed
>Possible $X$ values?
>* The set of possible $X$ values is $\{1,2,3,4,...\}$
>* Outcomes/$X$ values
>	* $L;21$
>	* $AL,RL;2$
>	* $RAL,RRL,ARL,AAL;3$
>* 

>[!tip] Notation
>$X,Y,Z,U,V$ are random variables
>$x,y,z,u,v$ are the values of the random variables
### Bernoulli Random Variables

>[!info] Definition
>A rv that has only 2 possible values

>[!Example]
>Flip a coin once
>* $X=\{^{1,Head}_{0,Tail}$
### Discrete Random Variable

>[!info] Definition
>A rv $X$ is discrete if its set of possible values is finite or countable infinite

#### Probability Distribution

>[!info] Definition
>The probability distribution or the probability mass function (pmf) of a discrete rv $X$ is the function $p_X(x)=P(X=x)$ for any real number $x$

>[!warning]
>$\sum\limits_xp_X(x)=1$

>[!example]
>Find the pmf: 
>
>| $x$ | 2 | 5 | -10 | otherwise |
>| ---- | ---- | ---- | ----------- | -- |
>| $p_X(x)$ | $\frac{3}{36}=\frac{1}{12}$ | $\frac{18}{36}=\frac{1}{2}$ | $\frac{15}{36}=\frac{5}{12}$ | 0 |
>$p(x)=\{^{\frac{1}{12},x=2}_{...}$

>[!example] Example 12
>1. $P(y\leq50)=1-P(y>50)=1-0.17=0.83$
>2. $P(y>50)=0.17$
>3. $P(y\leq49)=P(y\leq50)-P(y=50)=0.83-0.17=0.66$
>4. $P(y\leq47=0.27)$
















