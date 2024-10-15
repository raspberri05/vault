## 4.1 - Probability Density Function

> [!info] Definition
> A $rv$ $X$ is continuous if its set of possible values forms an interval or a union of intervals on a number line and the $P(X=$ a number$)=0$

> [!info] Definition
> The probability distribution (also known as the probability density function, $pdf$) of a continuous $rv$ $X$ is the function that satisfies the following
> 1. $f(x)\geq0$ for any $x$
> 2. $\int_{-\infty}^{\infty}f(x)dx=1$
> 3. For any real numbers $a$ and $b$ with $a\leq b$ 
> $$P(a\leq X\leq b)=\int_{a}^{b}f(x)dx$$
> $$P(X=a)=\int_{a}^{a}f(x)dx=0$$
> $$P(a\leq X\leq b)=P(a<X<b)$$
### Uniform Distribution

> [!info] Definition
> A $rv$ $X$ has a uniform distribution with parameters $A$ and $B$ if the $pdf$ of $X$ is 
> $$f(x;A,B)=\{^{\frac{1}{B-A},\:A\leq X \leq B}_{0,\:otherwise}\}$$
> $$X\sim U[A,B]$$

> [!example] Example 2
> Given: $X=$ the reaction temperature
> $$X\sim U[-5,5]$$
> 1. $P(X<0)$
> 	* $\int_{-5}^{0}\frac{1}{10}dx=1/2$
> 1. $P(-2.5\leq X\leq2.5)$
> 	* $\int_{-2.5}^2.5\frac{1}{10}dx=.5$
> 1. $P(-2\leq X\leq3)$
> 	* $\int_{-2}^3\frac{1}{10}dx=.5$

> [!example] Example 6
> The actual tracking weight of a stereo cartridge that is set to track at $3$g on a particular changer can be regarded as a continuous $rv$ $X$ with $pdf$
> $$f(x)=\{^{k[1-(x-3)^2]\:\:2\leq x\leq4}_{0 \:\:otherwise}\}$$
> 1. Sketch the graph of $f(x)$
> $$f(x)=\{^{\frac{3}{4}(1-(x-3)^2)\:\:2\leq x\leq4}_{0 \:\:otherwise}\}$$
> 2. Find the value of $k$
> 	* $\int_2^4k(1-(x-3)^2)dx=1$
> 	* $k\int_2^4(1-(x-3)^2)dx=1$
> 	* $k(x|^4_2-\frac{(x-3)^3}{3}|^4_2)=1$
> 	* $k(2-(\frac{1}{3}-\frac{(-1)^3}{3}))=1$
> 	* $k(2-\frac{2}{3})=1$
> 	* $k*\frac{4}{3}=1$
> 	* $k=3/4$
> 3. What is the probability that the actual tracking weight is greater than the prescribed weight?
> 	* $P(X>3g)=\frac{1}{2}$
> 4. What is the probability that the actual weight is within .25g of the prescribed weight?
> 	* $|x-3|<.25$
> 	* $P(2.75 <X<3.25)=$
> 	* $=2\int_{2.75}^{3}\frac{3}{4}(1-(x-3)^2)dx$
> 	* $=\frac{3}{2}(.25)-\frac{(x-3)^3}{3}|_{2.75}^{3}$
> 	* $=\frac{3}{2}(.25-(0-\frac{(-.25)^3}{3}))$
> 	* $=.3670$
> 5. What is the probability that the actual weight differs from the prescribed weight by more than .5g?
> 	* $|X-3|>.5$
> 	* $P(X<2.5$ or $X>3.5)=2\int_2^{2.5}\frac{3}{4}(1-(X-3)^2)dx$
> 	* $=\frac{3}{2}(x|_2^{2.5}-\frac{(X-3)^3}{3}|_2^{2.5})$
> 	* $=.3125$

## 4.2 - Cumulative Distribution and Expected Values

>[!info] Definition
>The cumulative distribution function of a $rv$ $X$ with the $pdf$ $f(x)$ is 
>$$F(x)=P(X\leq x)=\int_{-\infty}^{\infty}f(t)dt$$for any real $x$

### Uniform Distribution

>[!info] Definition
>$$X\sim U[A,B]$$
>$$F(x;A,B)=\{^{\frac{1}{B-A},\:A\leq x \leq B}_{0,\:otherwise}\}$$
>If $x<A,\:then\: F(x;A,B)=0$
>If $A\leq x \leq B,\:F(x;A,B)=\int_A^x f(t;A,B)dt$
>If $x\geq B,\:then\: F(x;A,B)=\int_A^B f(t;A,B)dt=1$

>[!example] Example 20
>1. Compute and sketch the $cdf$ of Y
>	* $y<0\Rightarrow F(y)=0$
>	* $0\leq y <5 \Rightarrow F(y)=\int_0^y\frac{1}{25}tdt=\frac{t^2}{50}|^y_0=\frac{y^2}{50}$
>	* $5\leq y <10 \Rightarrow F(y)=\int_0^y f(t)dt$
>	* $=\int_0^5\frac{1}{25}tdt+\int_5^y(\frac{2}{5}-\frac{1}{25}t)dt$
>	* $=...=\frac{1}{2}+\frac{2}{5}y-2=\frac{-y^2}{50}+\frac{1}{2}$
>	* $\frac{2}{5}y-\frac{-y^2}{50}-1$
>	* $y\geq 10 \Rightarrow F(y)=1$

>[!info] Proposition
>If $X$ is a $rv$ with the $pdf$ $f(x)$ and the $cdf$ $F(x)$, then $$F^1(x)=f(x)$$ at every $x$ at which $F^1$ exists
>Note: let $a,\:b$ be real numbers, $a<b$
>$$P(a\leq X \leq b)=F(b)-F(a)$$
>$$P(a<X)=1-F(a)$$
### Percentiles

>[!info] Definition
>let $0<p<1$
>The $(100p)^{th}$ percentile of the distribution of a $rv$ $X$ with the $pdf$ $f(x)$ and the $cdf$ $F(x)$ is the number
>$$\eta(p)$$ is the number such that $$F(\eta(p))=p=\int_{-\infty}^{\eta(p)}f(x)dx$$
>The median $\tilde{\mu}$ is the $50^{th}$ percentile
>$$\tilde{\mu}=\eta(.5)$$

>[!example] Example 20
>2. Obtain an expression for the $(100p)^{th}$ percentile
>	* $0<p<.5\Rightarrow p=\frac{y^2}{50}\Rightarrow y=\sqrt{50p}=5\sqrt{2p}$
>	* $\eta(p)=5\sqrt{2p}$
