In the roll of a die, find the probability of having 2 or 5:
- $A$ = roll the die, get 2
- $B$ = roll the die, get 5
$$
P(A\cup B) = P(A)+P(B)-P(A\cap B)
$$
Here, $P(A\cap B)=0$ because a dice cannot be thrown as both 2 and 5 at the same time. So: $$
P(A\cup B) = P(A)+P(B)=\frac{1}{6}+\frac{1}{6}=\frac{1}{3}
$$
### Conditional Probability

The probability that event $A$ happens if we already know that event $B$ happens then the probability of $A$ given $B$ is: $$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$
This also has a consequence that: the probability of $A$ and $B$ is: $P(A\cap B)=P(B)*P(A|B)$ this is the chain rule.
### Example

Box I contains 3 red and 2 blue marbles while Box II contains 2 red and 8 blue marbles. A fair coin is tossed. If the coin comes up heads, a marble is chosen from Box I; if it comes up tails, a marble is chosen from Box II. Find the probability that a red marble is chosen.

$R$: choosing a red marble
$I$: from box 1
$II$: from box 2

FIL INNN

### Dependence and Independence

Events can occur independently, the occurrence of one event is not dependent on the occurrence of another. The mathematical definition: two events are independent iff: $$
P(A\cap B)=P(A)*P(B)
$$
Another, equivalent formulation:
If two events $(A,B)$ are independent, that means the probability of event $A$ will not change given event $B$ happens: $$
P(A|B)=P(A)\implies P(A)=\frac{P(A\cap B)}{P(B)}\implies P(A\cap B)=P(A)*P(B)
$$
### Bayes' Theorem

Conditional probability represents probability of an event given a condition, a condition happens then an event happens.

Other scenario: An event happens $(B)$, we want to determine the probability of the occurrence of a condition $(A)$. Bayes' theorem computes the probability of a condition, given an outcome: $$
P(A|B)=\frac{P(B|A)*P(A)}{P(B)}
$$
We also call $P(A)$ the $prior$ probability, $P(A|B)$ the $posterior$ probability, $P(B|A)$ the $likelihood$ and $P(B)$ the $evidence$: $$
Posterior = \frac{Likelihood*Prior}{Evidence}
$$
### Example

![[Pasted image 20251010124015.png]]

$P(H)$: probability of high contamination
$P(F)$: probability of failure $$
P(F)=P(F\cap H)+P(F\cap \bar{H})
$$



