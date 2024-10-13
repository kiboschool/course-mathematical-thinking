## Remainder classes

Let's go back to the division algorithm. We recognized earlier that the way we describe odd and even numbers falls nicely into that pattern.

How about what happens when we divide a number by 3? the possible remainders are integers between 0 and 2, inclusive. Any and all integers can be written either as:

- Numbers that fit the pattern of $3k$, also known as multiples of 3:  {...-6, -3, 0, 3, 6, 9 ...}
- Numbers that fit the pattern of $3k + 1$, {...-5, -2, 1, 4, 7, 10 ...}
- Numbers that fit the pattern of $3k + 2$, {...-4, -1, 2, 5, 8, 11 ...}

These three sets are called **the remainder classes, modulo 3**

More specifically, we can say that these sets *partition* the integers: Any number is in exactly one of these sets, as any number has a unique remainder when divided by 3.

## Congruence modulo n

If two numbers *a* and *b* belong to the same remainder class, modulo **n**, then we say that *a* is **congruent** to *b* modulo *n*. We can express this as $a \equiv b (\text{mod n})$

Notice here that we are not using an equals sign! the $\equiv$ sign means something essentially different. Most equations we have seen so far use the equal sign, and we have to be careful when shifting between the two. That shift relies on the following theorem:

$a \equiv b (\text{mod n}) \iff a = b + kn$ for some integer *k*

Take a look at all the numbers that fit $3k + 1$: You can see that the difference between 1 and 4 is 3. The difference between 1 and 10 is 9, which is a multiple of 3. In other word, if you pick any two numbers from this set, they will be some multiple of 3 apart from each other.

We can capture this same idea in a different way, leveraging our recent definition of divisibility:

$a \equiv b (\text{mod n}) \iff n | a-b$. 


## Properties of congruence

### Congruence as a relation:
We can look at congruence as a relation, and easily show that it is an equivalence relation:

1. $a \equiv a (\text{mod n})$ is trivial to show. For example, we can say that $a = a + 0n$, which is equivalent to $a \equiv a (\text{mod n})$

2. if $a \equiv b (\text{mod n})$ then $b \equiv a (\text{mod n})$. This comes from the fact that $n | a-b \implies n | b-a $, which is equivalent to $b \equiv a (\text{mod n})$

3. if $a \equiv b (\text{mod n})$ and if $b \equiv c \text{(mod n), then } a \equiv c (\text{mod n})$ is also fairly straightforward to show, but will be left as part of your homework!

### Arithmetic

We can perform operations on both sides of a congruence. For example, let $c \in \mathbb Z$: if $a \equiv b (\text{mod n})$ \\ then $a + c \equiv b + c (\text{mod n})$

This is familiar to what we've done for years with equations, but congruence is more "flexible" in a way. In fact if you have that $a \equiv b (\text{mod n})$ and $c \equiv d (\text{mod n})$, it follows that:

- $a + c \equiv b + d (\text{mod n})$
- $a - c \equiv b - d (\text{mod n})$
- $ac \equiv bd (\text{mod n})$
- $a^p \equiv b^p (\text{mod n})$

How about division? can we safely divide both sides of a congruence? let's look at an example: $24 \equiv 39 (\text{mod 5})$ 

Both 24 and 39 are multiples of 3, so let's try dividing both sides of the congruence by 3, we get:

$8 \equiv 13 (\text{mod 5})$ which is correct (We can establish this in a couple different ways, for example 13-8 = 5 so we satisfy the condition for congruence.)

So what's the issue with dividing? seems to be working fine! Let's however look at the same example, but using a different modulo: $24 \equiv 39 (\text{mod 15})$

Let's divide both sides by 3 once again to get that: $8 \equiv 13 (\text{mod 15})$ 

This is simply incorrect? 8 modulo 15 is 8, and 13 module 15 is 13, they are not in the same remainder class!

That does not mean we can not simplify the congruence by dividing, we however *might* need to change modulo. Generally, our approach to dividing both sides of a congruence will be:

if $a.d \equiv b.d (\text{mod n})$ then $a \equiv b (\text{mod }\frac{n}{GCD(n,d)})$

In our first example, we have that GCD(3,5) = 1 so we did not change our modulo. 

However, applying the formula to the second example where GCD(15, 3) = 3 we can simplify $24 \equiv 39 (\text{mod 15})$ as $8 \equiv 13 (\text{mod 5})$

## Simplifying congruences

### Example 1:
Find the remainder of x modulo 9. Now we could approach this quickly with a calculator, but it's helpful to see how we can do it directly by leveraging our understanding of congruence. This is the same as solving the following:

- $x \equiv 3491 (\text{mod 9})$
- $x \equiv 3000 + 400 + 90 + 1 (\text{mod 9})$

Can we figure out each of these remainders? 1 mod 9 is 1, so no issues there. 90 is clearly a multiple of 9, so 90 mod 9 is 0

How about 400? Well $400 \equiv 4\times100 (\text{mod 9})$

Notice that 100 = 99 + 1 so 100 mod 9 = 1

This means that $400 \equiv 4\times1 (\text{mod 9})$

Similarly, we can find that $3000 \equiv 3\times1 (\text{mod 9})$

So overwall, we get that $x \equiv 3 + 4 + 0 + 1 (\text{mod 9})$

$x \equiv 8 (\text{mod 9})$
### Example 2:
find the remainder of $3^{123} (\text{mod 7})$. We will be relying on our third and fourth arithmetic properties of congruence for this. Our goal is to break down the power so that we can slowly reduce the values on the right side of our congruence. 

$3^123 \equiv 3^{3\times41} (\text{mod 7})$

$3^123 \equiv 27^{41} (\text{mod 7})$

$3^123 \equiv 6^{41} (\text{mod 7})$ since $27 \equiv 6 (\text{mod 7})$

$3^123 \equiv 6\times6^{2\times20} (\text{mod 7})$

$3^123 \equiv 6\times36^{20} (\text{mod 7})$

$3^123 \equiv 6\times1^{20} (\text{mod 7})$ since $36 \equiv 1 (\text{mod 7})$

$3^123 \equiv 6 (\text{mod 7})$ since $1^{20} = 1)$

## References:

- [Chapter 4 of Number Theory, in context and interactive](https://math.gordon.edu/ntic/ntic/section-div-alg.html)
- [Chapter 5.2 of Discrete Mathematics, an open introduction, 3rd edition](https://discrete.openmathbooks.org/dmoi3/sec_addtops-numbth.html)