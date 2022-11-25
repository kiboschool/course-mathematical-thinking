## Common denominators

Let's consider an integer *a*. We can define a set of denominators of *a* such that \\(denominators = \\{k \in \mathbb N \\} \\) if \\(k|a\\)

We will not often need to identify all the denominators of a given number, we are however interested in finding what denominators two numbers share in common. Common denominators can be handy to address some problems. Note that given integers *a*, *b*, and *d* such that \\(d|a\\) and \\(d|b\\) we can easily show that:

- \\(d | k_1.a + k_2.b\\) for any integers \\(k_1 , k_2\\)
- \\(d | k_1.a - k_2.b\\) for any integers \\(k_1 , k_2\\)
- \\(d | k.a.b\\) for any integer *k*

### The GCD

Most commonly, we will often seek to know what their **greatest** common denominator is. We will refer to it as GCD moving forward. 

Consider the following situation: We are fixing up a house, and have a rectangular space that is 253 cm long and 92 cm wide. We want to decorate it with square tiles. How big of a tile can we use to make sure that we cover everything?

One obvious first answer is using tiles that are 1 cm by 1cm in size. It would take us a lot of tiles, but we would cover the space completely using square tiles.

What if we tried 2 by 2 cm tiles? that would fit nicely along the width of the space, as \\(2|92\\), but that would not properly cover the length. 

Whatever number we use must be a common denominator of the two dimensions. Let's try to factor out 92: \\(92 = 2 \times 2 \times 23\\). How about 253? You can try out a few numbers, but hopefully you will also find that \\(253 = 11 \times 23\\). This means that GCD(92, 253) = 23, so we can use 23 by 23 cm tiles and fully cover the area we need.

## Primes:

Every number has a few guaranteed denominators: 1 can divide every number after all. Similarly, a number always divides itself, with the exception of 0. 

For some numbers, these are the **only** denominators they have. For example both 2 and 3 are prime, so are 11, 13 and 29.

if *p* is a prime number then for any integer *b* we have that: 
- \\(p|b \implies GCD(p, b) = p\\)

- \\( \not p|b \implies GCD(p, b) = 1 \\)

Prime numbers have fascinated mathematicians for centuries, and their properties come in very handy as we will see in the final part of our project. For now though, you should simply be aware of them. 

### Relative primes

How about if the dimensions we had to deal with for our tiling problem were 92 by 105 centimeters? Well, \\(105 = 3 \times 5 \times 7\\), so what does that mean for our GCD? the only denominator these tho numbers have in common is 1. 

More formally, if *a* and *b* are integers and GCD(a, b) = 1, then *a* and *b* are **relative primes**

## Finding the GCD:
So far, we've found the GCD of relatively small numbers that were straightforward to factor out. How can we reliably answer problems that are larger though? Luckily we have a handy method to do just that: 

### The euclidian algorithm:

Let *a* and *b* be integers. To find GCD(a,b) perform the division algorithm until you hit a remainder of zero, as below.

- \\(a = q_1.b + r_1\\)
- \\(b = q_2.r_1 + r_2\\)
- \\(r_1 = q_3.r_2 + r_3\\)
- \\(r_2 = q_4.r_3 + r_4\\)
- \\(...\\)
- \\(r_{n-3} = q_{n-1}.r_{n-2} + r_{n-1}\\)
- \\(r_{n-2} = q_{n}.r_{n-1} + 0\\)

Then \\(GCD(a,b) =r_{n-1}\\), the final non-zero remainder.

Let's work through an example: Let's find GCD(60, 42):

- \\(60 = 42.1 + 18\\). Our first remainder is 18
- \\(42 = 18.2 + 6\\). We divide 42 by our first remainder
- \\(18 = 6.3 + 0\\) We devide our first remainder, 18, by the next one, 6.

At this point we find a remainder of 0, so we stop. GCD(60,42) = 6, as it was our last non-zero remainder.

### What even is an algorithm?

An algorithm is a set of instructions or rules to be followed to solve a specifc problem. This will be a term you will see more and more often as you progress through your study of computer science. Every problem you've solved in code so far, you have created an algorithm for. 

Algorithms are to be followed strictly to reach the desired goal, but that doesn't make all algorithms correct? We still have the burden of proof to **show** that a specific algorithm can achieve its goal for any input we provide it. Euclid's algorithm was correct in finding GCD(60, 42), but how do we prove that 

### Showing The algorithm terminates

You may have ran into an issue already in your programming class where your code kept running, kept looping, and you could not stop it. An algorithm should be designed to eventually *terminate*. Let's show that euclid's algorithm eventually does so.

By our definition of division, we know from this statement 
\\(a = q_1b + r_1\\) that \\(r_1 \in \mathbb N\\) and that \\(0 \leq r_1 < b\\)

Similarly then, from \\(b = q_2r_1 + r_2\\) we know that \\(r_2 \in \mathbb N\\) and that \\(0 \leq r_2 < r_1\\)

so if we look at the sequence of all remainders produced by the algorithm \\(\{r_1, r_2, r_3....\}\\) we know that all its elements belong to \\(\mathbb N\\), and that this sequence is decreasing, each one of them is smaller than the previous one.

The smallest element in \\(\mathbb N\\) is 0, so if we continue following the algorithm we would _eventually_ reach that value. A new remainder can never be larger than the previous one. This means that sooner or later, we will reach the **condition** that ends our algorithm. 

### showing that \\(r_{n-1}\\) is the GCD
We can approach this proof in a few different ways, but it ultimately relies on showing two things:

1. Showing that \\({r_{n-1}}\\) is a common denominator of *a* and *b*
2. Showing that \\({r_{n-1}}\\) is indeed the greatest of all common denominators of *a* and *b*

Can we convince ourselves that \\(r_{n-1}|a\\) and \\(r_{n-1}|b\\)?

Let's start from the final step of the algorithm:
- \\(r_{n-2} = q_nr_{n-1} + 0 => r_{n-1} | r_{n-2}\\)
- We can keep working backwards from there: Since \\(r_{n-1} | r_{n-2}\\), then  \\(r_{n-3} = q_{n-1}r_{n-2} + r_{n-1} \implies \\(r_{n-1} | r_{n-3}\\)
- Ultimately this means that \\(r{n-1} | r_2\\) and \\(r_{n-1} | r_1\\)
- Since \\(b = q_2r_1 + r_2\\), it follows that \\(r_{n-1} | b\\)
- Since \\(a = q_1b + r_1\\), it follows that \\(r_{n-1} | a\\)
- So \\(r_{n-1}\\) is a common denominator of both *a* and *b*

let *d* be any common denominator of *a* and *b*

- By definition, \\(d | a\\), and \\(d | q_1.b\\) 

- \\(d | a - q_1.b\\) by definition, so \\(d | r_1\\)

- Considering the second step of our algorithms we have that \\(b = q_2.r_1 + r_2\\). By the same logic as above it follows that \\(d | r_2\\)
- Repeatedly applying the same logic for each step of the algorithm, we ultimately reach that \\(d | r_{n-1}\\)
- This implies that \\(r_{n-1} \geq d\\)
- so for any commond denominator *d* of *a* and *b*, \\(d \leq r_{n-1}\\)
- Therefore, \\(r_{n-1}\\) is the greatest common denominator of *a* and *b*

And here you go, your first proof of an algorithm's correctness! You can view a live version of the proof [here](https://www.youtube.com/watch?v=8cikffEcyPI&ab_channel=MichaelPenn) for reference.

## Bezout's identity

We have one final takeway from the algorithm to explore. Let's look at a simple application of the algorithm to find the gcd of 8 and 5:

- 8 = 1.5 + 3
- 5 = 1.3 + 2
- 3 = 1.2 + 1
- 2 = 2.1 + 0

so we have that GCD(8,5) = 1

Now let's start from the equation 3 = 1.2 + 1:
- 3 - 1.2 = 1
- (8-5) - (5-3) = 1
- 8 - 2.5 + 3 = 1
- 8 - 2.5 + (8-5) = 1
- 2.8 - 3.5 = 1

Ultimately, using substitution we can find a way to express GCD(8,5) as a *linear combination* of 8 and 5: in other words, we found integers \\(x, y \in \mathbb Z\\) such that \\(8x + 5y = GCD(8,5)\\)

Working through the euclidian algorithm backwards is one way of approaching this, and is generalizable. **Bezout's identity** states that given integers a, b \\(\exists x,y \in \mathbb Z \text{such that } ax + by = GCD(a,b)\\)

This will come in handy in two ways: First, this will make it easier for us to spot whether or not a specific problem has a solution in the first place.

Secondly, and most importantly, is the case of coprime numbers, like 8 and 5 above. Since their GCD is 1, this means we can multiply both sides of the equation by any integer. In other words, we **can** find a linear combination of 8 and 5 to represent **any** integer we want. This will come in handy in our project!

At this point though let's transition to discussing congruence, and seeing the kind of problems we can solve with it.

## References:

- [Chapter 2 of Number Theory, in context and interactive](https://math.gordon.edu/ntic/ntic/section-div-alg.html)
- [Chapter 5.2 of Discrete Mathematics, an open introduction, 3rd edition](https://discrete.openmathbooks.org/dmoi3/sec_addtops-numbth.html)