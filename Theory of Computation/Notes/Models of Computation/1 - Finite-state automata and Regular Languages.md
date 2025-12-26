A DFA (Deterministic Finite Automata) is a mathematical object that we can use to recognise patterns or decide if a string belongs to a particular language. For example we could create a DFA that will take in an input string made of the alphabet $\sum$ = (0,1) and will determine if it ends with an even number of 0s.

A DFA has 5 properties:
- States $Q$ - finite set of possible conditions.
- Alphabet $\sum$ - finite set of input symbols.
- Transition function $\delta$ - defines what state to go to next, given the current state and an input symbol: $\delta: Q \sum\to Q$.
- Start state $q_{0}$ - where the machine begins.
- Accept states $F$ - a subset of states that means "accept" or "true" when reached.

## Example

If we have the following DFA let's try to define it's 5 properties.
![[Pasted image 20251006151427.png]]
$$
Q = \{q_{1},q_{2},q_{3}\}
$$
$$
\sum = \{0,1\}
$$
$\delta:$

|         | $0$     | $1$     |
| ------- | ------- | ------- |
| $q_{1}$ | $q_{1}$ | $q_{2}$ |
| $q_{2}$ | $q_{3}$ | $q_{2}$ |
| $q_{3}$ | $q_{2}$ | $q_{2}$ |
$q_{1}$ is the $start$ state and $F=\{q_{2}\}$.

This can extend to much more complex examples but I won't put any in here because I think it's more important to just be able to build them myself. However, one thing I do find important is running this DFA on 2 example strings: 0100 and 1010. Let's see how it runs on these two.

for 0100:
$$
q_{1}\to_{0}q_{1}\to_{1}q_{2}\to_{0}q_{3}\to_{0}q_{2} \ (accept)
$$
for 1010:
$$
q_{1}\to_{1}q_{2}\to_{0}q_{3}\to_{1}q_{3}\to_{0}q_{3} \ (reject)
$$
## Regular Languages

The DFA $M$ recognises the language $L$ if $L=\{w|M \ accepts \ w\}$.
A language is called a regular language if some DFA recognises it.

## Regular Operations

We have a set of 6 operations that we can perform on regular languages to produce another regular language these are:

- Union
- Intersection
- Difference
- Complement

- Concatenation
- Kleene Star

The two at the bottom of the list are separated as they are language theory specific the other four are set-theoretic.

### Union ($A \cup B$)

This is just all the strings in $A$ or in $B$.
### Intersection ($A \cap B$)

This is all the strings that are in both $A$ and in $B$.
### Difference  ($A \setminus B$)

This is the strings that are in $A$ but not in B.
### Complement ($\bar{A}$)

This is a bit more tricky its all the strings not in $A$, from all possible strings over the alphabet. For example, if $\sum = \{a,b\}$ and $A=\{\text{"a", "b"}\}$
Then
$\sum^* = \{\epsilon, \text{"a", "b", "aa", "ab", "ba", "bb", ...}\}$ 
$\bar{A} = \{\epsilon, \text{"aa", "ab", "ba", "bb", ...}\}$

### Concatenation ($A\circ B$)

This is the set of all strings created by joining the strings of $B$ to those of $A$. For example,
if $A=\{\text{"a", "b"}\}$ and $B=\{\text{"x", "y"}\}$ 
Then
$A\circ B = \{\text{"ax", "ay", "bx", "by"}\}$

### Kleene Star ($A^*$)

This essentially means repeat words from $A$ any number of times, even zero. So, If $A=\{\text{"ab"}\}$
Then
$A^* = \{\epsilon, \text{"ab", "abab", "ababab", ...}\}$

### Non-deterministic Finite Automaton

The only difference in definition of this compared to a DFA is that the transition function is now: $$
\delta:Q*(\Sigma \cup\{\epsilon\})\to \mathcal{P}(Q)
$$Where $\mathcal{P}(S)$ means the power set of $S$.
This is an example of a NFA:
![[Pasted image 20251013102203.png]]
However, this NFA has 3 potential problems,
- More than 1 next possible state (in $q_{1}$ read 1).
- $\epsilon$-transition (in $q_{2}$, and the next symbol is $0$).
- No "next" state (in $q_{3}$ read $0$): the computation hangs, i.e. ends before the input has been exhausted.

Note: $\epsilon$ is not a letter from the alphabet; it means go straight away to that state and postpone reading the next input symbol.

Note 2: $\epsilon$'s can be freely added inside the actual word $\in$ $\Sigma$*, eg. 010110 can be viewed as: $\epsilon01\epsilon\epsilon 01\epsilon 10$.

So basically, non-deterministic computation just means trying all the possible paths and accept if and only if at least one accepts.

### Converting a NFA into a DFA

Fill this in tonight



### Closure under Regular Operations

Finish writing here






