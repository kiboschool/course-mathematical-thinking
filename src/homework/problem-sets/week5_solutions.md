# Problem Set 5 Solutions



1. We flip a coin three times. The set of all outcomes can be described as:
\\(\omega = \{HHH, HHT, HTH, HTT, TTT, TTH, THH, THT\}\\)
For each of the following events which are subests of \\(\omega\\), describe the event in english, then compute the probability of it occuring:
  - \\(E_1 = \{HHH, TTT\}\\)

  This is the event that all coin tosses are the same. \\(P(E_1) = \frac{1}{4}\\)

  - \\(E_2 = \{HHT, THH, HTH\}\\)
  
  This is the event that we toss exactly two H. \\(P(E_2) = \frac{3}{8})
  
  - \\(E_3 = \{HHH, HHT, HTH, HTT\}\\)
  

  This is the event that our first toss is an H. \\(P(E_3) = \frac{1}{2})

  
2. If A, B, and C are three events, show that:
\\(P( A \cup B \cup C) = P(A) + P(B) + P(C) - P(A \cap B) - P(B \cap C) - P(A \cap B) + P(A \cap B \cap C)\\)

This is equivalent to showing that \\(|A \cup B \cup C| = |A| + |B| + |C| - |A \cap B| - |B \cap C| - |A \cap B| + |A \cap B \cap C|\\)


We can start by defininig the set \\(S = A \cup B\\). It follows that \\(|S| = |A \cup B| =  |A| + |B| - |A \cap B|\\) per our class notes

So our initial statement \\(|A \cup B \cup C| = |S \cup C|\\)

By our notes, \\(|A \cup B \cup C| = |S| + |C| - |S \cap C| \\)

Plugging in |S| we get \\(|A \cup B \cup C| =  |A| + |B| - |A \cap B| + |C| - |(A \cup B) \cap C| \\)

Note that \\((A \cup B) \cap C\\) is logically equivalent to \\((A \cap C) \cup (B \cap C)\\)

\\(|(A \cup B) \cap C| = |(A \cap C) \cup (B \cap C)| = |A \cap C| + |B \cap C| - |A \cap C \cap B|\\)

Plugging this into our previous equation we obtain: 

\\(|A \cup B \cup C| =  |A| + |B| - |A \cap B| + |C| - (|A \cap C| + |B \cap C| - |A \cap C \cap B|) \\)

Therefore, we have shown that \\(|A \cup B \cup C| =  |A| + |B| + |C| - |A \cap B| - |B \cap C| - |A \cap B| + |A \cap B \cap C|\\)

It follows from the definition of probability that \\(P( A \cup B \cup C) = P(A) + P(B) + P(C) - P(A \cap B) - P(B \cap C) - P(A \cap B) + P(A \cap B \cap C)\\)


3. From a deck of five cards numbered 2, 4, 6, 8, and 10, respectively, a card is drawn at random and replaced. This is done three times. What is the probability that the card numbered 2 was drawn exactly two times, given that the sum of the numbers on the three draws is 12?


Let \\(S\\) be our sample space. 

Let \\(E\\) be the event that we draw the number 2 exactly two times.

Let \\(F \\) be the event that the sum of the three cards drawn is 12

\\(E \cap F = {(2,2,8), (2,8,2), (8,2,2)} be the event that we draw the number 2 exactly two times and we reach a sum of 12 \\)

We can now compute \\(P(E | F) = \frac{P(E \cap F)}{P(F)} \\)

\\(P(E | F) = \frac{|E \cap F|}{|S|} . \frac{|S|}{|F|} \\)
\\(P(E | F) = \frac{|E \cap F|}{|F|}\\)

How do we compute |F|? There are three ways of adding up 3 of the numbers provided and obtaining 12. As we've seen, we can add 2,2, and 8. This gives us 3 permutations. 

We have that 4+4+4 = 12, so drawing the number 4 three times in a row gives us one additional outcome. 

Finally, we also have 2+4+6 = 12. there are 3! = 6 ways to rearrange those numbers, so that gives us 6 additional outcomes.

Therefore, |F| = 3+1+6 = 10

\\(P(E | F) = \frac{|E \cap F|}{|F|} = \frac{3}{6}\\)


4. One coin in a collection of 65 has two heads. The rest are fair. If a coin, chosen at random from the lot and then tossed, turns up heads 6 times in a row, what is the probability that it is the two-headed coin? 

Let \\(P(2H) = \frac{1}{65}\\) be the probability that we pick the coin with two heads. Note that if we use that coin, our probability of tossing 6 heads in a row is 100%.

Let \\P(6inRow)\\) be the probability we toss 6 heads in a row. We are guaranteed to toss 6 heads if we pick the unfair coin. If we pick a fair coin, the probability of tossing 6 heads is \\((\frac{1}{2})^6\\). This gives us that \\(P(6inRow) = \frac{1}{65} + \frac{64}{65}.\frac{1}{2})^6\\)

Plugging in the values, we get \\(P(6inRow) = \frac{2}{65}\\)

We can now compute the conditional probability: \\(P(2H | 6inRow) = \frac{P2H \cap 6inRow}{P(6inRow)}\\)

\\(P(2H | 6inRow) = \frac{\frac{1}{65}}{\frac{2}{65}}\\)

\\(P(2H | 6inRow) = \frac{1}{2}\\)


5. You are given two urns and forty balls. Half of the balls are white and half are black. You are asked to distribute the balls in the urns with no restriction placed on the number of either type in an urn. How should you distribute the balls in the urns to maximize the probability of obtaining a white ball if an urn is chosen at random and a ball drawn out at random? Justify your answer.

Let's start by finding a formula for \\(E\\), the event of getting a white ball from a randomly chosen urn:

\\(P(E) = P(choose urn 1)P(pick white from urn 1) + P(choose urn 2)P(pick white from urn 2)\\)

Since we pick the urns randomly, so \\(P(E) = \frac{P(pick white from urn 1)}{2} + \frac{P(pick white from urn 2)}{2}\\)

What happens if we split the balls evenly, so each urn has 10 white ones and 10 black ones:

- \\(P(pick white from urn 1) = P(pick white from urn 2) = \frac{10}{20} = \frac{1}{2}\\)

This gives us that \\(P(E) = \frac{1}{4} + \frac{1}{4} = \frac{1}{2}\\)

What happens if we move one white ball from urn 1 to urn 2? We get that:

- \\(P(pick white from urn 1) = \frac{9}{19}\\)
- \\(P(pick white from urn 2) = \frac{11}{21}\\)

In this scenario, we can compute that \\(P(E) = 0.498\\). Our likelihood went down! You can continue shifting white balls to a different urn, and the probability will keep worsening. 

How about we put all our white balls in urn 1, and all the black ones in urn 2?

- \\(P(pick white from urn 1) = 1\\)
- \\(P(pick white from urn 2) = 0\\)

This gives us \\(P(E) = \frac{1}{2}\\)

At this point though, what happens if we move a white ball from urn 1 to urn 2? The probability that we pick white from urn 1 remains 1, but we improve the probability of picking a white ball from urn 2.

What is the minimum number of white balls we can put in urn 1 and still have a probability of 1 to draw a white ball? well we can make urn 1 contain a single white ball. This gives us:

- \\(P(pick white from urn 1) = 1\\)
- \\(P(pick white from urn 2) = \frac{19}{39}\\)

Which gives us \\(P(E) = \frac{1}{2} + \frac{19}{78} = 0.7436\\)

This is the best possible odds, because \\(\frac{19}{39}\\) are the best odds we can get on one urn, while keeping the other urn at 100% chance.

## References: 

These problems were drawn from chapters 1.2 and 4.1 of [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
