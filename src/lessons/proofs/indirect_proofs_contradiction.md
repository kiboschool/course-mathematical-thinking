# Proofs by contradiction

## Key Ideas:
- Defining the strategy for proofs by contradiction
- Showcasing examples of proofs by contradiction

## The argument's strategy:
A proof by Contradiction can be very handy when trying to prove a proposition P through a series of implications. In scenarios where you find it hard to show that P is True, it may be easier to show that P *can not be False*

It sounds a bit obvious, but the two strategies are inherently different. To show that a proposition *can not be false*, our plan is going to be to *assume that it is False*, then reach a *contradiction*, something that makes no logical sense. Since we can not allow contradictions to be True, it means our assumption is incorrect, so the proposition is True!

Let's look at at an example. Let's consider the following implication and try to prove it using a direct proof:

	"for all integers n, If \\(n^2\\) is even, then n is even"

- We assume the antecedent. so let's assume n is a number such that \\(n^2\\) is even
- This means that we can express \\(n^2\\) as a multiple of 2, so \\(n^2 = 2k\\) for some integer k
- Simplifying the equation we get that \\(n=\sqrt{2k}\\)
- And now what? can we argue at this stage that *n* is even? It's quite unclear. 

Let's approach this from a different angle. We want to show that it's impossible for this proposition to be False. So we will start by assuming that it is False, then looking for a contradiction. We have an implication, so we can rephrase it as follows: 
- \\let (E(x):  x is even\\)
- Show that \\(\forall n E(n^2) \to E(n)\\)

When is an implication \\(P \to Q\\) false? well when P is True and Q is false. We will then show that if this is the case for some number, then we will reach a contradiction. 

- Assume that the implication is false
- This means that for some integer x, \\(E(x^2)\\) is true.
- It also means for that same integer x, \\(E(x)\\) is false. This means that x is an odd number. 
- \\(x = 2k + 1\\) for some integer k, by the definition of odd numbers.
- \\(x^2 = (2k + 1)^2)
- \\(x^2 = 4k^2 + 4k + 1\\)
- \\(x^2 = 2(2k^2 + 2k) + 1\\)
- \\(x^2) = 2y + 1\\) for some integer \\(y = 2k^2 + 2k\\)
- This means that \\(x^2\\) is an odd number by the definition of odd numbers.
- This contradicts our initial assumption that \\(E(x^2)\\) is true.
- Therefore our assumption that the implication is False leads to a contradiction
- Therefore, our implication can not be False!

While it was a bit more wordy, this gave us a logical path to reach our conclusion, whereas a direct proof was challenging. This way of thinking may take some time to become more intutive so the best thing we can do is to keep practicing! Take a look at the following videos for some additional examples and explanations:

<iframe width="560" height="315" src="https://www.youtube.com/embed/b-kFWP9a2tw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## References:
For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.9](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
