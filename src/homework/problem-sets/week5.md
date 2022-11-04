# Problem Set 5

## Submission

This problem set is due Sunday November 13th at 10pm

- You may collaborate with your peers. If you do, be sure to mention who you 
  collaborated with explicitly in your submission. For example, write "I worked
  with Ope and Mehdi on this problem set" at the top.
- Show your work. Direct answers will not be accepted.

Submit your response in Gradescope, either using the app or the website.

## Problems


1. We flip a coin three times. The set of all possible outcomes is:
\\(\omega = \\{HHH, HHT, HTH, HTT, TTT, TTH, THH, THT\\} \\)

    Each of the following events are subsets of \\(\omega\\). For each event, 
    describe the event in english, then compute the probability of it occuring:

    - \\(E_1 = \\{HHH, TTT\\}\\)
    - \\(E_2 = \\{HHT, THH, HTH\}\\)
    - \\(E_3 = \{HHH, HHT, HTH, HTT\}\\)

2. If A, B, and C are three events, show the following: 

    \\(P( A \cup B \cup C) = P(A) + P(B) + P(C) - P(A \cap B) - P(B \cap C) - P(A \cap B) + P(A \cap B \cap C)\\)

   Hint: You might start by showing the result for just events A and B. It may 
   also help to draw a Venn diagram. 

3. From a deck of five cards numbered 2, 4, 6, 8, and 10, respectively, a card is drawn at random, then placed back in the deck. This is done three times, and you are told that the sum of the numbers on the three draws is 12. What is the probability that the card numbered 2 was drawn exactly two times, given that the sum was 12?

4. One coin in a collection of 65 coins has two heads. The rest are fair. If a coin, chosen at random from the collection and then tossed, turns up heads 6 times in a row, what is the probability that it is the two-headed coin? 

5. You are given two urns and forty balls. Half of the balls are white and half 
  are black. You are asked to distribute the balls between the two urns with no 
  restriction on the number of white or blank in an urn. An urn will be chosen 
  at random, and a ball will be drawn from it at random. 

    How should you distribute the balls in the urns to maximize the probability 
    of drawing a white ball? Justify your answer.

    Extension (optional): Prove your answer. 

    One approach might be to write a Python program that loops through every 
    possible arrangement, calculates the probability of drawing a white ball 
    for each arrangement, and finds the maximum probability.

## References: 

These problems were drawn from chapters 1.2 and 4.1 of [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
