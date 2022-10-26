# Combinations

## Key Ideas:
- Defining the notation and formula for combinations
- Highlighting the binomial coefficient visually

## Definition

Picture this: It's a hot day, and you stumble into a juice vendor. They have 5 different fruits: Bananas, Oranges, Guava, Strawberries, and Pineapple. You can combine any three fruits into a juice. How many possible juices are there? 

We may be tempted to immediately apply permutations here, and compute \\(P(5, 3) = \frac{f!}{2!} = 60\\) different options. This is a good start, but a key observation here is about **order**

When dealing with permutations, the **order** of each element is highly relevant. It's inherent in the formula that picking Bananas **then** Oranges **then** Guava is different from picking Oranges **then** Guava **then** Bananas. 

However, I'd argue that once we blend them all into juice, the order in which we put them in does not matter all that much!

So how do we find a more accurate approach? Let's think about it in similar fashion as with permutations with repetition: There are a lot of permutations that are effectively the same. If I pick Bananas **then** Oranges **then** Guava, no matter how many times I rearrange those fruits, as long as the exact same three are present we obtain the same juice. 

How many ways are there to rearrange three elements? 3 factoriel! 

So our total number of possible juices needs to be further divided by 3! = 6, giving us 10 different options. We can list them intuitively:
1. Bananas, Oranges, Guava
2. Bananas, Oranges, Strawberries
3. Bananas, Oranges, Pineapple
4. Bananas, Guava, Strawberry
5. Bananas, Guava, Pineapple
6. Bananas, Strawberry, Pineapple
7. Oranges, Guava, Strawberries
8. Oranges, Guava, Pineapple
9. Oranges, Strawberries, Pineapple
10. Guava, Strawberries, Pineapple

Which gives us 10 different combinations. Let's formalize our formula and notation.

## Notation

The number of ways we can pick *k* elements out of *n* different choices is denoted by the symbol \\(\binom{n}{k} = \frac{n!}{k!(n-k)!} \\). We read this as *n choose k*. More formally, this is also refered to as the **binomial coefficient**

This formula has some interesting properties: What is \\(\binom{n}{n}\\)? How many ways are there to choose n elements from a set of n? there should only be one way, which works out once we plug the values in: \\(\frac{n!}{n!(n-n)!} = \frac{n!}{n! * 1} = 1\\)

How about \\(\binom{n}{0}\\)? well plugging into our formula we get \\(\frac{n!}{0! (n-0)!} = \frac{n!}{n! * 1} = 1\\). This is odd once you word it out in english, but still makes sense: How many ways can you choose 0 elements from a set? well only one way: Don't choose anything. Interestingly though, we notice that \\(\binom{n}{0}\\) = \\(\binom{n}{n}\\) = 1

This symmetric pattern continues. Let's look at two other scenarios:

\\(\binom{n}{1} = \frac{n!}{1! (n-1)! = \frac{n!}{(n-1)!} = n\\) 

Once again this makes sense in plain english: How many ways are there to pick one element from a set of *n*? *n* different ways - you could pick any of the elements

How about \\(\binom{n}{n-1}\\)?
Well: \\(\binom{n}{n-1} = \frac{n!}{(n-1)! (n-(n-1))! = \frac{n!}{(n-1)!} = n\\) 

Interestingly we obtain the same result! \\(\binom{n}{1}\\) = \\(\binom{n}{n-1}\\) = n. We can make sense of this logically: Choosing n-1 elements from a set of *n* is effectively the same as picking 1 element **not** to choose. 

This symmetric pattern continues, as  \\(\binom{n}{k}\\) = \\(\binom{n}{n-k}\\) for all \\(0 \le k \le n). This is an important pattern that can help in problem solving, and is explored in the diagram below

![\\(Pascal's triangle\\)](/images/pascal-triangle.svg)

Notice the pattern: Starting from the top, the left and right edges of the triangle consist of the number *1*

Every other spot is the sum of the two numbers above it. How does this connect to combinations? you can view the topmost row as mapping out to \\(\binom{0}{0}\\), which equals 1

The next row, from left to right, represents \\(\binom{1}{0}\\) and \\(\binom{1}{1}\\)
The following one, once again from left to right, represents \\(\binom{2}{0}\\), \\(\binom{2}{1}\\), and \\(\binom{2}{2}\\)

This makes pascal's triangle a handy tool if you are working on combination problems. Eac


## References:
For further details, you can read through the following chapters:
- [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
- [Discrete mathematics - an open introduction part 1.4](https://discrete.openmathbooks.org/dmoi3/sec_comb-proofs.html)
