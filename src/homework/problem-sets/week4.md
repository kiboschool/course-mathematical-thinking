# Problem Set 4

## Submission

This problem set is due Sunday November 6th at 10pm

- You may collaborate with up your peers. If you do, be sure to mention who you 
  collaborated with explicitly in your submission. For example, write "I worked
  with Ope and Mehdi on this problem set" at the top.
- Show your work. Direct answers will not be accepted.

Submit your response in Gradescope, either using the app or the website.

## Problems

1. The door to a building has a lock which has 5 buttons numbered from 1 to 5. The combinations of numbers that opens the lock is a sequence of 5 numbers and is reset every week.
   
   a. How many combinations are possible if every button must be used once?
   
   b. Assume that the lock can also have combinations that require you to push 2 buttons simultaneously, and then the other three one at a time. How many combinations does this permit? To clarify, in a sequence of 5 buttons, 2 consecutive buttons **must** be pressed at the same time to be considered correct.

1. A computer has 3 processors that receive *n* tasks. Tasks are assigned to the processors purely at random, meaning that all 3^n possible assignments are equally likely. What is the probability that exactly one processor has no tasks assigned?
2. Find a formula for the probability that among a set of *n* people, at least two have their birthday in the same month. (Assuming the months are equally likely for birthdays)
3. In how many ways can we choose five people from a group of ten to form a basketball team?
4. How many 7-element subsets are there in a set of nine elements?
5. A poker hand is a set of 5 cards randomly chosen from a deck of 52 cards. Find the probability of a:
   6. Royal flush (ten, jack, queen, king, ace of a single suit)
   7. Straight flush (five in a sequence in a single suit, but not a royal flush)
   8. Four of a kind (4 cards of the same face value. The fifth card is not relevant)
   9. Full house (one pair and one triple)
   1. Flush (5 cards of the same suit, but not a straight flush or royal flush)
   2. Straight (5 cards in a sequence, but not all of the same suit) 
6. Someone wants to color their fingernails on one hand using at most 2 of the colors red, yellow, and blue. How many ways can they do this?
7. Assume that you are interviewing candidates for a job. As you interview a candidate, you must immediately decide if you are hiring the candidate or reject them. Once you hire a candidate, you interviewing. Once you reject a candidate, they immediately get another job and you can not go back to hire them. 

Candidates all have a skill ranking, so there is an objectively strongest candidate. For example if you see 5 candidates, they would be ranked from 1 to 5, and show up in a random order. So you might see candidate with rank 3, then 2, then 4, then 1, then 5. 

Assume that there are *n* candidates that show up in random order of skill.
   1. What is the probability that you hire the best candidate if you interview ALL *n* candidates?
   2. What is the probability that you hire the best candidate if you hire the first candidate you interview?
   3. Let's consider a different strategy: We will interview and reject the first half of candidates, then whenever we find a candidate in the second half with a better score, we will pick them. Show that there is **at least** a 25% chance that this strategy identifies the best candidate.




## References:
These problems were drawn from chapter 3 of [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
