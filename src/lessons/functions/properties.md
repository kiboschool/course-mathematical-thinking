# Properties of functions:

## Key Ideas:
- Introducing Injective, Surjective, and Bijective functions.
- Showcasing techniques for proving whether or not a function shows these properties.
- Introducing the concepts of inverses of a function.

## Injective functions

A function is injective if **no two elements of the input map to the same element.** 

Formally, let \\(f: A \to B\\). *f* is injective if \\(\forall x, y \in A: f(x) = f(y)  \implies x = y\\)

For example let's consider our \\(not\\) function from the last chapter:
- \\(not(True) = False\\)
- \\(not(False) = True\\)

So \\(not\\) is injective since we tested all the values from our domain, and none of them shared the same image.

Is the function \\(And\\) injective? We have that \\(And(True, False) = And(False, False) = False\\), so the function is not injective as those two inputs map to the same output.

Visually, we can also express this idea as: There are no two arrows that point to the same element

![injective function visualization](/images/injective_functions.png)


### Showing a functon is injective, or not
To show that a function is **not** injective only requires a counter example, can you find two **distinct** elements *x* and *y* from the domain such that f(x) = f(y)? if so your proof is done.

Conversely, showing that a function **is** injective requires showing that \\(\forall x, y \in Domain: x \neq y \implies f(x) \neq f(y)\\). This can be done directly in some cases, but can also be achieved using a proof by contradiction.

For example, you may assume that our function f is **not injective**, meaning that there is an x and y such that \\(f(x) = f(y)\\) and \\(x \neq y\\). 

You can then try to simplify \\(f(x) = f(y)\\) and obtain that x is indeed equal to y, contradicting your initial claim.

## Surjective functions

A function is surjective if **Every element of the codomain is the image of some element in the domain**

Formally, let \\(f: A \to B\\) be a surjective function. *f* is surjective if that \\(\forall y \in B, \exists x \in A: f(x) = y\\)

Going back to our examples, we can quickly see that both the \\(And\\) function and the \\(Not\\) function are surjective as there are outputs that produce True and outputs that produce False. 

Let's consider however the function \\(g: \mathbb R \to \mathbb R: g(x) = x^2\\). Is it surjective? consider that \\(-1 \in \mathbb R\\), our codomain. Can we solve the equation \\(x^2 = -1\\)? 

As we do not have a definition for the square root of a negative number, -1 is not the image of any element from our domain

It follows then that *g* is not surjective.

Visually, we can also express this property as: Every element in the codomain has at least one arrow pointing to it.

![surjective function visualization](/images/surjective_functions.png)

### Showing a function is surjective, or not

To show that a function is **not** surjective requires a counter example: Can you find an element *k* of the codomain such that \\(\forall x \in Domain: f(x) \neq k\\)? This requires some careful thinking for what *k* is, as well as some insight into the function itself to prove that there is no *x* in the domain that satisfies f(x) = k

Alternatively, one can also apprach this by looking at the sizes of the domain and codomain: if the codomain is larger than the domain, and each value of the domain maps to exactly one value in the codomain by definition of what a function is, then surely there are elements of the codomain with no source in the domain.

To show a function is surjective requires showing that \\(\forall y \in Codomain, \exists x \in Domain: f(x) = k\\). This is often done in a direct proof. You can define an arbitrary variable \\(y \in Codomain\\), then show that \\(\exists x \in Domain: f(x) = y\\). The crux of this proof often lies in finding an expression of x in terms of y, then establishing that it is indeed a member of the domain.


## Bijective functions

Let's think about what it means for a function to be *injective*: For a given y in the codomain, how many possible values f are there in the domain such that f(x) = y? There can't be two or more, by definition of what it means to be an injective function. There could be none at all, and there could be one. Those are the only options. In other words **at most one value in the domain maps to any value in the codomain**

Let's consider the same question for *surjective* functions. For a given y in the codomain, how many possible values f are there in the domain such that f(x) = y? Well **there has to be at least one**, otherwise we would not be a surjective function. 

So what can we say about a function that is both injective **and** surjective? The most intuitive way to think about it is that for every element of the domain there is exactly one element of the codomain, and **vice versa**.

Visually, a bijective function looks like this:

![bijective visualization](/images/bijective_function.png)

### Inverting functions

The most powerful property of bijective functions is that they can be inverted. If we have a bijective function \\(f: A \to B\\), we can define it's inverse \\(f^{-1}: B \to A, f^{-1}(y) = x \iff f(x) = y\\)

From a visual perspective, this is the function we obtain if we flip all the arrows in the previous image!

The lesson to take here is that a bijective function can be **undone**. If we have the output of a bijective function, we can reliably reconstruct its original input.

This translates well to functions in a programming context. When defining your own content, it is worthwhile to think about what properties it exhibits. If it is bijective, mapping every possible input to a unique output, then you could write a function that does the opposite of it easily. 

If it is not bijective however - say that some of its inputs map to the same output - then it would be quite difficul to **reliably** undo the action that function performs. If you were provided with that output, how would you decide what input it connects to? 

Functions as they are used in programming draw a lot of inspiration from mathematical functions and their properties. Let's explore one final one in the next section.


## References:
[Chapter 0.4 of Discrete Mathematics: An Open Introduction, 3rd edition](http://discrete.openmathbooks.org/dmoi3/sec*intro-functions.html)
[chapter 1 of Precalculus, 3rd corrected edition by S&Z](https://www.stitz-zeager.com/szprecalculus07042013.pdf)
