# Part 2: Building up to RSA

We concluded the previous checkpoint with the observation that symmetric key cryptography has a major challenge when it comes to sharing the key itself. 
In Part 3, we will dive deep into the RSA algorithm, a popular strategy to avoid this problem, but we need to get on the same page on a few definitions and theorems before tackling RSA head on.

## Asymmetric key encryption:
- One key idea behind RSA, and other similar algorithms, is that the key used to encrypt the message is *different* from the key used to decrypt it.
- RSA relies on the idea that each party in communication has two different keys: A public key *e* and a private key *d*
- Let's say that pub(m) represents applying the public key on some message m, and priv(m) represents applying the private key. We want to define *e* and *d* such that:
  - priv(pub(m)) = m
  - pub(priv(m)) = m
- If Alice wants to receive messages from Bob, she would make her public key publicly known
- Bob can then send pub_alice(m) to Alice. 
- Alice can then decrypt the cypher text by applying her private key, so priv_alice(pub_alice(m))
- If Cynthia is still eavesdropping, then she knows the public key of Alice, she can also intercept pub_alice(m), but because she does not know the private key, she should not be able to decypher the message. 

1. How do you feel about this set up? Do you have any questions in mind about e and d, the public and private keys?

RSA relies on some interesting properties of numbers to create these keys and apply them to data. We will now go over some key concepts before diving into the details of RSA.

## Relative primes:
We have covered in class what a prime number is: a number that is divisible only by itself and 1. 

We say that two numbers are considered relatively prime if their greates common divider is 1. By definition, it then follows that a prime number p is relatively prime with any other number.

2. Show that two non-prime numbers a and b can also be relatively prime. 
3. Find a relatively prime number for the following numbers:
  1. 1715
  2. 100
  3. 482671
4. Using the definition, test if the following pairs of numbers are relatively prime:
  1. 215 and 216
  2. 17 and 68
  3. 16 and 81

## Extended Euclidian algorithm.
You may have used the euclidian algorithm to solve some of the problems above. We will slightly tweak it now to get a bit more information out of it. 
Before we introduce the extended euclidian algorithm, let's first think through what other information we really want. 

5. Prove that if gcd(a, b) = d, then \exists x, y \in Z such that d = ax + by

The extended euclidian algorithm allows us to identify exactly what this x and y are. It returns 3 different values: the gcd, a factor x, and a factor y, such that gcd(a, b) = ax + by

def extended-euclidian(a, b):
  if a == 0:
      return b, 0, 1
  
  gcd, x1, y1 = extended-euclidian( b mod a, a)
  
  x = y1 - (b/a) * x1 # we use integer division here
  y = x1
  
  return gcd, x, y
  
Proving the correctness of this algorithm is left as an optional exercise. However, we should convince ourselves that it does work. 
6. For the following three pairs of integers a and b, apply the extended-euclidian algorithm to identify x, y such that gcd(a, b) = ax + by:
  1. 17 and 68
  2. 16 and 81
  3. 215 and 321
  
With this knowledge in hand, we are now ready to tackle RSA in the next section of the lab!

How to submit your work:

Create a file in this repository called 2-answers.md. Write your answers to each of the prompts 1-6 in that file.


    