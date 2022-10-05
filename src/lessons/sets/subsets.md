# Subsets & Powersets

## Key Ideas:
- Introduce subsets and strict subsets
- Compute Power Sets

## Equality and Subsets:
Two sets are equal if they contain exactly the same elements. Recall that order does not matter in this case, so if we have: 
- \\(A = \\{1, 2, 3\\}\\)
- \\(B = \\{2, 3, 1\\}\\)
then we can still say that \\(A = B\\). All elements of \\(A\\) are in \\(B\\), and vice versa. 

How about comparing our set \\(A\\) with \\(C = \\{1, 2, 3, 4\\}\\)? Clearly they are not equal, but they are close! all of the elements of \\(A\\) are in \\(C\\). We say in this case that \\(A\\) is a *subset* of \\(C\\), and that \\(C\\) is a *superset* of \\(A\\). We have two symbols to represent this, depending on how strict we want the statement we make to be. 

If we only want to say that all elements of \\(A\\) are in \\(C\\), we use \\(\subseteq\\). \\(A \subseteq C \to \forall x \in A, x \in C\\). In this case, it is also true that \\(A \subseteq B\\)

Sometimes, we want to state that a set is a **strict subset** of another - meaning we do not allow the scenario for the sets to be equal. This is similar in spirit to the difference between \\(x \lt 3 \\) and \\(x \le 3\\).

So to indicate that \\(A\\) is a strict subset of \\(C\\), we use \\(\subset\\). \\(A \subset C \to (\forall x \in A, x \in C) \land (\exists y \in C \land y \notin A)\\)

## Power sets:
How many subsets does the set \\(A = \\{1, 2, 3\\}\\) have? we can think of a few quickly, like \\(\\{1\\}\\) or \\(\\{2, 3\\}\\). We use the term *Power Set* to represent - and bear with us here - the set of all subsets of a given set. Think about it for a moment, how many elements do you think qualify as *subsets* of \\(A\\)? Take a few minutes to think about it before clicking here!

More directly, the powerset of \\(A\\) \\( \mathcal P\(A\) = \\{\emptyset, \\{1\\}, \\{2\\}, \\{3\\}, \\{1, 2\\}, \\{1, 3\\}, \\{2, 3\\}, \\{1, 2, 3\\}\\}\\)

Note that \\(2 \notin \mathcal P\(A\)\\), as it is the **set** {2} that is contained, not the number 2.


## References:
For further details, you can read through the following chapter:
- [Discrete mathematics - an open introduction part 0.3](http://discrete.openmathbooks.org/dmoi3/sec_intro-sets.html)
