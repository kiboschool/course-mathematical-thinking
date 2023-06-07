# Sets

## Key Ideas:
- Define sets, as well as set builder notation.
- Introduce the concept of elements belonging to a set.
- Define established sets
- Introduce Cardinality and Complements of sets

## What is a set?

Sets are a crucial but simple concept for our studies. A **set** is an **unordered collection of objects**. You can probably think of a few things that are sets: The set of all the players to ever play for Arsenal, or the set of meals you've tried in a given restaurant. The *fundamental* question we ask about sets is whether or not an item belongs to them. It does not matter what order it is within the set, just whether or not it is in it. 

Let's talk notation with a simple set: let \\( V = \\{a, e, i, o, u, y\\}\\) be the set of all vowels. We can say that a belongs to the set \\( V\\), and that z does not belong to \\( V\\). We have notation for that too:
- \\(a \in  V\\) - in other words *a* belongs to the set \\( V\\), which is a True proposition
- \\(z \notin  V\\) - in other words *z* does not belongs to the set \\( V\\), which is also a True proposition

Finally, one thing to bear in mind is that sets can contain anything and everything: numbers, symbols, words, other sets.

For example consider: \\( A = \\{42, guide, \\{79, 80, 82\\}\\}\\) This set contains the number 42, the word guide, and the set {79, 80, 82}. This means that 80 \\(\notin  A\\), even though 80 belongs to a set within \\( A\\), it is not directly an element of \\( A\\)
### Programming 1 connection:
Sets are so useful, they are a core part of many programming languages as well. You can even create them in a similar fashion: In python you can recreate our set of vowels as follows:

> v = {'a', 'e', 'i', 'o', 'u', 'y'} 

You can view more information about sets in python [here](https://realpython.com/python-sets/). Effectively everything we cover in this week's content can be done in code as well, so feel free to experiment with Python alongside this week's content!

### Cardinality and the empty set:
Here we are again with new names, but cardinality is a simple concept: It refers to the size of a set. Our set of vowels \\( V\\) has 6 elements within it, so we can say that its cardinality is 6, or using a new symbol: |\\( V\\)| = 6

Could there be a set with no elements at all? a cardinality of 0? well yes, we call it the empty set, and will use it extensively soon! We use it so often in fact that it gets its own symbol, \\(\emptyset\\)

### Complements of sets:
If a set defines a specific collections that belong to it, then there surely is a set of elements who *do not* belong to it. We call that new set the complement. For example, we may think that the complement of \\(V\\) is the set of all consonants. This makes intuitive sense, but there is a wrinkle here. \\(\bar V\\), the complement of \\(V\\), is the set of all elements which do not belong to \\(V\\). Does the number 187 belong to \\(V\\)? it does not, so it should then belong to \\(\bar V\\). 

Let's combine the last two concepts we've encountered: What is the complement of the emptyset, \\(\bar \emptyset\\)? Well *nothing* is in the empty set, so *everything* should be in its complement. We refer to the set that contains *everything* as the Universal set, with symbol \\(U\\)
## Famous sets

In the days and weeks to come, we will reason about specific groups of numbers. These are so commonly used that they have some shorthands we share here for reference:
- \\(\mathbb N\\) is the set of **natural** number, or non-negative integers. Sometimes refered to as whole numbers, \\(\mathbb N = \\{0, 1, 2, 3 ...\\}\\)
- \\(\mathbb Z\\) is the set of **integers**, this includes positive and negative whole numbers, \\(\mathbb Z = \\{..., -2, -1, 0, 1, 2, ...\\}\\)
- \\(\mathbb Q\\) is the set of **rational** numbers, this includes all elements of \\(\mathbb Z\\), as well as all numbers that can be expressed as finite fractions like 0.25, or 0.11
- \\(\mathbb R\\) is the set of **real** numbers, this includes all elements of \\(\mathbb Q\\), as well as all numbers that can not be expressed as finite fractions such as *pi*, or \\(\frac {1}{3}\\)

## Set builder notation
Our initial examples of sets were quite small, so we could list all the elements directly, but as we saw in the famous sets above, some sets have infinitely many elements! 

We can express the key idea behind a set using set builder notation, a shorthand that captures the *conditions* we set on an element to belong to a set. Let's try to define an infinite set: \\(E\\) is the set of **even, positive** integers. 

In other words, \\(E\\) is the set of all elements of \\(\mathbb N\\) that are even. so if we consider a variable \\(x \in E \to (x \in \mathbb N \land x\\) is even \\()\\)

We can further condense this idea by saying: \\(E = \\{x \in \mathbb N : x\text{ is even }\\}\\). Here, the **:** is a shorthand for "such that". Following the **:** you can define propositions that **must** be true for all elements of the set. 

There may be a few different ways to express a given definition of a set, but this is a helpful notation we should practice. Try to interpret the following four sets in plain english:

\\(\\{x \in \mathbb R: x + 3 \in \mathbb N\\}\\)

This is the set of all numbers x such that x + 3 is in \\(\mathbb N\\), in other words a postive integer. In other words, this is the set {-3, -2, -1, 0, 1, ...} as -3 + 3 = 0 which belongs to \\(\mathbb N\\)

\\(\\{x \in \mathbb N : x + 3 \in \mathbb N\\}\\)
This is the set of all positive integers x such that x+3 is a positive integer. We end up with the set of positive integers \\(\mathbb N\\)

\\(\\{x \in \mathbb R: x \in \mathbb N \lor -x \in \mathbb N\\}\\)
This is the set of all numbers x such that x is a positive integer, or -x is a positive integer. If -x is a positive integer, then x is a negative integer. This ends up being a convoluted way to represent \\(\mathbb Z\\), the set of all integers.

\\(\\{x \in \mathbb R: x \in \mathbb N \land -x \in \mathbb N\\}\\)
This is the set of all numbers x such that x is a positive integer, **and** -x is a positive integer. This is an odd combination, but there is one number which satisfies it: 0. This makes our answer the set {0}

Next, we cover operations between sets.

## References:
For further details, you can read through the following chapter:
- [Discrete mathematics - an open introduction part 0.3](http://discrete.openmathbooks.org/dmoi3/sec_intro-sets.html)
