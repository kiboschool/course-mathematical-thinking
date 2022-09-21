# Part 3: RSA!

Let's jump straight ahead into the RSA algorithm:
- We begin by picking two prime numbers, *p* and *q*
- We compute ***n*** = *pq*
- We compute \phi (n) = *(p-1)(q-1)*
- We compute ***e*** to be a small odd integer which is relatively prime to \phi (n)
- Finally, we compute ***d*** to be the *multiplicative inverse of* ***e***, modulo \phi (n)
  - This last step takes some clarification. We can phrase that step as solving the equation de \equiv 1 \pmod \phi (n)

At this stage, we consider the pair (e, n) to be our public key, and (d, n) our private keys. 

1. Manually compute the private RSA keys for the following inputs:
  1. p = 17, q = 19, e = 11
  2. p = 17, q = 19, e = 5

2. Pick two values for p and q of your chosing, so long as they are primes less than 100. Create your own public and private keys. 

3. Generally, write e and d in terms of p and q. Here is a hint: what does *ed* equal to? 

We still need to understand the encryption and decryption functions necessary. To encrypt a message m, considering m is an integer, we get cypher text *c* such that:
c = P(m) = \m^e \pmod n

In order to obtain the original message *m* from the cypher text *c*, we compute: 
m = S(c) = \c^d \pmod n

First, let's see this in action:
4. Say our secret message *m* is the number 65. Compute the cypher text, then decrypt it, using the following values: n = 299, e = 5, d = 53
5. Encrypt and decrypt the same message using your own public and private key.

# Proving the correctness of RSA

The RSA algorithm's ability to encrypt and decrypt data hinges on the fact that m = P(S(m) = \(\m^e \pmod n\)^d \pmod n. 
How can we convince ourselves that this is true for all correctly defined n, e, and d? Let's work on the proof collaboratively. 

- We can simplify the statement above and say that P(S(m)) = \m^ed \pmod(n)
- From our previous findings, we know that ed = 1+k(p-1)(q-1) for some integer k
- Let's assume that m \neq 0 \pmod p, we have that:
  -  \m^ed \equiv \m^(1+k(p-1)(q-1)) \pmod p
  -        \equiv m^1 (\m^(p-1))^kq-1 \pmod p 
  -        \equiv m ((m \mod p)^(p-1))k(q-1) \pmod p
  - Using Fermat's little theorem we covered in class, we can proceed to the following form:
  - \m^ed \equiv m(1)^k(q-1) \pmod p
  - \m^ed \equiv m \pmod p
- We made an assumption above that  m \neq 0 \pmod p which enabled us to use Fermat's little theorem. If however m \equiv 0 \pmod p then we can trivially conclude that m^ed \equiv m \pmod p
- Therefore, m^ed \equiv m \pmod p for all m
- At this point we are left with this system of congruent equations:
\begin{array}
 m^ed \equiv m \pmod p \\
 m^ed \equiv m \pmod q
\end{array}

6. Using the CRT, simplify the system of equation above to establish that  m^ed \equiv m \pmod n and finish our proof.

# So what? 
We've established that RSA works, but is it really all of that more secure than the alternatives?

7. given that e and n are public, describe the process of reverse engineering q.
8. Apply this process for e = 35 and n = 221. Which step was most time consuming?

So what gives? well we used fairly small prime numbers so that we can apply the math and see it in action. In practice however, p and q are between 1024 and 2048 bit long. This makes them extremely large.
While it's fairly straightforward to compute n even with such large numbers, it is however very challenging, even for a computer, to find p and q from n in a timely fashion. 

In other words, a program trying to factor out the number n will run slower and slower as the size of p and q increases. This crucial observation is what maintains RSA as a popular algorithm to this day

# Conclusion:

Well done! you have grappled with a complex algorithm and applied the learning of many weeks in one go. 
If you are curious about the field of cybersecurity, then pursuing additional reading in number theory will prove very useful. Remember however, security is not all about numnbers and algorithms. 
It is a [mindset](https://xkcd.com/538/)

If this algorithm felt intimidating, do not worry! plenty other areas of computer science do not rely on this depth of mathematics. 
Following the reasoning above is good practice however for future algorithms we will cover. 

Most importantly, our future studies will focus a lot on not only proving that algorithms are correct, but on figuring out how fast they operate exactly. 
This is called runtime analysis, and is a crucial skill to support your growth as a developer and computer scientist. 
You intuitively might believe that factoring large numbers is hard and slow when the numbers get really big, but we will move from intuitions to proofs in that area too! 

How to submit your work:

Create a file in this repository called 3-answers.md. Write your answers to each of the prompts 1-8 in that file.
