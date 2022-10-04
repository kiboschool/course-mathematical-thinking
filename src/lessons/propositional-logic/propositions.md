# Propositional Logic

## Key ideas:
- Defining what a proposition is.
- Recognizing ambiguous and unambiguous statements
- Recognizing atomic componts of a sentence
- Establishing the goal of propositional logic

## Building a clear language:

This may come as a surprise to some of you, but computers are not very smart at all! Sure, they can compute a lot of numbers, and *we* have been able to build incredible software to run on them. They are incredible machines, but at a fundamental level, all they do is *follow instructions*. There is no room for interpretation, they can't inherently ask follow up questions, or interpret the instructions you provide them in different way. Computers follow instructions literally. 

As you will see in your practice of programming, this means that *translating the way you think* into something computers understand can be tricky. One of the key goals we will have in how we think about programs is **unambiguity**: There should be only one possible way to interpret what we say. 

## Propositions:

For the purposes of this course, a ***proposition*** is simply a sentence. However, we want to focus ourselves and think through sentences that are **unambiguous**. This means we should be able to evaluate all our sentences, all our propositions, as being either True or False. 

Let's look at some pairs of sentences and see if they are propositions or not:

> Tobi is kind of tall
> Tobi is 1.6 meters tall

The first sentence is subjective! some may find Tobi tall, some may not. What's considered tall in a given area may not be in another. The second sentence however is verifiable: We can measure Tobi and say if the sentence is True or False. 

> This song is bad!
> This song is in English

The second sentence is straightforward to verify: We can look at the lyrics and tell if the song is in English or not. The first sentence is not only ambiguous - you might like the song, and I might not - but the word "bad" is sometimes used to actually indicate the complete opposite in slang! The word itself is now ambiguous. 

Someimes, we will have to grapple with challenging sentences that are *impossible* to evaluate for other reasons. Let's look at these last two examples:
> This sentence is True. 
> This sentence is False.

Can the first sentence be True? well yes, it says so! Some propositions may have a unique value, *either* True or False, based on how they are crafted. They remain propositions nevertheless. 

How about the second sentence then? Do you think it is a proposition? Think aboutit for a second before seeing the answer below

<details>answer:
Well if it is a proposition, then it can be evaluated as either True or False:
- If we say that it is True, then that means the sentence is False, which is a contradiction!
- If we say that it is False, then that means the sentence is not False, so it is True! this is another contradiction!

This is inherently ambiguous: In the language we want to build, a proposition can not be both True and False at the same time, so we won't consider sentences like this.
</details>

### Notation:

We will often assign a propositon to a variable \\(P\\) instead of rewriting the whole sentence. Here \\(P\\) simply stands for **P**roposition. 

If we deal with multiple propositions, we carry on in alphabetical order, so our second proposition is \\(Q\\), then \\(R\\), etc.

### Programming 1 connection:
As you start progressing in programming 1, you will encounter boolean variables - variables that can either be True or False. You can effectively apply everything we learn about propositions in this course to boolean variables in programming!

*As an aside, we will include sections like this whenever a topic we cover is strongly related to something you are learning in programming 1!*

## Atomic sentences

Another big word! The concept behind atomic sentences is however simple. An atomic proposition is one **that can not be broken down into connected propositions**

Let's look at an example of an atomic sentence: 
> 2 + 2 = 4

Is this a proposition? Yes! it is True that 2+2 is equal to 4. 

Is there any way to "chop up" this proposition so that we find another proposition? Let's see:
- Can "2+2" evaluate to True or False? no, this sentence evaluate to 4 as we saw above. 
- How about just "4"? 4 is neither True nor False, so it's not a proposition.
- How about "2 = 4"? Well this is a proposition - a False one. Does that mean that "2+2=4" is not atomic? well let's look at what's left of the initial sentence: *"2 +"*: This is clearly not a proposition. 

You can keep trying to break the sentence above into components, but you won't find a way to break it down into multiple propositions. 

How about this sentence though?

> If the DJ is playing Jerusalema, then Zainab is not on the dancefloor

Is *"The DJ is playing Jerusalema"* a proposition? sure is, the song is either playing or not.

How about "Zainab is not on the dancefloor" ? This is also a proposition, Zainab is either on the dancefloor or not.

So we can consider two different propositions here:
- \\(P\\): The DJ is playing Jerusalema
- \\(Q\\): Zainab is not on the dancefloor

Which makes our initial sentence take the form of if \\(P\\), then  \\(Q\\)

So our intiial sentence is *not* atomic. At the end of the day, this is good! this means we can combine simple, atomic propositions to express much larger and complex ideas. In the next sections we will cover the connectors we have to make complex propositions.

### References:
For further details, you can read through the following chapters:
- [A Concise introduction to logic part 1.1](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 3.1](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)

