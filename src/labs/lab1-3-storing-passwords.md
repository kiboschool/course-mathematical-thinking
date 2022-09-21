# Part 3: Storing passwords

Even more effective in practice than brute force attacks and dictionary attacks are _credential stuffing attacks_.

Here's how it works from the attacker's perspective. Say some company has a data breach, which comprimises the passwords and emails of thousands of users. That company might fix their problem - get everyone to change their password, or something. But... people reuse passwords across sites. An attacker could buy that list of usernames and passwords, and try using them on other platforms.

The site [HaveIBeenPwned](https://haveibeenpwned.com/PwnedWebsites) maintains a database of leaks, so that you can find out if a given username / password pair has been leaked. There are a _ton_ of sites that have leaked passwords.

Credential stuffing attacks aren't really that interesting as users or as attackers. For users, there's no great answer. You should use different passwords on different sites, and you should try not to use sites that don't have strong security... but it's hard to tell which those are. As an attacker, credential stuffing is _effective_, but there's no cleverness to it - you just try the usernames and passwords in the list.

Preventing credential stuffing and mitigating data breaches is _really_ interesting from the perspective of application developers. If we're trying to build secure systems, what are the lessons to learn? How can we avoid being added to the list of sites with data breaches?

## Hashing passwords

One key problem in many of these breaches was that passwords were stored in plain text. In the database for these applications, there was a username column and password column. When a user logged in, the app would check that the password matched the username.

Attackers were able, through various means, to get access to that database. When they did, all the passwords were there to be stolen, just like that. Those passwords could be reused in credential stuffing attacks, as described above.

What if the application never stored the passwords in plain text? If there was some way to avoid keeping a _password_ column in the database, then even if the attacker got access, they wouldn't be able to get the passwords.

The app still needs to be able to _verify_ the password when someone logs in. We need a way to verify passwords, without storing them. It turns out, there is a way to do this, based on a clever mathematical trick called a _hash function_.

(We can also get some protection using _encryption functions_, which you will explore more in the next project)

A hash function is useful because it's _very hard to undo_. There's no easy-to-compute inverse function. Instead of storing the password in the database, we can store the hash of the password (the output of the hash function). Because the hash function is non-invertible, even if an attacker got ahold of the database, they wouldn't be able to see the passwords - just some random-looking noise.

## A hash function

Run the code in hashing_demo.py, and provide it with a test password. What do you notice about the size of the hashed value? Try it again, several times, with the same password. What do you notice about the output? Finally, make a small change to your password - swap a letter, or change its casing, or add just one number. What do you notice about the output?

The algorithm in `hashing_demo.py` is called _md5_ and it is a very popular example of a hash function.

Here's the formal definition of a hash function:

> A hash function takes input of an arbitrary size, and generates output of a fixed size.

That... doesn't say much about non-invertibility, or other things that make a function a _good_ hash function.

So, what else makes a function _good_ for hashing passwords?

## What makes a good hash function?

Domain needs to be the set of possible passwords, range should be a fixed-length output.

- **Deterministic**: output should be the same for the same input
- **Uniform**: should generate each output with the same probability
- **Avalanche Effect**: Small changes to the password should yield drastically different outputs

## Task: Assessing hash functions

Let’s try to assess some hashing functions now.

Consider the following hashing algorithm for numeric pincodes in S2:

```txt
- Sum the last 4 digits
- Add the result to the number represented by the first 4 digits
- Output the result
```

1. Prove that for any number _N_ in S2, applying the instructions above can not yield a result that is 6 digit large.

2. Consider the relation H1, with domain S2, and range N(5) (five digit numbers)

- Is H1 a function? Why or why not?
- Come up with two numbers, x and y, such that H1(x) = H1(y)
- Does H1 fit the formal definition of a hash function?
- Is H1 a _good_ hash function? Why or why not?

3. Consider a hashing function H2. It’s domain is S7, and it’s range is N(6) (six digit numbers). What is the cardinality of the range of H2?

4. Consider the following statement

> *“If a function’s range is smaller than its domain, then that function cannot be injective”*

- Prove or refute this statement.
- Based on your proof, what is the implication for H2?
- Could there be a function D1 that is the inverse of H2?
- What is the implication for using H2 to hide passwords? What might happen if hashed passwords leaked?

## Conclusion

Hash functions are prone to _collisions_. Collisions happen when two different inputs lead to the same hash output. This means that while we are safer by storing **a hash of our passwords** instead of our plain passwords, we now run a new risk: there could be some other password with the same hash value as our password! A malicious user could gain access to an account using a that different password.

Let's add another property to the list for what makes a good cryptographic hash function:

- **Collision resistant**: difficult to find two different messages that have the same hash

Security is an arms race. When researchers invent new techniques to keep things secure, attackers discover new flaws, which in turn motivate new techniques. All of the techniques, for both attackers and defenders, are heavily reliant on mathematics and design: probability, sets, functions, and, as you'll see when you learn more about encryption, number systems and number theory.

On a lighter note, take a look at this [comic](https://imgs.xkcd.com/comics/password_strength.png).

5. (Optional) What do you think of the statement the comic makes? Is the password scheme from the comic (four 3-to-8 letter words) safe? What would you recommend to your friends and family, in terms of password management?