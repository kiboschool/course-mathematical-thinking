# Permutations

## Key Ideas:
- Defining the concept of a permutation.
- Introduce notation and mathematical intuition behind computing permutations.
- Introduce a few applications of permutations.

## Definition

A permutation is a potential rearrangement of elements. For example, the alphabet as we know it, from *a to z*, is one *possible way* of ordering the 26 letters. The aim of this first section is to develop the mathematical tools to answer questions like "How many other alphabets could there have been?" we will revisit this further down, but let's start with smaller examples.

Say you have three classmates that are running late: Emmanuel, Kwasi, and Maya. You start wondering in what order they will show up - assuming none of them show up at exactly the same time.

1. Emmanuel, Kwasi, Maya
1. Emmanuel, Maya, Kwasi
1. Maya, Kwasi, Emmanuel
1. Maya, Emmanuel, Kwasi
1. Kwasi, Emmanuel, Maya
1. Kwasi, Maya, Emmanel

As far as I can tell those are the possible ways we can see our classmates coming through. six total permutations. Regardless of what the sequence is, if you have a sequence of three elements, there are six permutations to it. How can we shuffle the letters abc? well we have abc, acb, bca, bac, cab, cba. 6 options as well. 

Let's simplify even further, and build up our intuition from an even more basic example.. A sequence of one elements only has one possible permutation. You can't shuffle a deck that contains only 1 card. So if our elements are only the letter 'a', then 'a' is the only permutation possible.

If we have two elements, *a* and *b*, how many permutations do we have? you can quickly intuit that there are two: ab and ba. Let's dissect this a bit further though: Any permutation will have two elements. You can imagine that there are two slots available to put letters in - the first one and the last one. How many options do we have to put in the first slot? two letters, we could put either a or b. Once we've done so, how many options do we have for the last slot? just one, the letter we did not chose at the beginning.

Let's continue with this same logic with three elements now, *a* and *b* and *c*. There are now three available slots. How many options do we have to put in as the first letter of our permutation? well three. At that point, we are left with two slots to fill, and two letters to insert them in. This is the same as the problem above of permutations of two elements, so we know there are two options to complete the permutation. So given that there are three options for the first slot, then two to continue on, we get the total of six permutations. 

Let's do it one more time! *a, b, c, d*. There are four options for the first letter, and we are left to organize three letters in three slots, which we've already established to be six permutations. This gives us a total of 24 options. 

## Notation:

First, let's define the factorial notation. \\(n! = n . (n-1) . (n-2 )...1\\). In plain english, we read that n factoriel is the product of n, n-1, n-2, etc. all the way up to 1.

We can therefore define the number of permuations of n **distinct** elements as n!

So to go back to our original question: How many potential orders could there have been? well there are 26 letters, so 26! gives us 4.03 x 10^26, or 403 million billion billion - yes, there are no typos here - different possible permutations. As you can see, with as simple a set as the 26 letters, we would quickly have to perform a tremendous amount of computation and store a lot of data if we wanted to keep a record of every possible permutation of the alphabet.

### Special case: Zero!

What shoud 0! be equal to? this is a tricky one to define, but we can reach a definition from the following observation. 

Notice that \\(\fract{n!}{n} = \frac{n . (n-1) . (n-2 )...1}{n})\\)

As we cancel out *n* from both parts of the fraction, we obtain \\((n-1) . (n-2 )...1 = (n-1)!\\) by definition

Applying this to n = 1 we obtain:
\\(\frac{1!}{1} = (1-1)!\\)
\\(\frac{1}{1} = 0!\\)

Thus we define 0! to be equal to 1 moving forward!

## k-permutations:

Sometimes, we do not care about the entire set of elements, but rather just a subset of it. For example, there are 32 teams joining the world cup. How many permutations are there for the top three? By our current logic, this means we have *three* slots to fill. How many teams could take the first slot and win the world cup? well there are 32 options. In the next slot, we are left with 31 options, and finally, 30 options, so 32.31.30 gives us 29760 possible permutations to get to the top three!

This can be generalized in the following notation. We call a *k-permutation* of *n* elements the number of ways to arrange *k* elements from a set of *n* distinct ones. The number of these permutations can be computed as follows:

\\(P(n, k) = \\(\frac{n!}{n-k!}\\)

More simply, we want the first *k* terms of the factorial computation, not all of them. We can obtain that mathematically by divinding n! by (n-k)!, leaving us with k elements.


## Repetitions:

Both the formulas we have shown so far fundamentally rely on the set of elements being unique, but what if there is some repetition?  There are two types of problems that will force us to change our approach. 

### Repeated elements:
For this first category of problems, we have elements in our sequence that are equivalent to each other. let's look at an example. If our sequence of elements are *a*, *a*, and *b*, the possible permutations are:
1. aab
2. aba
3. baa

We only find three permutations this time, instead of the six when we had all distinct elements. How do we find a pattern we can generalize here? Let's label our two *a*'s. Now our sequence is \\(a_1, a_2, and b\\). When we look at the permutation aab, we could've picked either a for the first two slots. So we could've picked \\(a_1a_2b\\) or \\(a_2a_1b\\) and the result would've been the same. 

In other words. When we have two slots dedicated to the letter a, we can distribute \\(a_1\\) and \\(a_2\\) across them. How many ways can we do that? it would be 2 factoriel! 

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

The same logic applies for the third and fourth slot. This leaves us with \\(26 . 26 . 26 . 26 = 4^26 \\) possible permutations. 

Generally speaking then, a k-permutation of a sequence of n elements that **allows replacement** can be computed as \\(k^n\\)

## References:
For further details, you can read through the following chapters:
- [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
- [Discrete mathematics - an open introduction part 1.3](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
