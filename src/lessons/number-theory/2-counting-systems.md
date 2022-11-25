# Counting systems
## Key ideas:
- Deconstructing numbers in terms of their base
- Introducing a method for converting decimal numbers to binary
- Introducing the relevance of the binary counting system in computer science.

## Anatomy of a number
Let's take a big step back to our early years in school, and how we first learned about numbers. How did we build a number such as 213? We can look at it as a table:

|10^3|10^2|10^1|10^0|
|-|-|-|-|
|0|2|1|3|

In other words, \\(213 = 0.1000 + 2.100 + 1.10 + 3.1\\)

\\(213 = 0.10^3 + 2.10^2 + 1.10^1 + 3.10^0\\)

We can look at this in yet another way leveraging what we have just covered of division:

- 213 = 21.10 + **3**
- 21 = 2.10 + **1**
- 2 = 0.10 + **2**
- We have a 0 now so we stop the process.

The number of our units is the **remainder** of dividing our entire number by 10.

We can repeat this process again with the result of the division: What is the remainder of dividing 21 by 10? that our number of tens. 

We can repeat this process as many times as needed until we reach 0. As we are dividing by 10, our remainders may be any number between 0 and 9 inclusive. All numbers we've been using since our childhood have been built this way: We call them decimal numbers, or **base 10 numbers**.

### binary numbers
Now base 10 numbers are very convenient, but we can get some interesting benefits by using a different **base**. Let's look at the process of representing a number in base 2 - also known as binary - instead of base 10. 

We will follow the same approach, repeatedly dividing and considering the remainders, but dividing by 2 insteady of 10. 

Let's represent the number 7 in base 2. Since we will be dividing by 2, our possible remainders can only be 0 or 1:

- 7 = 3.2 + **1**
- 3 = 1.2 + **1**
- 1 = 0.2 + **1**
- We have a 0 now so we stop the process.

This means that in base 2, we represent 7 as 111. 

Let's try to go the other way around: How should we interpret the base 2 number 1011? As we used 2 as our building block, we can break the number apart as:

|2^3|2^2|2^1|2^0|
|-|-|-|-|
|1|0|1|1|

so shifting from binary to decimal, 1011 is equivalent to \\(1.2^3 + 0.2^2 + 1.2^1 + 1.2^0 = 11\\)

### Why bother?

Are there any reasons to use binary numbers? they seem less readable, less practical than what we've been working with. Yet, they are very much the basis for our computing systems. 

At the end of the day, it all comes down to hardware. Computers use tiny devices called transistors to store information. A transistor can either be on or off, and it takes very little electricity to switch them on or off. They are cheap, and allow us to represent numbers very easily using the binary system.

In this scenario, we call each of these transistors a "bit". They can be on or off, which represents 1 or 0 respectively. With only 8 transistors, how many possible arrangements of on and off bits can we have? That's how many numbers we could represent in binary.

Now if we can represent any arbitrary number, we can build logic on top of this to interpret these numbers as words, or sounds, or colors, or whatever other piece of information is relevant to the problems at hand. If you are curious to learn more, feel free to check out this [video](https://www.youtube.com/watch?v=Xpk67YzOn5w&ab_channel=BasicsExplained%2CH3Vtux), otherwise we will dive much deeper into how computers are built in later courses.

## References:
Problems 1-3 were drawn from [chapter 6 of Precalculus, 3rd corrected edition by S&Z](https://www.stitz-zeager.com/szprecalculus07042013.pdf)
