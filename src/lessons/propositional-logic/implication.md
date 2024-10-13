# Connectors part 2: Implication and Negation

## Key ideas:
- Introduce the truth table and notation for implications
- Define inverse, converse, and contrapositive.

## Implications:
This is one of the more natural sentences for us to consider. If this, then that! This kind or proposition is often refered to as an *implication*. Let's consider one we've seen before:

> If the DJ is playing Jerusalema, then Zainab is not on the dancefloor

Let $ P$ be "The DJ is playing Jerusalema". In the context of implications, this first proposition is refered to as **the hypothesis**
Let $ Q$ be "Zainab is not on the dancefloor". In the context of implications, the proposition that occurs after the hypothesis is **the conclusion**

We can denote the same sentence above now with the shorthand. $ P \to  Q$.

Let's try to build up our truth table. This one is not as straighforward so we will do it step by step.

| $ P$ | $ Q$ | $ P \to  Q$ |
| ------------ | -------------| -----------------------------------|
| True | True |  |
| True | False |  | 
| False | True |  | 
| False | False |  | 


If $ P$ is True, and $ Q$ is true, that means the DJ is playing Jerusalema, and Zainab is not the dancefloor. This is in line with our implication, so we should consider the implication True in this case.

What about the second scenario? The DJ is playing Jerusalema, but Zainab is still on the dancefloor! This situation contradicts our implication, so if that's the case, our implication is false.

| $ P$ | $ Q$ | $ P \to  Q$ |
| ------------ | -------------| --------------------------------|
| True | True | True |
| True | False | False | 
| False | True |  | 
| False | False |  | 

Let's look at our third scenario: The DJ is not playing Jerusalema, and Zainab is not on the dancefloor. How does this information influence our assessment of the initial implication? Think about it for a few moments before proceeding. 

I would argue that in this case, our implication remains True. This scenario gives us no infromation that invalidate it. Let's look at another example to emphasize this. 

- Let $ R$: *x* is a multiple of 4
- Let $ S$: *x* is a multiple of 2

Consider $ R \to  S$ - or in other words if *x* is a multiple of 4, then *x* is a multiple of 2. Intuitively, we know this to be True (although we can formally prove statements like this in a few weeks!)

So what about a scenario where *x* is equal to 6? In this case $ R$ is False, 6 is not a multiple of 4. However, $ S$ is True, as 6 is an even number. Is this a valid reason to no longer think that our implication is True? it isn't!

So we can update our truth table 

| $ P$ | $ Q$ | $ P \to  Q$|
| ------------ | -------------| -------------------------------|
| True | True | True |
| True | False | False | 
| False | True | True | 
| False | False |  | 

Similarly, we can conclude that the final scenario should also evaluate to True. Consider the scenario where *x* is 5. $ R$ and $ S$ are both False, but does that change anything to the truth of our initial statement $ R \implies  S$ ? It does not! So to conclude our truth table for implications is

| $ P$ | $ Q$ | $ P \to  Q$|
| ------------ | -------------| -----------------------------------|
| True | True | True |
| True | False | False | 
| False | True | True | 
| False | False | True | 

This may seem counterintuitive to you at a glance. The key idea here is not to consider implications as *more strict* than they are: They simply say that the *conclusion* will always follow *the hypothesis*, but there may be other scenarios where the conclusion is True. The only way an implication is false is by showing that *the hypothesis is True* and *the conclusion is False* 

We will look at some more strict connectors than implication in the next few sections. For now though, let's move on to a very simple one. 

## Converse, Inverse, Contrapositive

Given an implication $ P \to  Q$, we can derive 3 related propositions:

1- The **converse** of our implication is $ Q \to  P$ - Our initial hypothesis and conclusion swap.

2- The **inverse** of our implication is $\lnot  P \to \lnot  Q$ - if they hypothesis is not true then the conclusion is not true.

3- The **contrapositive** of our implication is $\lnot  Q \to \lnot  P$ - if the conclusion is not true, then the hypothesis is not true.

Let's find the converse, inverse, and contrapositive of our first implication: "If the DJ is playing Jerusalema, then Zainab is not on the dancefloor
"

- The *converse* is: If Zainab is not on the dancefloor, then the dj is playing Jerusalema.
- The *inverse* is: If the dj is not playing Jerusalema, then Zainab is on the dancefloor.
- The *contrapositive* is: If Zainab is on the dancefloor, then the dj is not playing Jerusalema.

Let's build up the truth tables for each of these new propositions. Try it yourself before seeing the answer below:

<details>answer:
	
| $ P$ | $ Q$ | $ P \to  Q$| $ Q \to  P$ | $\lnot  P \to \lnot  Q$|$\lnot  Q \to \lnot  P$ |
| ------------ | -------------| -----------------------------------|--|--|--|
| True | True | True | True | True | True |
| True | False | False | True | True | False |
| False | True | True | False | False | True |
| False | False | True |  True | True | True |

</details>

What do you notice? Which of these forms are equivalent to each other? Your tables should indicate that the inverse and conerse are equivalent, and that an implication and its *contrapositive* are equivalent. We will use this fact next week!

### Priority:
$\to$ has the lowest priority, so $\land$ and $\lor$ will always be evaluated before it, unless parenthesis change that.
$\lnot$ has the highest priority, so it will be evaluated before anything else. 


## VIdeo on implication and biconditional

<div style="position: relative; padding-bottom: 59.73451327433629%; height: 0;"><iframe src="https://youtube.com/embed/9AOt6w4cKZI" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## References:

For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.2](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
