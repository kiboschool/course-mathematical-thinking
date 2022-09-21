# Part 1: Intuition for encryption

Encryption fundamentally differs from hashing in that we want to ultimately be able to decrypt our initial message. Let's formalize this.
We define a function *Encrypt* with domain *D* and range *R*. for some message *m* in *D*, *Encrypt(m)* will be referred to as the cyphertext
We also must define a function *Decrypt*, the inverse of *Encrypt*, so that *Decrypt(Encrypt(m)) = m*

Let's look at a practical, historical example: 

| Letter      | a | b | c | d | e | f | g | h | i | j | k | l | m | n | o | p | q | r | s | t | u | v | w | x | y | z |
| ----------- | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| Encrypt(Letter) | s | n | v | f | r | g | h | j | o | k | l | a | z | m | p | q | w | t | d | y | i | b | e | c | u | x |

The above table is an example of a 'substituion cypher'. Using the table above, we encrypt each character in our provided message. 

1. What is the value of *Encrypt(GOODLUCK)*? what is the value of *Decrypt(ASDYASN)*?
2. More formally, how would you define the domain and range of the Encrypt and Decrypt functions?

This strategy has been used for centuries - perhaps you've used it before yourself? This is known as a symmetric key strategy: both parties communicating need to know this same table in order to encrypt and decrypt messages correctly. 

This strategy served as the basis for developing more complex encryption algorithm, which we will explore in the next sections:

## Moving from characters to numbers:
We know at this point that arbitrary data on our computers is represented in terms of bits. Everything is a number! We want to be able to encrypt the binary representation of data, as that would equally apply to text as it would audio or images. We can use a look up table as our 'key', mapping numbers to others, but there are many alternative ways to approach this situation:

3. Let's define B_4 as the set of all 4 bit binary numbers. For each of the following relations, justify if they are a valid encryption function, and if so define their corresponding decryption function.
    1. R_1(x, key), where *x* is in B_4 and *key* is a positive integer. We rotate *x* to the left n times to produce our cypher text. For example R_1(1011, 1) = 0111 and R_1(1011, 2) = 1110
    2. R_2(x, key) = x + key, where key is also an element of B_4
    3. R_3(x, key) = x XOR key, where key is also an element of B_4

## Dealing with arbitrarily large data:
I trust you've justified this on your own, but R_3 looks promising! say our plan is to XOR our binary input with the secret key k=1010. How can we handle a 12 bit message m instead of a 4 bit one? simply computing m XOR k would only encrypt the four right most bits. Let's think about this situation:

4. Given a 12 bit number, what mathematical operation would allow you to identify the 4 leftmost bits? Based on this operation, what would be your strategy to encrypt a 12 bit number using a 4 bit key? 
5. Formalize and proove that your strategy above is correct.
6. How would you change your approach if the input was an 11 bit number instead of a 12 bit one? 

## We do not trust the messenger:
With this kind of strategy, where a single piece of information - our key - is crucial, we quickly run into a major problem. Imagine that Alice wants to send a secret message to Bob, and that Cynthia is eavesdropping on their communication. 
- Alicee computes *Encrypt(message, key)* and sends it to Bob.
- Cynthia intercepts the message but can not decrypt it, as she does not have access to the key!
- Bob receives the message as well...but also can not decrypt it, as he does not have the key. 

Unfortunately, we do not have a guaranteed way to share the key over an untrusted network. The moment anyone knows the key, then our encryption serves no purposes. In the next part of this lab we will explore strategies to address this challenge, but before moving to that section: 

7. Can you think of a strategy that would allow communication over an untrusted network? this is an open ended question where we expect you to think about the problem and share ideas or questions of your own, no pressure to create a brand new algorithm!

How to submit your work:

Create a file in this repository called 1-answers.md. Write your answers to each of the prompts 1-7 in that file.

