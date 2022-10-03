# Connectors part 1: And/Or:

## Key ideas:
- Introduce the concept of truth tables
- Introduce the truth table and notation for And
- Introduce the truth table and notation for Or

## And:
The first connector we will discuss is ***AND***. We use it often to connect propositions - "I am tired ***AND*** I am happy" - but let's formalize our understanding of it. Firt, in propositional logic, we often use a specific symbol to indicate ***AND*** rather than writin the word over and over again. The symbol for AND is \\(\land). So you should be able to interpret I am tired \\(\land) I am happy the same way as the above sentence.

Let \\(\mathbb P), \\(\mathbb Q) be two propositions. Instinctively, we have a sense for what \\(\mathbb P) \\(\land) \\(\mathbb Q) mean, but let's formalize it! remember that our key objective is to be very specific. This might be easier to reason about with concrete examples so:
- Let \\(\mathbb P) be the proposition "You are reading this on your phone"
- Let \\(\mathbb Q) be the proposition "You are listening to music"

How many scenarios do we have to consider? Well P can be either True or False, so that's two different values. Same for Q. So all together we have 4 scenarios:
- Both P, Q are True. \\(\mathbb P) \\(\land) \\(\mathbb Q) is therefore True
- P is True and Q is False. \\(\mathbb P) \\(\land) \\(\mathbb Q) is False
- P is False and Q is True. \\(\mathbb P) \\(\land) \\(\mathbb Q) is False
- Both P, Q are False. \\(\mathbb P) \\(\land) \\(\mathbb Q) is False

We will typically condense this information in what is called as a *truth table*:

| \\(\mathbb P) | \\(\mathbb Q) | \\(\mathbb P) \\(\land) \\(\mathbb Q) |
| ------------ | -------------| -----------------------------------|
| True | True | True |
| True | False | False | 
| False | True | False | 
| False | False | False | 

So to summarize, \\(\mathbb P) \\(\land) \\(\mathbb Q) is only True if and only if both \\(\mathbb P) and \\(\mathbb Q) are True.

## Or:

- Let \\(\mathbb P) be the proposition "You are reading this on your phone"
- Let \\(\mathbb Q) be the proposition "You are reading this on your computer"

Let's jump straight ahead and define our symbol for Or to be \\(\lor). So expressing  "you are reading this on your phone or your computer" can be condensed to the proposition \\(\mathbb P) \\(\lor) \\(\mathbb Q). 

We build up our truth table:

| \\(\mathbb P) | \\(\mathbb Q) | \\(\mathbb P) \\(\lor) \\(\mathbb Q) |
| ------------ | -------------| -----------------------------------|
| True | True | True |
| True | False | True | 
| False | True | True | 
| False | False | False | 

## Priority:
Let's consider the following proposition: \\(\mathbb P) \\(\land) \\(\mathbb Q) \\(\lor) \\(\mathbb R). How would we interpret this?

Well we know that \\(\mathbb P) \\(\land) \\(\mathbb Q) is a proposition, so we could evaluate it first, then combine it with the remaining \\(\lor) \\(\mathbb R) part.

But similarly, \\(\mathbb Q) \\(\lor) \\(\mathbb R) is also a valid proposition we could evaluate first. How do we prioritize? 

By default, note that \\(\land) has a higher priority than \\(\lor). This means that the first interpretation above is the correct and expected one. 
This is similar to basic algebra: If you see the expression *2 x 3 + 1* you should evaluate it as 7, not 8, as multipication has a higer priority. If you wanted to make sure the addition happened first, you could use parenthesis to indicate it. so *2 x (3 + 1)* is equal to 8

You can similarly use parenthesis in propositional logic. So we have that:
-  \\(\mathbb P) \\(\land) \\(\mathbb Q) \\(\lor) \\(\mathbb R) is equivalent to  (\\(\mathbb P) \\(\land) \\(\mathbb Q)) \\(\lor) \\(\mathbb R) since \\(\land) has higher priority.
-  \\(\mathbb P) \\(\land) (\\(\mathbb Q) \\(\lor) \\(\mathbb R)) is a different proposition altogether, as now prioritize the \\(\lor)

but don't take my word for it. Let's show this using truth tables. Two statements are equivalent if their respective truth tables are the same. Let's take a moment and fill up the table below and see if our statements are the same or different. Give it a shot for a few minutes before consulting the answer.

| \\(\mathbb P) | \\(\mathbb Q) | \\(\mathbb R) | \\(\mathbb P) \\(\land) \\(\mathbb Q) \\(\lor) \\(\mathbb R) | \\(\mathbb P) \\(\land) (\\(\mathbb Q) \\(\lor) \\(\mathbb R)) |
| ------------ | -------------| -----------------------------------|
| True | True | True | | |
| True | True | False | | |
| True | False | True | | |
| True | False | False | | |
| False | True | True | | |
| False | True | False | | |
| False | False | True | | |
| False | False | False | | |

<details>answer:

| \\(\mathbb P) | \\(\mathbb Q) | \\(\mathbb R) | \\(\mathbb P) \\(\land) \\(\mathbb Q) \\(\lor) \\(\mathbb R) | \\(\mathbb P) \\(\land) (\\(\mathbb Q) \\(\lor) \\(\mathbb R)) |
| ------------ | -------------| -----------------------------------|
| True | True | True | True| True |
| True | True | False | True | True |
| True | False | True | True | True |
| True | False | False | False | False |
| False | True | True | True | False |
| False | True | False | False | False |
| False | False | True | True | False |
| False | False | False | False| False |

As you can tell, the fourth and fifth columns are different, so the two statements are *not* equivalent. You can use truth tables to assess if two propositions are the same by simply showing that they evaluate the 
</details>

We will continue looking at connectors in the next section.

## References:

For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.5 and 1.7](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)

