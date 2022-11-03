# A case study: The monty hall problem

## Key ideas
- Apply conditional probability in a practical scenario.
- Introduce the ability to run trials in code to build up intuition of probability.

## A tricky game show:

Let's consider one of Mathematics' most famous questions: The Monty Hall problem. This problem became famous when it was shared in a journal in 1990:

> Suppose you're on a game show, and you're given the choice of three doors: Behind one door is a car; behind the others, goats. You pick a door, say No. 1, and the host, who knows what's behind the doors, opens another door, say No. 3, which has a goat. He then says to you, "Do you want to pick door No. 2?" Is it to your advantage to switch your choice?

Think about it for a moment. What move maximizes your chance of winning: Staying with your first choice? shifting? or does it even matter? Take some time to think through it, and try applying conditional probabilities to figure it out before moving forward. 

To clarify the rules of the game:
- You pick a random door out of 3 options.
- The host will then open a door with a goat behind it, and offer you an opportunity to switch. 
- The host will never open your door, or the door with the car. 
- If the host has options for what door to open, they will pick randomly.

We can define a few events for this: Let \\(C_1, C_2, C_3\\) represent the events that the car is behind door 1, 2, and 3 respectively. 

Similarly, let \\(H_1, H_2, H_3\\) represent the events that the host opens door 1, 2, and 3 respectively. 

We set a scenario where you initially pick door 1, then the host opens door 2. At this point in time, what is \\(P(C_3|H_2\\)? Are they better than your odds if you stick to your initial choice?

\\(P(C_3|H_2) = \frac{P(C_3 \cap H_2)}{P(H_2)}\\)

Let's start by computing \\(P(H_2)\\), following the assumption that you choose door 1.

- If the car is indeed behind door 1, then the host has a \\(\frac{1}{2}\\) chance to open door 2, and a \\(\frac{1}{2}\\) chance to open door 3, as they pick randomly.
- If the car is behind door 2, then the host will open door 3. There is no chance the host opens door 2 in this scenario.
- If the car is behind door 3, then the host will always open door 2.


The car has a \\(\frac{1}{3}\\) chance to be behind any door. This means that the probability the host opens door 2 is \\(\frac{1}{3} . \frac{1}{2}  + \frac{1}{3} . 0 + \frac{1}{3} . 1 = \frac{1}{2}\\)

Now what is \\(P(C_3 \cap H_2)\\)? As mentioned, if the car is behind door 3 then the host is guaranteed to open door 2, so this is the same as the odds that the car is behind door 3. \\(P(C_3 \cap H_2) = P(C_3) = \frac{1}{3}\\)

Plugging this in, we get that our conditional probability \\(P(C_3|H_2) = \frac{2}{3}\\). We have a 66.67% chance to win by switching instead of sticking to our initial guess!

This is a surprising result to many - in fact, thousands of readers sent very angry letters when the solution was published. The reasoning is sound though.

In general, conditional probabilities push us to be very accurate about the situations we are in and question some of our biases about what events are indeed connected or not.

### Running trials

As an aside - as developers, you can always easily confirm your computations and intuitions for probability in code. The [linked python script](https://replit.com/@MehdiOulmakki/Monty-Hall-Demo#main.py) defines two functions:

- The first function simulates the scenario where we always stick to our first choice. This function returns true or false if our guess turned out correct.
- The second function simulates the scenario where we always switch our choice after the host opens a door. It also returns true or false if the guess turned out correct. 

We run both those functions 500 times, and track how often each returns True. The results confirm what we computed earlier: The odds of winning when sticking to our choice are about 33%, whereas the odds of winning when changing doors are 66%. 

Two things to note before we wrap up this week:

1. As unlikely as it is, it **is** possible for our first strategy to guess correctly for all 500 attempts. Our code would then report a 100% success rate. Never run trials like this only once, or on small samples.

2. As you grow more confident with Python, you will be able to simulate increasingly more complex situations. However, it is your understanding of the underlying statistics that will allow you to write the correct code to make it happen. There is no silver bullet here! it's up to you to bring your knowledge into the code.
