## Functions

Every function is a relation, but not every relation is a function. In order to be a function, a relation needs to satisfy **one key constraint:** 

A relation \\(R\\) on a subset of \\(A x B\\) is a function if and only if \\(\forall x \in A\\), there exists a **unique** element \\(y \in B\\) such that \\(xRy\\)

Let's go back to our previous examples. We had a relation,  \\(Table1: \\{(Ife, 200), (Tolu, 150), (Olivia, 150), (Tolu, 100)\\}\\) to capture donations from people. If I were to ask you how much Ife donated, the answer is clear: 200

But if I were to ask you how much Tolu donated, there is more than one singular answer. Tolu maps to two different outputs. This means there isn't a unique element that the value "Tolu" maps to, so this relation is not a function.

How abot \\(R_2: \\{(Tomi, 0), (Edward, 3), (Kwasi, 1), (Afia, 1)\\}\\). It is a function indeed, as each name only appears once.

### Definition of a function:

We define a function \\(f: A \to B\\) such that all elements of \\(A\\) are *uniquely* mapped to some element of \\(B\\)

- The set \\(A\\) is known as the **domain** of the function
- The set \\(B\\) is the function's **codomain**
- We say that \\(f(x)\\) - pronounced "f of x" - is the *image* of the value *x* using function *f*.  It follows that \\(f(x) \in B\\)

Let's consider two functions, *f* and *g*. 

we can define \\(f: \mathbb N \to \mathbb N: f(x) = x^2\\) and \\(g: \mathbb R \to \mathbb R: g(x) = x^2\\)

Both these functions take an input, then raise it to the power of two. However these are different functions - even though they follow the same logic - as their domains and codomains are different. 

This could be clearer if we go back to thinking of sets as relations. The pair (0.1, 0.01) is part of the relation *g*, but is not part of the relation *f* 

### Images of a set:
We can also take images of a set. Let \\(f: A \to B\\) be a function and \\(C \subset A\\)

\\(f(C)\\) represents the set of the images of all elements in C, or in other words: \\(f(C) = \\{f(x) \forall x \in C\\}\\)

\\(f(A)\\) represents the set of images of all the elements of our domain. Note that this does not **necessarily** mean that \\(f(A) = B\\). We can however say that \\(f(A) \subseteq B\\).

## Interesting functions and relations:

In this section we cover a few different functions to solidify the concept, revisiting some older topics in the process.

### Logical operators:

We can look at many of our logical operators as a function. Let's start with \\(\lnot\\). We can define a function \\(Not\\) as follows:
- The **domain** is the set \\(B = \\{True, False\\}\\)
- The **codomain** is also the set \\(B\\)
- \\(not(x) = \\lnot x\\)

Our inputs and outputs in this case are both a single boolean value.

Functions don't necessarily have to take single values as an input. We can define a function \\(And\\) which takes two diffent boolean values. 

How can we express all the pairs of boolean values? Let's use the cartesian product:

We can define a function \\(And: B \times B \to B\\):
- The **domain** of the function is the set \\(B \times B = {(True, True), (True, False), (False, True), (False, False)}\\)
- The **codomain** of the function is the set \\(B = {True, False}\\)
- \\(And(x, y) = x \land y\\)

### Probability distributions:

We can revisit probability as well in terms of functions. Say we want to create a function that gives us the odd that a dice rolls a specific number. 

- Our domain is the set \\(D = \\{1, 2, 3, 4, 5, 6\\}\\)
- Our codomain, by definition of probability, is values between 0 and 1. we can define a set \\(P = \\{x \in \mathbb R: 0 \geq x \leq 1\\}\\). In this case it would also be valid to consider the codomain to be just the element \\(\frac{1}{6}\\), but let's stick with 
- Therefore we have our function set up such that \\(f(1) = f(2) = f(3) = f(4) = f(5) = f(6) = \frac{1}{6}\\)

This is what we call a uniform probability distribution: All the odds are the same for any of the values. This has been our assumption throughout week 5, but events are not always evenly distributed.

Imagine we have some unfair dice, where a 6 is **twice** as likely to be rolled than any other number, and all other numbers have the same probability to be rolled as each other. Our domain does not change, neither does our codomain, but our mapping must change!

Well we said that rolling a 6 is twice as likely, so can we define the function like this?

|x|1|2|3|4|5|6|
|-|-|-|-|-|-|-|
|**f(x)**|\\(\frac{1}{6}\\)|\\(\frac{1}{6}\\)|\\(\frac{1}{6}\\)|\\(\frac{1}{6}\\)|\\(\frac{1}{6}\\)|\\(\frac{2}{6}\\)|

Let's remember that the sum of all our probabilities must add up to 1. Is it the case? Adding all the probabilitis up we get \\(\frac{7}{6}\\) which is greater than 1, so we have an issue. 

This is tricky, but we can figure this out. From the definition of this unfair dice, the probability of rolling a one is the same as rolling a two, a three, a four, or a five. The probability of rolling a six is twice as much as rolling one of the other numbers. 

So we know that we want \\(f(1)+f(2)+f(3)+f(4)+f(5)+f(6) = 1\\)

\\(5f(1) + f(6) = 1\\) since all numbers under 5 have the same probability to be rolled.

\\(5f(1) + 2f(1) = 1\\) since rolling a 6 is twice as likely as rolling a 1.

\\(f(1) = \frac{1}{7}\\)

Which gives us our definition:

|x|1|2|3|4|5|6|
|-|-|-|-|-|-|-|
|**f(x)**|\\(\frac{1}{7}\\)|\\(\frac{1}{7}\\)|\\(\frac{1}{7}\\)|\\(\frac{1}{7}\\)|\\(\frac{1}{7}\\)|\\(\frac{2}{7}\\)|

This kind of function is called a **probability distribution**, which we will explore a lot more in future classes. 

The main takeway to share here is that ***functions are crafted for a specific purpose***. For example, probability distributions have a constraint on them that the sum of all the probabilities must be equal to 1. This allows us to apply our knowledge of statistics, while at the same time looking at it through the lense of functions. 

Throughout your studies and careers, you will come up with many functions - often implementing them in code. Be creative! You can set your own constraints and limits to them to solve the problem at hand.