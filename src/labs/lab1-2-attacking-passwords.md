# Part 2: Attacking passwords

In Part 1, you got a rough sense of the security of a password scheme by asking how likely it was that two random passwords from the same scheme would match. But... that's not actually what happens in the real world. In the real world, passwords have to be secure against an _attacker_.

In order to understand how secure different password schemes are, you'll step into the shoes of an attacker. Read the descriptions and complete the prompts below to think through password security from the point of view of breaking a password.

## Brute force

The simplest method for attack is to guess all the possible passwords. This is called "brute force" because there's nothing clever about it. It's surprisingly effective against many password schemes.

The basic idea is to try everything, very quickly. Just how fast can a computer check a password? Quite fast, it turns out! The limiting factor depends a lot on what kind of passwords are being checked, and how they are stored, but the top results are usually measured in _billions of passwords per second_. Those speeds are typically for 'offline' attacks, where the attacker can try passwords without needing to interact with the system they are attacking. For 'online' attacks, where the attacker has to interact with the service under attack, speeds are lower and techniques are more complicated (but still shockingly fast!)

## Questions

1. Let’s assume that a dedicated attacker can try 1 million passwords per second. Answer the following questions for each of the password schemes S1-S7 from Part 1.

- How quickly would every possible password be tried?
- How likely is it that the password would be broken within 1 minute of trying?
- How likely is it that the password would be broken within 1 hour of trying?
- How likely is it that the password would be broken within 1 day of trying?

(Give the probabilities as a % chance)

2. A common mechanism to mitigate brute force attacks is to limit login attempts. An attacker would have to wait a 'cooloff' period before they get to try more passwords. Answer the following questions for each of the password schemes S1-S7.

- How likely is an attacker to correctly guess the password in 3 attempts? (give your answer as a %)
- If after every 3 attempts, there was a 5 minute 'cool off' period, how quickly would the scheme be guaranteed to be broken? (give your answer as a number of seconds)
- If you were an attacker, what ideas do you have to get around such a scheme?

## Dictionary attacks

Trying every possible combination is the the most effective strategy. Attackers are smart - they can try guessing passwords that are more likely! People are predictable. They need to choose passwords that they can remember, so they end up choosing some passwords much more frequently than others.

Consider the password scheme S1 - a 4-digit numeric pincode. What do you think are the most common 4-digit pincodes?

[This post](https://www.datagenetics.com/blog/september32012/index.html) analyzed the most frequent pincodes from a database of leaked credit card information. A stunning 11% of pincodes were `1234`! As detailed in the post, lots of people seem to use their birth year as their pincode.

An attacker doesn't need to try every single password. They can try them in order of how likely people are to use that password.

This style of attack is called a _dictionary attack_. Instead of trying random passwords, it guesses from a 'dictionary' of frequently used passwords.

3. Assume an attacker is using a dictionary attack against the pin codes (scheme S1), starting with the top 20 passwords from that post. Assume that they can try 1 password / second.

Given the % of users who would choose one of those as their 4 digit pin, what is the % chance that a password will be cracked within 1 minute? 1 hour? 1 day?


### Dictionary attacks for other passwords

What would an attacker need in order to conduct a dictionary attack for alphabetic passwords? Instead of a list of commonly used pins, the attacker could use lists of _words_.

Consider S3 (8-character lowercase alphabetic passwords). Many people will use a combination of _words_ for their password.

Let’s call weak_S3 the set of passwords that are made up entirely of known words - one word, or more than one.

4. The table below shows how many common words there are of each length. Calculate the number of possible passwords in the set weak_S3.

| word length | # in dictionary |
| --- | --- |
| 8 | 80148 |
| 7 | 78035 |
| 6 | 87151 |
| 5 | 158390 |
| 4 | 149165 |
| 3 | 15939 |
| 2 | 675 |

Note the difference in size between weak_S3 and S3.

Some large fraction of people use weak passwords. Depending on what you ask, between 30% and 80% of people have bad password habits. Let's assume for our purposes that bad habits mean picking an easy to remember password: an existing word or combination of words.

5. Assume that 60% of users would choose a weak password (a password from weak_S3), and that an attacker can try 10^6 passwords per second. How likely is it that a given password would be broken within 1 minute? 1 hour? 1 day?

6. weak_S3 is S3, but made only from common words. How you would you calculate the set weak_S4, which allows for capitalized characters?

As an optional bonus task: write a python function that takes one member of weak_S3 as an argument, and returns a list of related passwords in weak_S4.

7. Consider the set of passwords S5 (8 character alphanumeric passwords). What would be - in your opinion - a weak password in this scheme?  What if we *forced* the password to have 2 numeric digits?

8. Given what you now know about dictionary attacks, what do you think about the distinction between sets S6 and S7?

As an optional bonus task: write a python function to return a set of passwords in weak_S6 from a member of weak_S7. (Assume that those sets are similar to the other weak_* sets we've defined above)

## How to submit your work

Create a file in this repository called `2-answers.md`. Write your answers to each of the prompts 1-8 in that file.