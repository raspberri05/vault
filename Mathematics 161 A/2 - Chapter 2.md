---
tags:
  - math161a
---

## 2.1 - Sample Spaces and Events

### Sample Space

> [!info] Definition
> The collection of all outcomes of an experiment, represented by $S$

> [!example]
> * Roll a die twice, $S = \{(1,1),(1,2),…,(6,6)\}$
> * Flip a coin until you get heads, $S = \{H,TH,TTH,TTTH,…\}$

### Event

> [!info] Definition
> An event $E$ of an experiment is a subset of the sample space $S$ of the experiment

> [!example]
> * Experiment: toss a die twice
> 	* $S=\{(1,1),(1,2),…,(6,6)\}$
> 	* Event: getting a double
> 		* $E=\{(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)\}$
> * Experiment: flip a coin until two heads are obtained (not necessarily consecutively)
> 	* $S=\{HH,THH,TTHH,…\}$
> 	* Event A: the coin is tossed 4 times
> 		* $A=\{HTTH,THTH,TTHH\}$

> [!tip]
> Event $E$ has occurred if the resulting outcome  is in $E$
#### Simple

Only one outcome
#### Compound

More than one outcome
#### Null

Event with no outcomes
### Set Operations

#### Complement

> [!info] Definition
> The complement of event $A$, $A^1$, is the set of all outcomes in the sample space $S$ that are not in $A$
> ![[complement]]
#### Union

> [!info] Definition
> The union of events $A$ and $B$, $A \cup B$, read as "$A$ or $B$", is the set of all outcomes $S$ that are in $A$ or $B$  or in both $A$ and $B$
> ![[union]]
#### Intersection

> [!info] Definition
> The intersection of events $A$ and $B$, represented by $A \cap B$ read as "$A$ and $B$", is the set of all outcomes that are in both $A$ and $B$
> ![[intersection]]
#### Mutual Exclusivity

> [!info] Definition
> $A$ and $B$ are disjoint or mutually exclusive if $A \cup B = \emptyset$
#### Pairwise Disjoint

> [!info] Definition
> $A_1,A_2,A_3,…$ are mutually exclusive or pairwise disjoint if for any $i \neq j$, $i,j=1,2,3,…$, $A_{i} \cap A_{j} = \emptyset$

> [!example]
> * Experiment: roll the die twice
> 	* Events
> 		* $A_1$: getting a sum of 7 dots
> 			* $A_1=\{(1,6),(6,1),(2,5),(5,2),(3,4),(4,3)\}$

### Textbook Exercise 8

* Let $A_i$ denote the event that the plant at site $i$ is completed by the contract date
* Events: $A_1,A_2,A_3$
* At least one plant is completed by the contract date
	* $A_{1}\cup A_{2}\cup A_3$
* All plants are completed by the contract date
	* $A_{1} \cap A_{2}\cap A_3$
* Only the plant at site 1 is completed by the contract date
	* $A_{1}\cap A_2^1\cap A_3^1$
* Exactly one plant is completed by the contract date
	* $(A_1 \cap A_2^1 \cap A_3^1) \cup (A_1^1 \cap A_2 \cap A_3^1) \cup (A_1^1 \cap A_2^1 \cap A_3)$
*  Exactly the plant at site 1 or both of the other two plants are completed by the contract date 
	* $A_1 \cup (A_2 \cap A_3)$

## 2.2 - The Axioms and Properties of Probability

The probability of event $A$, $P(A)$ is a measure of chance that event $A$ will occur
### The Three Axioms

1. For any event $A, P(A) \geq 0$
2. $P(S)=1$
3. Let $A_1,A_2,A_3,…$ be an infinite collection of pairwise disjoint events
	* Then, $P(A_1,A_2,A_3,…) = P(A_1) + P(A_2) + P(A_3) + …$
### Properties

1. $P(\emptyset) = 0$
2. Let $A_1,A_2,…,A_n$ be pairwise disjoint events
	* Then $P(A_1 \cup … \cup A_n) = P(A_1) + P(A_2)$
3. For any event $A, P(A) + P(A^1) = 1$ or $P(A)=1-P(A^1)$

> [!example]
> * Roll a fair die twice. What is the chance that the sum of the dots will be at least 4?
> 	* $A=\{(1,3),(3,1),(2,2),…\}$
> 	* $A^1=\{(1,1),(1,2),(2,1)\}$
> 	* $P(A) = 1 - \frac{3}{36} = \frac{11}{12}$

1. For any $A,P(A)\leq1$
2. For any event $A$ and $B,P(A \cup B) = P(A) + P(B) - P(A \cap B)$
3. For any events $A,B,C$, $P(A \cup B \cup C)  = P(A) + P(B) + P(C) - P(A\cap B) - P(A \cap C) - P(B\cap C) + P(A \cap B \cap C)$
### Textbook Example 18

5 $10 bills, 4 $5 bills, 6 $1 bills

If the bills are selected one by one in random order, what is the probability that at least two bills must be selected to obtain a first $10 bill?

$P($the first bill is not $10) = $\frac{10}{15} = \frac{2}{3}$

### Textbook Example 26

Let $A_i(i = 1,2,3)$

* What is the probability that the system does not have a type 1 defect?
	* $P(A_1^1) = 1 - P(A_1) = 0.88$
* What is the probability that the system has both type 1 and type 2 defects?
	* $P(A_1 \cap A_2) = P(A_1) + P(A_2) - P(A_1 \cup A_2)=0.06$
* What is the probability that the system has both type 1 an type 2 defects but not a type 3 defect?
	* $P(A_1 \cap A_2 \cap A_3^1) = P(A_1 \cap A_2) - P(A_1 \cap A_2 \cap A_3) = 0.05$
* What is the probability that the system has at most two of these defects?
	* $P($at most 2 defects) = $1-P($all three defects)
	* $1 - .01 = 0.99$ 
* Probability of at least one defect?
	* $P($at least one defect) $=P(A_1 \cup A_2 \cup A_3) =$ *use property 6*
### Relative Frequency Approach to Probability

Consider an experiment that can be repeated $n$ times in and identical and independent fashion.

> [!info] Definition
> The relative frequency of event $A$, is$f_n(A)=$ # of time $A$ occurs / $n$ 
> $f_n(A) =$ a limit value as $n \rightarrow \infty$
> $P(A)$ is the limiting value

## 2.3 - Counting Techniques

### The Product Rule

> [!info] Definition
> Suppose an experiment or procedure consists of $k$ steps, and there are
> $n_1$ ways to complete step $1$,
> $n_2$ ways to complete step $2$
> .
> .
> .
> $n_k$ ways to complete step $k$
> Then, there are $n_1 * n_2 * … * n_k$ ways to perform the experiment or complete the procedure

> [!Example]
> Flip a coin and then roll a 6 faced die
> 1. Flip a coin: $H$ or $T$ (two branches)
> 2. Roll a die $1,2,3,4,5,6$ (each branch from step 1 gets 6 branches)
> 3. Outcomes
> 	* $H1,H2,H3,…,H6$
> 	* $T1,T2,T3,…T6$
> 	* $2*6=12$
#### Textbook Example 32

Receiver: Kenwood, Onkyo, Pioneer, Sony, Sherwood (5)
Compact disk player: Onkyo, Pioneer, Sony, Techniques (4)
Speakers: Boston, Infinity, Polk (3)
Turntable: Onkyo, Sony, Teac, Techniques (4)

* In how many ways can one component of each type be selected?
	* $5*4*3*4 = 240$
* In how many ways can components be selected if both the receiver and compact disk player are to be Sony?
	* $1*1*3*4=12$
* In how many ways can components be selected if none is to be Sony?
	* $4*3*3*3=108$
* In how many ways can a selection be made if at least one Sony component is to be included?
	* All selections - selections without Sony $=240-108=132$
* If someone flips switches on the selection in a completely random fashion, what is the probability that the system selected contains at least one Sony component?
	* $P($at least one Sony$)=\frac{132}{240}$
	* Exactly one Sony component?
		* $P($exactly one Sony$)=\frac{1*3*3*3 + 4*1*3*3 + 4*3*3*1}{240}$
### Permutations

> [!info] Definition
> Let $0<k\leq n$, $k,n$ are integers
> A $k$-permutation of a set of $n$ distinct objects (elements) is an **ordered** selection of $k$ objects of the set
> $P_{k,n} =$ the number of $k$-permutations of $n$ elements
> It can be shown that $P_{k,n}=n(n-1)…(n-k+1)=\frac{n!}{(n-k)!}$
> $P_{n,n}=n!$

> [!example]
> $n=7$, $k=3 \Rightarrow \{a,b,c,d,e,f,g\}$
> Some 3-permutations: $abc,cab,bca,bfe$
> $P_{3,7}=7*6*5=7*6*5*\frac{4!}{4!} = \frac{7!}{(7-3)!}$

#### Textbook Example 30

A combination lock with 4 digits 0-9
Find the # of non-repetitive combinations $\Rightarrow \frac{10!}{6!}=10*9*8*7$

### Combinations

> [!info] Definition
> A $k$-combination of a set of $n$ distinct elements is subset of $k$ elements of the set
> $C_{k,n}=$ The # of $k$-combinations of $n$ elements
> $(^n_k)$
> $C_{k,n} = \frac{P_{k,n}}{k!}=\frac{n!}{(n-k)!*k!}$



> [!example]
> $\{a,b,c,d,e,f,g\},n=7,k=3$
> Some 3-combinations: $\{a,b,c\}=\{b,c,a\}$
> Permutations: $abc,bca,…,cba\Rightarrow 3!=6$
> $C_{3,7}=\frac{P_{3,7}}{3!}=\frac{7!}{(7-3)!*3!}$




