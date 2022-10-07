# Intro to proofs

## Key Ideas:
- Defining the general idea of a proof
- Showcasing how direct proofs of implication are crafted

## Anatomy of a proof:
You may have experienced conversations or watched debates where someone is trying to make a point, and it ends up feeling a bit like the following image:

![Then a Miracle Occurs. Copyrighted artwork by Sydney Harris Inc.](/images/miracle.png)

We want to learn to identify sound arguments and valid proofs from those that are less so. So how do we define a proof in our context? Well it has a few elements:
- First, we have a *hypothesis*: This is the statement we want to prove is True.
- Secondly, we have *theorems*: Statements that are *already established to be True*. These may be given to you in the context of the proof you are trying to make, or be topics that are established in mathematics. All in all, you can rely on theorems without needing additional proofs. 

Using established *theorems*, i.e True statements, we want to build a sequence of valid implications, which ultimately build into our hypothesis being True. If this sounds somewhat vague, let's look at a simple example. 

Here is some information we know - these are our theorems in this context:
- DJ Naoufal plays music from the opening of the club until 2 am
- DJ Naoufal never plays R&B

Our *Hypothesis*, the statement we want to prove, is as follows: 
	
	"If we hear an R&B song, then it's after 2 am"

How do we establish that this implication is True?
- Assume that We hear an R&B song. This means it is not DJ Naoufal that's playing it. *This is based on one of our theorems, so it is True*
- If DJ Naoufal is not playing, that means he stopped for the night at 2am. *This is also based on one of our given pieces of information*
- Therefore, the time must be after 2am.

This is an example of a Direct proof: In order to prove that \\(P \to Q\\), you can assume that P is True, then build up using your reasoning and established theorems to reach that Q is True as well. 

You may be saying to yourself wait wait wait. Can you just assume P is True? isn't that cheating? In the case of proving an implication, not at all! recall what the truth table for implications looked like:

| \\( P\\) | \\( Q\\) | \\( P \to  Q\\)|
| ------------ | -------------| -----------------------------------|
| True | True | True |
| True | False | False | 
| False | True | True | 
| False | False | True | 

If P is False, then the implication is seen to be True anyways! We can and should assume that P is True, and see if you can reach that Q is True. This means that in our current scenario we are experiencing the first row of our truth table. 

How about if you want to show that an implication is false? by the same reasoning, you can Assume P, then try to establish that Q is false. 

Before proceeding to other types of proofs, let's take a moment and consolidate our learning with the following video. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/01b3KjgPhfI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## References:
For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.9](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
