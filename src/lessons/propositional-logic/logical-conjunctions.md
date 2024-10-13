# Connectors part 1: And/Or:

## Key ideas:
- Introduce the concept of truth tables.
- Introduce the truth table and notation for And.
- Introduce the truth table and notation for Or.

## And:
The first connector we will discuss is ***AND***. We use it often to connect propositions - "I am tired ***AND*** I am happy" - but let's formalize our understanding of it. First, in propositional logic, we often use a specific symbol to indicate ***AND*** rather than writin the word over and over again. The symbol for AND is $ \land $. So you should be able to interpret I am tired $ \land $ I am happy the same way as the above sentence.

Let $ P$, $ Q$ be two propositions. Instinctively, we have a sense for what $ P \land  Q$ mean, but let's formalize it! remember that our key objective is to be very specific. This might be easier to reason about with concrete examples so:
- Let $ P$ be the proposition "You are reading this on your phone"
- Let $ Q$ be the proposition "You are listening to music"

How many scenarios do we have to consider? Well P can be either True or False, so that's two different values. Same for Q. So all together we have 4 scenarios:
- Both P, Q are True. $ P \land  Q$ is therefore True
- P is True and Q is False. $ P \land  Q$ is False
- P is False and Q is True. $ P \land  Q$ is False
- Both P, Q are False. $ P \land  Q$ is False

We will typically condense this information in what is called as a *truth table*:

| $ P$ | $ Q$ | $ P \land  Q$ |
| ------------ | -------------| -------------------------|
| True | True | True |
| True | False | False | 
| False | True | False | 
| False | False | False | 

So to summarize, $ P \land  Q$ is only True if and only if both $ P$ and $ Q$ are True.

## Or:

- Let $ P$ be the proposition "You are reading this on your phone"
- Let $ Q$ be the proposition "You are reading this on your computer"

Let's jump straight ahead and define our symbol for Or to be $\lor$. So expressing  "you are reading this on your phone or your computer" can be condensed to the proposition $ P \lor  Q$. 

We build up our truth table:

| $ P$ | $ Q$ | $ P \lor  Q$ |
| ------------ | -------------| -----------------------------------|
| True | True | True |
| True | False | True | 
| False | True | True | 
| False | False | False | 

## Priority:
Let's consider the following proposition: $ P \land  Q \lor  R$. How would we interpret this?

Well we know that $ P \land  Q$ is a proposition, so we could evaluate it first, then combine it with the remaining $\lor  R$ part.

But similarly, $ Q \lor  R$ is also a valid proposition we could evaluate first. How do we prioritize? 

By default, we note that $\land$ has a higher priority than $\lor$. This means that the first interpretation above is the correct and expected one. 
This is similar to basic algebra: If you see the expression *2 x 3 + 1* you should evaluate it as 7, not 8, as multipication has a higer priority. If you wanted to make sure the addition happened first, you could use parenthesis to indicate it. so *2 x (3 + 1)* is equal to 8

You can similarly use parenthesis in propositional logic. So we have that:
- $ P \land  Q \lor  R$ is equivalent to  $( P \land  Q) \lor  R$ since $\land$ has higher priority.
-  $ P \land ( Q \lor  R)$ is a different proposition altogether, as now prioritize the $\lor$

but don't take my word for it. Let's show this using truth tables. Two statements are equivalent if their respective truth tables are the same. Let's take a moment and fill up the table below and see if our statements are the same or different. Give it a shot for a few minutes before consulting the answer.

| $ P$ | $ Q$ | $ R$ | $ P \land  Q \lor  R$ | $ P \land ( Q \lor  R)$ |
| ------------ | -------------| -----------------------------------|--|---| 
| True | True | True | | |
| True | True | False | | |
| True | False | True | | |
| True | False | False | | |
| False | True | True | | |
| False | True | False | | |
| False | False | True | | |
| False | False | False | | |

What you should see is that the fourth and fifth columns are different, so the two statements are *not* equivalent. You can use truth tables to assess if two propositions are the same by simply showing that they evaluate the same way in a table. Make sure to fill it up entirely before looking at the solution below.


| $ P$ | $ Q$ | $ R$ | $ P \land  Q \lor  R$ | $ P \land ( Q \lor  R)$ |
| ------------ | -------------| -----------------------------------|--|---| 
| True | True | True | True| True |
| True | True | False | True | True |
| True | False | True | True | True |
| True | False | False | False | False |
| False | True | True | True | False |
| False | True | False | False | False |
| False | False | True | True | False |
| False | False | False | False| False |

We will continue looking at connectors in the next section.

## Video on Conjunction Disjunction and Negation

<div style="position: relative; padding-bottom: 59.73451327433629%; height: 0;"><iframe src="https://youtube.com/embed/LO4lFX4Ur2Q" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>


## References:

For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.5 and 1.7](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
