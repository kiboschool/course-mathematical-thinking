# Problem Set 1

## Submission

This problem set is due Sunday October 16th at 10pm

- You may collaborate with up to 1 peer, make sure to include it explicitly in your submission.
- Show your work. Direct answers will not be accepted.

## Problems

1. Make a truth table for the statement  \\(\neg P  \to (Q \wedge R)\\\)

2. Are the statements \\(P \to (Q\vee R)\\) and \\(  (P \to Q) \vee (P \to R) \\) logically equivalent?

3. Use De Morgan's Laws, and any other logical equivalence facts you know to simplify the following statements. Show all your steps. Your final statements should have negations only appear directly next to the sentence variables or predicates (\\(P\\), \\(Q\\),\\(E(x)\\), etc.), and no double negations. It would be a good idea to use only conjunctions, disjunctions, and negations.

    a. \\( \neg((\neg P \wedge Q) \vee \neg(R \vee \neg S)) \\)

    b. \\( \neg((\neg P \to \neg Q) \wedge (\neg Q \to R)) \\) (careful with the implications).

    c. For both parts above, verify your answers are correct using truth tables. That is, use a truth table to check that the given statement and your proposed simplification are actually logically equivalent.

4. Consider the statement, “If a number is triangular or square, then it is not prime”

    a. Make a truth table for the statement \\((T \vee S) \to \neg P\\).

    b. If you believed the statement was false, what properties would a counterexample need to possess? Explain by referencing your truth table.

    c. If the statement were true, what could you conclude about the number 5657, which is definitely prime? Again, explain using the truth table.

5. Tommy Flanagan was telling you what he ate yesterday afternoon. He tells you, “I had either popcorn or raisins. Also, if I had cucumber sandwiches, then I had soda. But I didn't drink soda or tea.” Of course you know that Tommy is the worlds worst liar, and everything he says is false. What did Tommy eat?

    Justify your answer by writing all of Tommy's statements using sentence variables (\\(P\\), \\(Q\\), \\(R\\), \\(S\\), \\(T\\)), taking their negations, and using these to deduce what Tommy actually ate.

    Hint: Write down three statements, and then take the negation of each (since he is a liar). You should find that Tommy ate one item and drank one item. (\\(Q\\) is for cucumber sandwiches.)

6.  Consider the following four cards in the figure. Each card has a letter on one side, and a shape on the other side.

    ![card1: star card 2: triangle card 3: q card 4: diamond](/images/cards.png)

    For each of the following claims, determine (1) the minimum number of cards you must turn over to check the claim, and (2) what those cards are, in order to determine if the claim is true of all four cards.

    a. If there is a \\(P\\) or \\(Q\\) on the letter side of the card, then there is a diamond on the shape side of the card.

    b. If there is a \\(Q\\) on the letter side of the card, then there is either a diamond or a star on the shape side of the card.

7.  Translate the following passage into our propositional logic.  Prove the argument is valid.

    Either Dr. Kronecker or Bishop Berkeley killed Colonel Cardinality.  If Dr. Kronecker killed Colonel Cardinality, then Dr. Kronecker was in the kitchen. If Bishop Berkeley killed Colonel Cardinality, then he was in the drawing room. If Bishop Berkeley was in the drawing room, then he was wearing boots. But Bishop Berkeley was not wearing boots. So, Dr. Kronecker killed the Colonel.

8. Prove whether or not each of the following arguments is valid.

    a. Premises: \\(((P \wedge Q) \iff R), (P \iff S), (S \wedge Q)\\). Conclusion: \\(R\\).

    b. Premises:  \\((P \iff Q)\\). Conclusion:  \\(((P \to Q) \wedge (Q \to P))\\).

    c. Premises: \\(P, \neg Q\\). Conclusion: \\(\neg(P \iff Q)\\).

    d. Premises:  \\(( \neg P \vee Q), (P\vee \neg Q)\\). Conclusion:  \\((P \iff Q)\\).

    e. Premises:  \\((P \iff Q), (R \iff S)\\). Conclusion:  \\(((P \wedge R) \iff (Q \wedge S))\\).

    f. Premises:  \\(((P \vee Q) \iff R), \neg P \iff Q)\\). Conclusion:  R\\).

    g. Conclusion:  \\(((P \iff Q) \iff (\neg P \iff \neg Q))\\)

    h. Conclusion:  \\(((P \to Q) \iff (\neg P \vee Q))\\)

## References

These problems were drawn from:

- [Discrete mathematics - an open introduction (part 3.1)](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
- [A Concise introduction to logic (part 1)](https://open.umn.edu/opentextbooks/textbooks/452)