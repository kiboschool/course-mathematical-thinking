# Permutations

## Key Ideas:
- Defining the concept of a permutation.
- Introduce notation and mathematical intuition behind computing permutations.

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

Let's simplify even further, and build up our intuition from an even more basic example:
- A sequence of one elements only has one possible permutation. You can't shuffle a deck that contains only 1 card. So if our elements are only the letter 'a', then 'a' is the only permutation possible.

- If we have two elements, *a* and *b*, how many permutations do we have? you can quickly intuit that there are 2: ab and ba. Let's dissect this a bit further though: Any permutation will have two elements. You can imagine that there are 2 slots available to put letters in. How many options do we have to put in the first slot? we could put either a or b. Once we've done so, how many options do we have for the last slot? just one, the letter we did not chose at the beginning. 

- With three elements now, *a* and *b* and *c*. There are now three available slots. How many options do we have to put in as the first letter of our permutation? 3. At that point, we are left with 2 slots to fill, and 2 letters to insert them in. This is the same as the problem above, so we know there are two options to complete the permutation. So given that there are 3 options for the first slot, then 2 to continue, we get the total of six permutations. 

Let's do it one more time! *a, b, c, d*. There are four options for the first letter, and we are left to organize three letters in three slots, which we've already established to be six permutations. This gives us a total of 24 options. 

## Notation:

First, let's define the factorial notation. $ n! = n . (n-1) . (n-2 )...1 $. In plain english, we read that n factorial is the product of n, n-1, n-2, etc. all the way up to 1.

We can therefore define the number of permuations of n **distinct** elements as n!

So to go back to our original question: How many potential orders could there have been? well there are 26 letters, so let's compute 26!. This should equate to approximately 403 million billion billion - yes, there are no typos here - different possible permutations. As you can see, with as simple a set as the 26 letters, we would quickly have to perform a tremendous amount of computation and store a lot of data if we wanted to keep a record of every possible permutation of the alphabet.

### Special case: Zero!

What shoud 0! be equal to? this is a tricky one to define, but we can reach a definition from the following observation. 

Notice that $ \frac{n!}{n} = \frac{n . (n-1) . (n-2 )...1}{n} $

As we cancel out *n* from both parts of the fraction, we obtain $ (n-1) . (n-2 )...1 = (n-1)! $ by definition

Applying this to n = 1 we obtain:

$ \frac{1!}{1} = (1-1)! $

$ \frac{1}{1} = 0! $

Thus we define 0! to be equal to 1 moving forward!

## Permutations Video 

<div style="position: relative; padding-bottom: 59.73451327433629%; height: 0;"><iframe src="https://youtube.com/embed/DkN_b5WoVsI" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## k-permutations:

Sometimes, we do not care about the entire set of elements, but rather just a subset of it. For example, there are 32 teams joining the world cup. How many permutations are there for the top three? By our current logic, this means we have *three* slots to fill. How many teams could take the first slot and win the world cup? well there are 32 options. In the next slot, we are left with 31 options, and finally, 30 options, so 32.31.30 gives us 29760 possible permutations to get to the top three!

This can be generalized in the following notation. We call a *k-permutation* of *n* elements the number of ways to arrange *k* elements from a set of *n* distinct ones. The number of these permutations can be computed as follows:

$$P(n, k) = \frac{n!}{n-k!}$$

More simply, we want the first *k* terms of the factorial computation, not all of them. We can obtain that mathematically by divinding n! by (n-k)!, leaving us with k elements.

## k-permutations Video 

<div style="position: relative; padding-bottom: 59.73451327433629%; height: 0;"><iframe src="https://youtube.com/embed/QQnalru1T9Y" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## References:
For further details, you can read through the following chapters:
- [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
- [Discrete mathematics - an open introduction part 1.3](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
