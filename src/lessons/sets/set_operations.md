# Set Operations

## Key Ideas:
- Introducing basic operations on sets: Union, Intersection, Substraction

## Manipulating sets:
The same way we can combine numbers through addition, substractions, etc. There are a number of questions we may want to ask about multiple sets. 

### Union:
The Union of two sets \\(A\\) and \\(B\\) represent all the elements that belong to either of the two sets. The union operation is represented by the symbol \\(\cup\\)

Formally then, \\(A \cup B = \\{x \in U: x \in A \lor x \in B\\}\\)
Given this definition, how would you evaluate \\(A \cup \emptyset\\) ? Try it out.


This evaluates to \\(A\\). The empty set has no elements to contribute to the union

How about \\(A \cup U\\)?

This evaluates to \\(U\\). The universal set already contains all the elements of \\(A\\)

### Intersection
The Intersection of two sets \\(A\\) and \\(B\\) represent all the elements that belong to both of the two sets. The intersection operation is represented by the symbol \\(\cap\\)

Formally then, \\(A \cap B = \\{x \in U: x \in A \land x \in B\\}\\)
Given this definition, how would you evaluate \\(A \cap \emptyset\\)?

This evaluates to \\(\emptyset\\). The empty set has no elements, so there are no elements in common between it and \\(A\\)

How about \\(A \cap U\\)?

This evaluates to \\(A\\). The universal set already contains all the elements of \\(A\\), so those are the elements the two sets have in common

### Substraction:
The substraction of two sets \\(A\\) and \\(B\\) represent all the elements that belong to \\(A\\) but not to \\(B\\) of the two sets. The intersection operation is represented by the symbol \\(\setminus\\)

Formally then, \\(A \setminus B = \\{x \in U: x \in A \land x \notin B\\}\\)

Notice that while order did not matter for union and intersection, \\(A \setminus B\\) and \\(B \setminus A\\) will produce different results.

Given this definition, how would you evaluate the following \\(A \setminus \emptyset\\)? 

This evaluates to \\(A\\). The empty set has no elements, so there are no elements to remove \\(A\\)

How about \\(A \setminus U\\) and \\(U \setminus A\\)? We should expect these to be different. 

\\(A \setminus U\\) evaluates to \\(\emptyset\\). The universal set already contains all the elements of \\(A\\), so we would 'take away' all the elements, leaving the empty set.

\\(U \setminus A\\) evaluates to \\(\bar A\\). By our definition, this would be all the elements that do not belong to \\(A\\), in other words its complement.

## References:
For further details, you can read through the following chapter:
- [Discrete mathematics - an open introduction part 0.3](http://discrete.openmathbooks.org/dmoi3/sec_intro-sets.html)
