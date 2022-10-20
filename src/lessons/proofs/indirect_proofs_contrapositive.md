# Proofs by contrapositive

## Key Ideas:
- Defining the strategy for proofs by contrapositive
- Showcasing examples of proofs by contrapositive

## The argument's strategy:

Direct proofs can sometimes be hard, we can reach dead ends where it's unclear how to proceed. Luckily, there are alternative strategies when the direct method proves challenging. 

The first strategy we will cover is the proof by contrapositive. This hinges on the observation that \\(P \to Q\\) is logically equivalent to its contrapositive \\(\lnot Q \to \lnot P\\). *Recall our truth table from last week for this!*

This means that if you can prove the contrapositive, it is the same as proving the initial implication. Instead of assuming P is True and trying to show Q is True, you can assume \\(\lnot Q\\) is True and try to show that \\(\lnot P\\)

Let's try out an example: 

	Show that if x and y are two integers whose product is even, then at least one of them is even. 

First of all, what is the contrapositive of this implication? think about it for a moment before proceeding:

	If x and y are two odd integers, then the product of x and y is odd.

From here on out, we can approach our proof directly: 
- Assume that x and y are two odd integers.
- This means that \\(x = 2k+1\\) and \\(y = 2n+1\\) for some integers k and n - we want to make a general argument, so we cannot assume that k and n are equal, but we also do not want to assume that they are different.
- This means that \\(xy = (2k+1)(2n+1)\\)
- Expanding we get \\(xy = 4kn + 2k + 2n + 1\\)
- \\(xy = 2(2kn + k + n) + 1\\)
- \\(xy = 2m + 1\\) where m is an integer such that m = 2kn + k + n
- This means that by the definition of odd numbers, xy is odd
- This shows that our contrapositive statement is True.
- Therefore, our inital implication is True.

Again, practice will make perfect. Consider the video below for more examples before we proceed to more strategies.

<iframe width="560" height="315" src="https://www.youtube.com/embed/vMwejR0bqwo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## References:
For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.9](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
