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
 
 > [!example] Example 32
 > 3 capacities: 16, 18, and 20 $ft^3$
 > Suppose $X$ has $pmf$
 > 
 > | $x$ | 16 | 18 | 20 |
 > | ---- | -- | --- | --- |
 > | $p(x)$ | 0.2 | 0.5 | 0.3 |
 > * Compute $E(x),E(x^2),$ and $V(X)$
 > 	* $E(X)$
 > 		* $16*.2+18*.5+20*.3=18.2ft^3$
 > 		* The expected capacity of a freezer sold at a store 
 > 	* $E(X^2)$
 > 		* $16^2*.2+18^2*.5+20^2*.3=333.2ft^6$
> 	* $V(X)$
> 		* $(16-18.2)^2(.2)+(18-18.2)^2(.5)+(20-18.2)^2(.3)$
> 		* $333.2-18.2^2=1.96ft^6$
> 		* $\sigma=\sqrt{1.96}=1.4ft^3$
> * Price $Pr(X)=70X-650$
> 	* $E(Pr(X))=(16(70)-650.2+(18(70)-650)*.5+(20(70)-650)*.3$
> 	* $E(Pr)=E(70X-650)=70E(X)-650=70(18.2)-650=624$
> * Calculate variance in price
> 	* $V(70X-650)=70^2V(X)=70^2(1.96)=\$^29604$
> 	* $\sigma_{70X-650}=70(1.4)=\$98$
> * Rated capacity is $X$, actual capacity is $h(X)=X-.008X^2$. What is expected actual capacity
> 	* $E(X-.008X^2)=\sum\limits_{x\in \{16,18,20\}}(x-.008x^2)p(x)$
> 	* $=\sum\limits_{x\in \{16,18,20\}} xp(x)-.008\sum\limits_{x\in \{16,18,20\}} x^2p(x)$
> 	* $E(X)-.008E(X^2)=18.2-.008(333.2)=15.5ft^3$

> [!info] Proposition
> If $h(x)$ is a function of rv $X$ with the $pmf$ $p_X(x)$ and the set of possible values $D$, then $E(h(X))=\sum\limits_{x\in D}h(x)p_X(x)$ provided that the sum exists

> [!info] Proposition
> Suppose a rv $X$ has $E(X)$. Let $a,b$ be any real numbers. Then, $E(aX+b)=aE(X)+b$
### Variance

> [!info] Definition
> Suppose rv $X$ with the $pmf$ $p(x)$ and the set of possible values $D$ has the mean $\mu$. The variance of $X$, denoted by by $V(X)$ or $\sigma^2$, is $V(X)=\sigma^2=\sum\limits_{x\in D}(x-\mu)^2p(x)$
> $V(X)=E((X-\mu)^2)$ provided that the sum exists

> [!info] Definition
> The standard deviation of $X$ is $\sigma=\sqrt{\sigma^2}=\sqrt{V(X)}$

> [!info] Proposition
> Let $X$ be a rv with the mean $\mu$ and variance $V(X)$. For any real numbers $a$ and $b$, $V(aX+b)=a^2V(X)$, $\sigma_{aX+b}=|a|\sigma_X$
#### Shortcut Formula

> [!info] Proposition
> for $V(X):$
> $V(X)=E(X^2)-(E(X))^2$

> [!example] Example 36
> 
> | damage | 0 | 1000 | 5000 | 10000 |
> | - | - | - | - | - |
> | chance | .8 | .1 | .08 | .02 |
> $\$500$ deductible policy
> Expected profit should be $\$100$
> What premium should they charge?
> * $Y=$ the payment made per customer
> * | $Y$ | 0 | 500 | 4500 | 9500 |
> | - | - | - | - | - |
> | $p(y)$ | .8 | .1 | .08 | .02 |
> * $E(Y)=50+360+190=600$
> * Premium should be $600+100=\$700$

## 3.4 - The Binomial Probability Distribution
### Binomial Experiment
1. Sequence of $n$ smaller experiments called trials
2. Each trials can result in one of the same two possible outcomes (dichotomous trials) which are denoted as $S$, success, or $F$, failure. The assignment of these variables are arbitrary
3. Trials are independent
4. The probability of success $P(S)$ is constant from trial to trial, we denote this probability as $p$
5. The probability of failure $P(F)$ is constant from trial to trial, we denote this probability as $q=1-p$
The goal of such an experiment is to count the number of successes $X$

> [!example] Examples
> 1. Toss a coin (fair or unfair) 10 times and count the number of heads
> 2. The National Statistics claims that 30% of Americans can raise one eyebrow at a time. Ask any ten people whether they can lift one eyebrow at a time and record the number of those who answer yes

> [!example] Non Examples
> * A deck of 20 cards contains 10 red and 10 black cards
> 	* 5 cards are randomly chosen and the number of red cards is recorded
> * Roll a six faced die until a 6 appears

### Binomial Distribution
> [!example] Definition
> Consider a binomial experiment with $n$ trials where 
> $X=$the number of successes;
> $p=$the probability of a success in a single trial.
> Then $X$ has a binomial distribution and we write
> $$X~Bin(n,p)$$
> More notations
> $b(x;n,p),$ the $pmf$ of $X$
> $B(x;n,p),$ …