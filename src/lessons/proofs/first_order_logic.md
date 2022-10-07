# First order logic

## Key Ideas:
- Defining the concept of a predicate
- Introducing symbols and concepts for "For All" and "There exists"
- Translating english sentences into the newly introduced notation

## Predicates:
Predicates are a bit of a tricky concept. So far we've worked with *propositions*: statements that evaluate to True or False. 

A predicate is a bit different. Defining a predicate is like defining a "test" of sorts. For example let a predicate \\(F(x): x can code in Python\\). Simply saying \\(F(x)\\) is not a proposition. What would that mean? who is x?

On the other hand, we should be able to answer the question \\(F(Guido Van Rossum)\\) with a quick google search - as the creator of Python, one would hope he knows how to use it! This can be a handy shorthand to separate to express our thinking more accurately. 

Predicates can work on multiple variables as well. For example we can define a predicate \\(G(x, y): x has seen more episodes of Top Boy than y\\). This may be True or False based on the x and y, but still captures what we need to do to establish if the predicate.

Let's revisit one of last week's example and update it using predicates. We go back to the dancefloor with our friend Zainab. Recall we had the implication:

> If the DJ is playing Jerusalema, then Zainab is not on the dancefloor

Let's rephrase this in terms of predicates
- Let \\(P(s): The DJ is currently playing song s\\)
- Let \\(Df(x): x is on the dancefloor\\)

We can rephrase our implication now as:
> \\(P(jerusalema) \to \lnot Df(Zainab)\\)


## For All and There Exists:

Zainab clearly is over the Jerusalema fad, but her friend Kamau is proving to be the true king of the dancefloor: Regardless of what songs the DJ plays, Kamau will be on the dancefloor. 

In other words, for all songs in the DJ's arsenal, Kamau will be on the dancefloor. We have predicates to indicate that a song is playing, and that Kamau is dancing, but how do we capture this new detail, that **for all songs**, Df(Kamau) will be true? 

We could write it, as we have been, but we are once again going to enjoy some notation:

\\( \forall song: P(song) -> Df(Kamau)\\). The upside down "A" is read as "for all". This proposition reads that no matter the song, for all songs, for any song, if the Dj plays that song then Kamau will be on the dancefloor. Based on what we've learned about Kamau, this seems a True statement. 

Is \\( \forall song: P(song) -> Df(Zainab)\\)? Clearly not, as we know she is not a fan of Jerusalema. How can we capture this idea then: There is a song for which Zainab will not dance. We have yet another shortcut for this:

\\( \exists song: P(song) \to \lnot Df(Zainab)\\). The rotated "E" here reads as "there exists". This proposition is true, and reads that "there exists a song such that the dj playing the song means that Zainab will not be on the dancefloor"

The symbols above can be negated. For example we could also express Zainab's preferences as \\(\lnot(\forall song: P(song) \to Df(Zainab))\\) - in other words it is not the case that for any song, the dj playing the song implies Zainab is dancing. 

Similarly, for Kamau: \\(\lnot(\exists song: P(song) \to \lnot Df(Kamau))\\) - It is not the case that there is some song such that the dj playing that song implies Kamau is not dancing. 

## A note on domains:

Note that this the way we've been discussing this. It only makes sense to talk about songs. Our predicate P() and our quantifiers are pertaining to songs. They would not make sense for numbers, vegetables, people, or any other type of data. 

This is important to bear in mind: It is your responsibility when using quantifiers to specify what kind of information we are talking about. For the purposes of this week's content, we will be focusing on positive whole numbers. When we say for all numbers *n*, we really mean for all positive integers. 

With this we have all the tools we need to start getting into the meat of things: Proofs!

## References:
For further details and solved practice problems, you can read through the following chapters:
- [A Concise introduction to logic part 2.11 and 2.12](https://open.umn.edu/opentextbooks/textbooks/452)
- [Discrete mathematics - an open introduction part 0.2](http://discrete.openmathbooks.org/dmoi3/sec_propositional.html)
