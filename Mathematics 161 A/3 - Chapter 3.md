---
tags:
  - math161a
---
## 3.1, 3.2 - Random Variables (rv)

> [!info] Definition
> For a given sample space $S$ of an experiment, a rv $X$ is a function that assigns every outcome in $S$ to exactly $1$ real number

![[rv|500]]

> [!example] Example 6
> Left ($L$), Right ($R$), Straight ($A$)
> Experiment terminates when car turns left
> Let $X=$ the number of cars observed
> Possible $X$ values?
> * The set of possible $X$ values is $\{1,2,3,4,…\}$
> * Outcomes/$X$ values
> 	* $L;21$
> 	* $AL,RL;2$
> 	* $RAL,RRL,ARL,AAL;3$
> * 

> [!tip] Notation
> $X,Y,Z,U,V$ are random variables
> $x,y,z,u,v$ are the values of the random variables
### Bernoulli Random Variables

> [!info] Definition
> A rv that has only 2 possible values

> [!Example]
> Flip a coin once
> * $X=\{^{1,Head}_{0,Tail}$
### Discrete Random Variable

> [!info] Definition
> A rv $X$ is discrete if its set of possible values is finite or countable infinite

#### Probability Distribution

> [!info] Definition
> The probability distribution or the probability mass function (pmf) of a discrete rv $X$ is the function $p_X(x)=P(X=x)$ for any real number $x$

> [!warning]
> $\sum\limits_xp_X(x)=1$

> [!example]
> Find the pmf: 
> 
> | $x$ | 2 | 5 | -10 | otherwise |
> | ---- | ---- | ---- | ----------- | -- |
> | $p_X(x)$ | $\frac{3}{36}=\frac{1}{12}$ | $\frac{18}{36}=\frac{1}{2}$ | $\frac{15}{36}=\frac{5}{12}$ | 0 |
> $p(x)=\{^{\frac{1}{12},x=2}_{…}$

> [!example] Example 12
> 1. $P(y\leq50)=1-P(y>50)=1-0.17=0.83$
> 2. $P(y>50)=0.17$
> 3. $P(y\leq49)=P(y\leq50)-P(y=50)=0.83-0.17=0.66$
> 4. $P(y\leq47=0.27)$

> [!example]
> The pmf of a rv $X$ (probability distribution)
> 
> | $x$ | $0$ | $1$| $2$ | otherwise |
> | ---- | --- | --- | ---- | ---------- |
> | $p(x)$ | $.5$ | $.3$ | $.2$ | 0 |
> The graph of the pmf
> * Histogram $\Rightarrow$ ![[histogram1|250]]

#### The Cumulative Distribution Function (cdf)

> [!info] Definition
> Let $X$ be a discrete rv with the pmf $p(x)$ and the set of possible values $D$. The cdf of $X$, denoted by $F(x)$, is the function $F(x)=P(X\leq x)=\sum\limits_{y\leq x}p(y)$, where $x$ is any real number

> [!example]
> 
> | $x$ | 0 | 1 | 2 | otherwise |
> | - | - | - | - | - |
> | $p(x)$ | .5 | .3 | .2 | 0 |
> $F(0)=P(X\leq0)=p(0)=.5$
> $F(1)=P(X\leq1)=p(0)+p(1)=.8$
> $F(2)=P(X\leq2)=p(0)+p(1)+p(2)=1$

> [!example] Example 18
> ![[line1]]

> [!info] Proposition
> Let $X$ be a discrete rv with the cdf $F(x)$. Then for any real numbers $a$ and $b$ with $a\leq b$,
> $P(X\leq b)=F(b)$
> $P(a\leq X\leq b)=F(b)-F(a^-)$ where $a^-$ is the largest possible value of $X$ that is less than $a$

> [!example] Example 18 (continued)
> $P(3\leq M\leq6)=p(3)+p(4)+p(5)+p(6)$
> $P(3\leq M\leq6)\neq F(6)-F(3)$
> $P(3\leq M \leq6)=F(6)-F(2)=1-\frac{1}{9}=\frac{8}{9}$
> $P(3<M\leq6)=F(6)-F(3)=1-\frac{1}{4}=\frac{3}{4}$
> $P(4<M)=1-P(M\leq3)=1-F(3)=1-\frac{1}{4}=\frac{3}{4}$

## 3.3 - Expected Values

 > [!info] Definition
 > Let $X$ be a discrete rv with the $pmf$ $p(x)$ and the set of possible values $D$
 > The expected value of $X$, also known as the mean of $X$ is the following number $E(x)=\mu_x=\sum\limits_{x\in D}xp(x)$ provided that the sum exists
 
 > [!example] Example Game
 > Roll a fair six faced die
 > Let $X=$ profit/loss per game
 > 
 > | outcome | $x$ | $p(x)$ |
 > | ---------- | --- | -------- |
 > | $1,2,3,4$ | $-3$ | $\frac{4}{6}=\frac{2}{3}=.667$ |
 > | $5,6$       | $+6$ | $\frac{1}{3}=.333$ |
 > $E(X)=-3(\frac{2}{3})+6(\frac{1}{3})=0$
 > Play the game 100 times
 > 
 > | outcome | count | relative freq. | $x$ |
 > | ---------- | ------ | ------------- | ----- |
 > | $1,2,3,4$ | $68$ | $.68$ | $-3$ |
 > | $5,6$       | $32$ | $.32$ | $+6$ |
 > Loss/profit per game:
 > $\frac{-3(68)+6(32)}{100}=-3(.68)+6(.32)=-.12$
 > $E(x)$ is the long-run average value of $X$ when the experiment is performed repeatedly
 
 