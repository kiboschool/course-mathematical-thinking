# Probability

## Key ideas

## Intro & Definitions

We talk of odds and chances very often, but rarely in a mathematically sound way! It has become a recent meme of late that any outcome is a 50/50: It either happens or it doesn't. 

As motivating as that statement is, it is far from mathematically accurate. We will get into the fundamentals of probability theory over the next week. As a topic, probability will have us apply our understandings of **Sets**, **Permutations & Combinations**, as well as some proofs. If you feel shaky on any of those topics, make sure take some time to review them, and come through to office hours for support.

Without further ado, let's define some key terms for probability:

- **Experiements:** When an experiment occurs, we obtain **one specific outcome**
- **Sample Space:** The sample space of an experiment is the **set** of all **possible outcomes** of that experiment
- **Event:** This is a subset of the sample space

### Example 1: coin toss
Let's quickly clarify the terms with the simplest experiment I can think of: Flipping a coin.

- Flipping the coin is the **experiment**. The outcome of which will be that we see either heads or tails. 
- Therefore, our **sample space** is $S = \\{H, T\\}$
- We can describe an event $E = \\{H\\}$ to represent that we get heads when we flip our coin.

How does this translate to probabilities? Fundamentally, the Probability of a given event $E$ occuring is equal to $\frac{|E|}{|S|}$

In simpler english, we are looking at the ration of "outcomes that make up the event" to "how many possible outcomes are there" In this case. The probabilit of $E$ is represented as $P(E) = \frac{|E|}{|S|} = \frac{1}{2}$ as expected. 

### Example 2: rolling dice
Let's look at another example: Rolling a six-sided dice. Our sample space is $S = \\{1, 2, 3, 4, 5, 6\\}$

How likely are we to roll an odd number? you'll probably immediately know that it is 50%, but let's apply the new vocabulary we are learning.

Let $E_{odd}\\ = \{1, 3, 5\}$ represent the event that roll an odd number. 

Therefore, $P(E_{odd}) = \frac{|E_{odd}|}{|S|} = \frac{3}{6} = \frac{1}{2}$ as expected.


### Example 3: The lottery!
While it may be helpful to explicitly define the sample space and the subset that makes up a given event. That is not always feasible though, but all we need is figuring out 

Imagine we run a lottery. We will randomly create a sequence of 5 *distinct numbers* between 0 and 9, the winning combination. Participants can submit their own sequence of 5 numbers, and win the big prize if they match the sequence we picked. What is the probability that you win this lottery?

Let $E_{win}$ represent he event that we win the lottery. There is only one winning combination, so $|E_{win}| = 1$. That's the first information we need to get our answer. 

Now what about our **sample space?** Last week has luckily given us the tools needed to compute how many such sequences we can have: We are trying to find how many 5-permutations there are of the 10 numbers we can use. The formula for this is $P(10, 5) = \frac{10!}{10-5!} = 10.9.8.7.6 = 30240$


This allows us to compute that our probability of winning $P(E_{win}) = \frac{1}{30240}$. Not particularly enticing! How about we offer participants a chance to win a lesser price.

We're willing to give a second prize to anyone who guesses the same numbers, but in a different order. Our sample space remains unchanged, but how many outcomes fit our new event, $E_{secondPrize}$? Think about it for a few minutes before proceeding. 

This is a permutation problem. Given a sequence of 5 distinct digits, how many ways do we have to shuffle them? recall from last week that there are 5! different ways to organize 5 elements. So is that representative of $|E_{secondPrize}|$? not quite! 

One of these permutations represents the **winning sequence!** if we pick that one, we'd win the first prize, not the second. Therefore,  $|E_{secondPrize}| = 5! - 1$

This gives us that $P(E_{secondPrize}) = \frac{119}{30240}$ Still not great odds, but 119 times more likely than winning.

## Key theorems:
In this section, we formalize some theorems regarding probability. These will form the basis for you to be able to prove more complex statements regarding probabilities. 

Consider an experiment with sample space $S$

### Theorem 1:
$P(E) \ge 0 \forall E \subset S$. 

Probabilities can never be negative by definition, as the cardinality of a set is always greater than or equal to 0.

### Theorem 2:
$P(S) = 1$. 

This is trivially shown from the formula for computing probabilities, as $\frac{|S|}{|S|} = 1$. In other words. The probability of any of the possible outcomes happening is 1. This also makes up the upper bound of what the probability of any event can be. 

### Theorem 3:
***if*** $E \subset F \subset S$***, then*** $P(E) \le P(F) $. 

This follows from the fact that given that E is a subset of F, $|E| \le |F|$


In the next section, we will look at computing the probabilities of multiple events at the same time, connected by a logical connector.

## Probability Spaces Video

<div style="position: relative; padding-bottom: 59.73451327433629%; height: 0;"><iframe src="https://youtube.com/embed/0L_srQfYtNc" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## References

Chapters 1.1 and 1.2 of [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
