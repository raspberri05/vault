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
#### Union

> [!info] Definition
> The union of events $A$ and $B$, $A \cup B$, read as "$A$ or $B$", is the set of all outcomes $S$ that are in $A$ or $B$  or in both $A$ and $B$
#### Intersection

> [!info] Definition
> The intersection of events $A$ and $B$, represented by $A \cap B$ read as "$A$ and $B$", is the set of all outcomes that are in both $A$ and $B$
$
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

Consider an experiment with equally likely outcomes

The sample space $S is always finite

Let $A$ be an event

$P(A)$ = # outcomes in $A$ / # outcomes in $B$
### Textbook Example 18

5 $10 bills, 4 $5 bills, 6 $1 bills

If the bills are selected one by one in random order, what is the probability that at least two bills must be selected to obtain a first $10 bill?

$P($the first bill is not $10) = $\frac{10}{15} = \frac{2}{3}$

