Probability is based on both the theory of counting and set theory. This can be particularly useful for computer scientists, such as for cryptography when we hash a password we can figure out how long it will take to brute force crack just by using relatively basic combinatorics. 

### Product Rule

If a sequence of tasks $T_{1},T_{2},\dots ,T_{m}$ can be done in $n_{1},n_{2},\dots,n_{m}$ ways, and every task arrives after the occurrence of the last task then there are $n_{1}*n_{2}*\dots*n_{m}$ ways to perform the tasks.

### Sum Rule

If a sequence of tasks $T_{1},T_{2},\dots ,T_{m}$ can be done in $n_{1},n_{2},\dots,n_{m}$ ways, then there are $n_{1}+n_{2}+\dots+n_{m}$ ways to do one of these tasks.

### Permutations

Counting of distinct objects in an ordered arrangement (Ordered arrangement of $r$ elements is called $r$-permutation)

### Practice Question

What is the number of different  
permutations of the 11 letters of the  
word M I S S I S S I P P I, which  
consists of 1 M, 4 I’s, 4 S’s, and 2 P’s?

We use the formula for permutations with indistinguishable elements (ie. $\frac{n!}{n_{1}!n_{2}!\dots n_{k}!}$) So, there are $\frac{11!}{1!4!4!2!} = 34650$ different permutations.

### Set Theory

A set is just a collection of unordered objects, there are 6 basic set operations (Examples with the sets $L$ and $R$):
- Size of set $L$ : $|L|$
- Union: $L \cup R$
- Intersection: $L \cap R$
- Complement: $\bar{L}$
- Subtract: $L-R$
- Subset: $L \subseteq S$
![[Pasted image 20251009104427.png]]

### Terms of probability

- An *experiment* is a procedure that yields one of a given set of possible outcomes. Example: $(a)$ tossing a coin or $(b)$ rolling a die.
- The *sample space* of the experiment is the set of possible outcomes. Example: $(a)$ heads, tails or $(b)$ a number $1,\dots,6$.
- An event is any subset of the sample space. Example: $(a)$ heads or $(b)$ an even number.

- $S$ is a finite sample space of all outcomes ($S$ is a set).
- Assume all outcomes are equally likely.
- E is an event (set) where: $E \subseteq S$.
- Then the probability of the occurrence of event $E$ is:
$$
P(E)=\frac{|E|}{|S|}
$$
### Practice Question 2

What is the probability that a positive integer selected at random from the set of positive integers not exceeding 100 is divisible by 2 or 5?












