This submodule is all about writing code that is particularly performant, C and C++ are useful for this application as they *can* both be incredibly efficient. 

### Pre-processor Directives

When writing C or C++ code, we have lines that start with a # and these are commands used by the C pre-processor for example: $$
\text{\#include <stdio.h>}
$$
This line tells the pre-processor to look for  the source code file $stdio.h$ and include it before any compilation occurs, $stdio.h$ is a file required to use the standard input and output library.

You can also create something like a variable called a symbolic constant using the pre-processor such as: $\text{\#define PI 3.1415}$ This code gives us a variable PI to work with, this can be useful to us for the sake of maintainability, readability and performance. For example if we use $\pi$ in this way we know that absolutely everywhere in the program we will have the same value of $\pi$ and it also has no runtime cost as substitution happens at compile time.

We can also make function like statements called macros, for example: `#define IS_EVEN(n) ((n) % 2 == 0)` This macro allows us to essentially have a function that we can use anywhere and is particularly fast, there's no function call as the code is actually expanded inline at compile time. However, macros do have some disadvantages one of which is the fact that arguments aren't type-checked: When a C function is called, the compiler checks each argument to see if it has the appropriate type. Macro arguments aren't checked by the pre-processor, nor are they converted.



