## Solving congruence problems

### Example 1:

How about solving the following congruence: Find an integer *x* such that $3x + 2 \equiv 4 (\text{mod 5})$

We can add -2 to both sides: $3x \equiv 2 (\text{mod 5})$

Can we divide by 3 right now? 3 and 5 are coprime, so we can divide without changing modulo. Our solution however would not be sound as $x \equiv \frac{2}{3} (\text{mod 5})$

So what can we do first? let's make it so that the right side is divisible by 3, without affecting the left side. 

Note that $0 \equiv 10 (\text{mod 5})$, so we can safely add 0 to the left side and 10 to the right, giving us:

$3x \equiv 12 (\text{mod 5})$

$x \equiv 4 (\text{mod 5})$ since GCD(3,5) = 1

### Example 2:
Find an integer *x* such that $20x \equiv 23 (\text{mod 14})$

Let's start by simplifying the congruence:

$6x \equiv 9 (\text{mod 14})$ since 20 modulo 14 is 6, and 23 modulo 14 is 9

$2x \equiv 3 (\text{mod 14})$ since gcd(3,14) = 1

How can we proceed from here? in prior examples, we would add 0 to the left side, and some multiple of 14 to the right side, until we can divide by 2. However, we won't be able to achieve this: 3 is odd, and 14 is even. No matter how many times we add 14 to 3 we won't find an even number we can divide. 

Sometimes, congruences just can not be solved.

There is a handy trick though to figure out whether or not we can solve a given congruence. Let's look at our congruence differently, we have that:

- $2x = 3 + 14k$ for some integer *k*
- $2x - 14k = 3$

The left hand side is clearly even, and the right hand side odd. More generally, the test we can apply here is to check if the congruence $ax \equiv b (\text{mod n})$ is to see if $GCD(a,n)|b$. If it does **not**, then the congruence has no solutions.

## Diophantine equations

Behind this complex name is a simple idea: A diophantine equation is one where we want to find integer solutions. For example, consider the equation:

$51x + 87y = 123$. If $x, y \in \mathbb R$, then we have many solutions captured by the formula $y = \frac{123 - 51x}{87}$. So for example, $x = 0, y = \frac{123}{87}$ is a solution

Are there any **integer** solutions to this though? It's a harder problem to approach, but we are now well equipped to do so:

First, we can check whether or not a solution exist by checking if $GCD(51, 87) | 123$. In this case, GCD(51,87) = 3 which divides 123, so we can proceed.

Let's simplify our equation by dividing both sides by 3:

$17x + 29y = 41$ 
If both sides of the equation are equal, then they must be **congruent** in respect to any modulo. We can use a congruence to simplify things. Let's pick modulo 17:

- $17x + 29y \equiv 41 (\text{mod 17})$ 
- $29y \equiv 41 (\text{mod 17})$ since 17x mod 17 is 0.
- $12y \equiv 7 (\text{mod 17})$
- $12y \equiv 24 (\text{mod 17})$ as we can add 0 to the left side, and 17 to the right side.
- $y \equiv 2 (\text{mod 17})$ as GCD(2,17) = 1

So we have some relevant information now! we can express y as 17k + 2. **y can no longer be any integer, and we can leverage that**

Let's plug it back in our initial equation, and try to express *x* in terms of *k*

- $17x + 29(17k + 2) = 41$ 
- $17x + 29(17k) + 58 = 41$
- $17x = -17 - 29(17k)$
- $17x = 17 (-1 - 29k)$
- $x = -29k - 1$

So we have a way to express both y and x in terms of an integer *k*! Let's try some values of *k* and convince ourselves that this works:

- For k = 0, x = -1 and y = 2. We get that 17(-1) + 29(2) = 58-17 = 41
- for k = 1, x = -30 and y = 19. We get that 17(-30) + 29(19) = 551 - 510 = 41

This process is convenient, but takes practice. I recommend tackling a few more problems. Try them on your own first before reading the solutions below. 

### Example 3:
Describe the general solution of $6x + 10y = 32$

First let's check if there is a solution. We can see that GCD(6,10) = 2 which divides 32.

Let's look for the general solution of $3x + 5y = 16$

Taking the congruence modulo 3 we get $5y \equiv 16 \text{mod 3}$

- $2y \equiv 1 (\text{mod 3})$
- $2y \equiv 4 (\text{mod 3})$
- $y \equiv 2 (\text{mod 3})$ as gcd(3,2) = 1

Therefore, y = 3k+2 for any integer $k \in \mathbb Z$

Plugging it back into the initial equation we get that:

- $3x + 5(3k + 2) = 16$
- $3x + 5(3k + 2) = 16$
- $3x + 15k = 6$
- $x = 2 - 5k$

so our general solution to the diophantine equation is that x = 2-5k and y = 3k+2 $\forall k \in \mathbb Z$

### Example 4:
Describe the general solution of $17x + 8y = 31$

First let's check if there is a solution. We can see that GCD(17,8) = 1 which divides 31.

Taking the congruence modulo 8 we get $17x \equiv 31 \text{mod 8}$

$x \equiv 7 \text{mod 8}$

Therefore, x = 8k+7 for any integer $k \in \mathbb Z$

Plugging it back into the initial equation we get that:

- $17(8k+7) + 8y = 31$
- $17(8k) + 119 +8y = 31$
- $8y = -88 -17(8k)$
- $y = -11 -17k$

so our general solution to the diophantine equation is that x = 8k+7 and y = -11 - 17k $\forall k \in \mathbb Z$

## References:

- [Chapter 5 of Number Theory, in context and interactive](https://math.gordon.edu/ntic/ntic/section-div-alg.html)
- [Chapter 5.2 of Discrete Mathematics, an open introduction, 3rd edition](https://discrete.openmathbooks.org/dmoi3/sec_addtops-numbth.html)