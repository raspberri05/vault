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
> 1. What is the probability that the actual tracking weight is greater than the prescribed weight?
> 	* $P(X>3g)=\frac{1}{2}$



