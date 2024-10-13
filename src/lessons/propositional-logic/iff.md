# Connectors part 3: If and Only If

## Key Ideas:
- Defining if and only if in terms of an implication and its converse
- Defining the truth table of if and only if relationships

## Biconditionals:

Intuitively, we should see that the two following propositions have a different meaning:
- If the DJ is playing Jerusalema, then Zainab is not on the dancefloor
- If and only if the DJ is playing Jerusalema, then Zainab is not on the dancefloor

Adding the *only if* wording doesn't only make the sentence sound more dramatic, it changes it makes it more strict: The *only* means that no other song will prevent Zainab from being on the dancefloor. She won't stop if she's tired. The only way Zainab is not on the dancefloor is if, and only if, the DJ plays Jerusalema. 

This is stricter than the simple implication. In fact, another way to reason about "if and only if" - also known as *biconditional* statements - is that they are true when an implication **and its converse are true**

Let's consider the following truth table:

| $ P$ | $ Q$ | $ P \to  Q$| $ Q \to  P$ | $( P \to  Q) \land ( Q \to  P)$ |
| ------------ | -------------| -----------------------------------|--------|-------|
| True | True | True | True | True | 
| True | False | False | True | False | 
| False | True | True | False | False | 
| False | False | True |  True | True |


Thinking through this in english we have:
- An implication: If the DJ is playing Jerusalema, then Zainab is not on the dancefloor
- Its converse: If Zainab is not on the dancefloor, then the DJ is playing Jerusalema

When both are true, we can say that "If and only if the DJ is playing Jerusalema, then Zainab is not on the dancefloor". This is why we call this kind of statement "biconditional", as they are the combination of two "conditional" statements. 

Let's simplify our truth table and introduce the formal statement for biconditionals: $\iff$

| $ P$ | $ Q$ | $ P \iff  Q$| 
| ------------ | -------------| -----------------------------------|
| True | True |  True | 
| True | False | False | 
| False | True | False | 
| False | False | True |

### Priority

$\iff$ shares the same priority as $\to$

We have covered all our connectors now! so our final priority order is:
1- $\lnot$
2- $\land$
3- $\lor$
4- $\to  ,  \iff$

## Video on Equivalent Propositions

<div style="position: relative; padding-bottom: 59.73451327433629%; height: 0;"><iframe src="https://youtube.com/embed/glYNeV14xqg" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>


## References:
For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.9](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
