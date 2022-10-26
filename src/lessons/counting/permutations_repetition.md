# Permutations with repetition

## Key Ideas:
- Highlight the difference between permutations with replacement, and premutations with limited repeated elements.
- Introduce notation and mathematical intuition behind computing permutations with forms of repetition.

## Repetitions:

Both the formulas we have shown so far for permutations fundamentally rely on the set of elements being unique, but what if there is some repetition?  There are two types of problems that will force us to change our approach. 

### Repeated elements:
For this first category of problems, we have elements in our sequence that are equivalent to each other. let's look at an example. If our sequence of elements are *a*, *a*, and *b*, the possible permutations are:
1. aab
2. aba
3. baa

We only find three permutations this time, instead of the six when we had all distinct elements. How do we find a pattern we can generalize here? Let's label our two *a*'s. Now our sequence is \\(a_1, a_2, and b\\). When we look at the permutation aab, we could've picked either a for the first two slots. So we could've picked \\(a_1a_2b\\) or \\(a_2a_1b\\) and the result would've been the same. 

In other words. When we have two slots dedicated to the letter a, we can distribute \\(a_1\\) and \\(a_2\\) across them. How many ways can we do that? it would be 2 factorial! 

So, for each of our original permutations, there is one other one that is equivalent to it, as it's simply a permutation of the different *a*'s, which is why we end up ulitmately with \\(\frac{6}{2} = 3\\) different permutations

More generally we can say that if we have *n* elements such that \\(n_1\\) of them are of type 1, \\(n_2\\) elements of type 2, all the way up to \\(n_k\\) elements of type k, then we can compute the number of permutations of all those elements as \\(\frac{n!}{n_1!n_2!...n_k!})

Time for an example: How about if we had two *a* and two *b* as our elements, how many permutations are there? we know we have 2 elements of the same type *a*, then another two elements of the same type *b*. Our number of permutations should then be: \\(\frac{4!}{2!2!} = \frac{24}{4} = 6\\)

Let's try to list them out:

1. aabb
2. abab
3. abba
4. bbaa
5. baba
6. baab

### Replacement:
Our second style of problems is known as replacement problems. In these kind of problems, putting an element from our sequence in a given slot does not prevent it from being added to another slot in our permutation. Imagine for example that while you step away from your laptop, a cat walks accross your keyboard. It presses the keyboard 4 times, then runs away as you come back.

Assuming for a moment that each letter on your keyboard is equally likely to be pressed - how many possible words could the cat have typed while you were away? Let's think about it. 

Our sequence of elements here are all the 26 letters of the alphabet. We are looking for how many 4-permutation can be generated, but allowing for the fact that the cat can press the same key many times.

So how many options do we have for the first slot? 26, as with our previous examples.
How about the second slot? well all the letters are still fair options - typing 'a' the first time does not prevent us from typing 'a' again, so it's 26 options once again.

The same logic applies for the third and fourth slot. This leaves us with \\(26 . 26 . 26 . 26 = 4^(26) \\) possible permutations. 

Generally speaking then, a k-permutation of a sequence of n elements that **allows replacement** can be computed as \\(k^n\\)

## References:
For further details, you can read through the following chapters:
- [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
- [Discrete mathematics - an open introduction part 1.3](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
