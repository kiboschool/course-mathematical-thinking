# Conditional Probability

## Key ideas
- Introduce the concept of dependents and independent events
- Define the formula for conditional probability and how it is affected by independent events

## Do these events matter?
Picture this. Your team has been competing with a rival school for many years now, and you have been keeping track diligently of your wins and losses. Your team's record so far is that you have won 70 games and lost 50. With this in mind, you are confident to head into the next game.

One of your older classmates however is not as confident, and she says that "Mr.O will be the referee this time around, he doesn't like us". This leaves you exceedingly curious. Time to go back to your data and see if the referee really influences your chances to win:

|Referee|# of wins|# of losses| Total |
|-|-|-|-|
|Mr C.|20|8|**28**|
|Mr O.|6|12|**18**|
|Mr S.|44|20|**64**|
|**Total**|70|50| **120**|

Our overwall probabilities to win are quite clear: $P(Winning) = \frac{70}{120}$, or approximately 0.58.  The question is: Is our chance of winning independent on who is the referee? or does our chance of winning **depend** on who will be the referee for the game?

Let's pause for a second to start some definition. We can represent the probability that an event $E$ occurs *given* an event $F$ by the notation $P(E|F)$ 

We say then that two events $E$ and $F$ are independent if $ P(E) = P(E|F)$. In other words, whether or not the event $F$ occurs, the probability of $E$ happening is unchanged.

Conversely, if $ P(E) \neq P(E|F)$, then the two events are dependent - $F$ can influence $E$, and vice versa.

Let's go back to our example above. What is **P(Winning | Mr.O is the referee)**? We do not have a set formula for this *yet*, but let's think about it. We have played a total of 18 games refereed by Mr.O, and won 6. The chances of us winning based on this data are therefore **P(Winning | Mr.O is the referee)** = $\frac{6}{18} = \frac{1}{3} $, noticeably lower than our overall 58% winrate!

This suggests that our two events, Winning and having Mr. O as our referee, are **depedent!** 

Let's dip now into the more theoretical aspects of conditional probability so that we can establish a general formula for it.

## Conditional probability

Start by watching [this video](https://www.youtube.com/watch?v=bgCMjHzXTXs&ab_channel=jbstatistics) on the fundamentals of Conditional probability. This will visually show where the formula comes from, as well as offer several practice problems.

### Conditional probability formula
The probability of event $E$ given event $F$ is computed as $ P(E|F) = \frac{P(E \cap F)}{P(F)}$, given that $P(F) \neq 0$

### Independence test
If $A$ and $B$, with $P(A) \neq 0$ and $P(B) \neq 0$, are independent then the following statements are equivalent: 

1. $P(A) = P(A|B)$
2. $P(B) = P(B|A)$
3. $P(A)P(B) = P(A \cap B)$

We can reach the second statement from the first as follows: 

$P(A) = \frac{P(A \cap B)}{P(B)}$ by definition of conditional probability

$P(B) = \frac{P(A \cap B)}{P(A)}$ given that both $P(A)$ and $P(B)$ are non-zero

$P(B) = P(B|A)$ by definition of conditional probability

And similarly, we can reach the third statement from the first: 

$P(A) = \frac{P(A \cap B)}{P(B)}$ by definition of conditional probability

$P(A)P(B) = P(A \cap B)$

The reason we take time to explicitly show that these three statements are equivalent is to offer you flexibility in how to approach problems involving checking for independence and computing conditional probability

### Independence and complements

If $A$ and $B$ are independent events, it follows that $A$ and $\bar B$ are independent as well. 

Intuitively this should make sense: If $A$ occuring does not influence $B$, then it shouldn't influence $\bar B$. If $P(B)$ doesn't change given $A$ then neither should $1-P(B)$

We can prove this statement directly:

$P(A)P(B) = P(A \cap B)$ by definition of independence

$P(A)(1-P(\bar B)) = P(A \cap B)$ by definition of complement

$P(A) - P(A)P(\bar B) = P(A \cap B)$

$P(A) - P(A \cap B) = P(A)P(\bar B)$

How can we evaluate $P(A) - P(A \cap B)$? This expression represents the probability of event $A$ occuring, minus the probability of event $A$ and $B$ occuring. From a set perspective, this means we care only about the outcomes that belong to $A$ but do not belong to $B$. This can be expressed as $P(A \cap \bar B)$. 

Therefore, $P(A)P(\bar B) = P(A \cap \bar B)$

And thus, we have shown that $A$ and $\bar B$ are independent.

Symmetrically, we can use the same approach to show that $ \bar A$ and $B$ are independent, as well as $\bar A$ and $\bar B$ 

In the next section, we bring all our knowledge together in a case study, and see how we can use code to help us hone our intuition with probabilities.


## References:

Chapter 4 of [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
