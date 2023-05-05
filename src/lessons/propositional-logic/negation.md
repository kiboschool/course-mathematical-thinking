# Connectors part 2: Implication and Negation

## Key ideas:
- Introduce the truth table and notation for implications
- Show De Morgan's law

## Negation

This is the most straightforward connector. \\(\lnot\\), also known as the ***NOT*** operator, simply changes the value of a proposition to its opposite. For example if we have \\( P\\): Zainab is on the dancefloor, then \\(\lnot P\\) is the proposition Zainab is *not* on the dancefloor. This leads to the very straightforward Truth table:


| \\( P\\) | \\(\lnot  P\\) |
| ------------ | -------------|
| True | False |
| False | True |

## Negating complex propositions

As easy as it is to apply \\(\lnot\\) to a single proposition, how do we apply it to more complex ones where other operators are involved? well, let's set up our initial truth table.
	
| \\( P\\) | \\( Q\\) | \\( P \land  Q\\)| \\(\lnot(P \land  Q)\\) | 
| ------------ | -------------| -------------|--|
| True | True | True | False | 
| True | False | False | True |
| False | True | False | True |
| False | False | False |  True | 

The above follows the simple rules we've established so far, but is there a way to simplify that proposition? Let's think about it with an example:
 - Let \\(P\\) be the proposition "The learner finished the problem set"
 - and Let \\(Q\\) be the proposition "The learner is taking a nap"

 When we say \\(\lnot(P \land  Q)\\), we mean that it is **not** the case that the learner finished the problem set **and** that the learner is taking a nap. This means that at least one of the two propositions within *must be False*. This is in line with what we saw in the truth table above. At least one of the two propositions being false means that \\(P\\) is false **or** \\(Q\\) is false. Let's explore the new truth table below:

| \\( P\\) | \\( Q\\) | \\( \lnot P\\) | \\(\lnot Q\\)| \\( (\lnot P \lor  \lnot Q)\\) | 
| ------------ | -------------| -----|--|---|
| True | True | False | False | False | 
| True | False | False | True | True |
| False | True | True | False | True |
| False | False | True |  True | True |

Notice that the last column of this truth table looks exactly the same as the last column of the prior one, leading us to state that \\(\lnot(P \land  Q)\\) and \\( (\lnot P \lor  \lnot Q)\\) are **equivalent**

This is refered to De Morgan's law, and will be very handy for us throughout the rest of the term. Note that this also applies the other way around:

\\(\lnot(P \lor  Q)\\) and \\( (\lnot P \land  \lnot Q)\\) are **equivalent**. Can you convince yourself that it is the case?

These two equivalences 
> \\(\lnot(P \lor  Q)\\) equivalent to \\( (\lnot P \land  \lnot Q)\\)

> \\(\lnot(P \land  Q)\\) and \\( (\lnot P \lor  \lnot Q)\\)

are called **De Morgan's Laws**

### Priority:
\\(\lnot\\) has the highest priority of all operations we will cover, so it will be evaluated before anything else. 

## References:

For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.2](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
