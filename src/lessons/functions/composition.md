# Function composition
## Key Ideas:
- Define notation for function composition
- Relate function composition to programming
- Show how established properties of functions translate to compositions

## Combining functions

As we think of functions in terms of inputs and outputs, we can imagine a system where the output of a function becomes an input for the next one. 

Let's say we have \\(f: A \to B\\) and \\(g: C \to D\\). Could we compose these two functions in a way that the output of the function *f* becomes an input to function *g*. For some \\(a \in A\\), we would want to compute g(f(a)). Can we even do that? 

It depends. We know that \\(f(a) \in B\\) so as long as \\(B \subseteq C\\), we can apply both functions, one after the other. However, if the codomain of our firt function is not a subset of the domain of the second, this will not reliably be the case. For the rest of these notes we will set things up so that codomains and domains match, but that is something to be cautious of when combining functions on your own. 

We can formally define the composition of two functions as a new function. Given \\(f: X \to Y\\) and \\(g: Y \to Z\\) we define the function:

\\(g \circ f: X \to Z, g \circ f(x) = g(f(x))\\). 

We use the \\(\circ\\) symbol to denote composition, and we read \\(g \circ f\\) as "g of f"

This translates directly to programming, where you may have seen this syntax before:

```Python
	def f(x):
		return x*x
	
	def g(x):
		return (5*x)-12
	
	# If we want to compute g of f of x, we can do so like this:
	composition = g(f(1))
	# We first figure out what the value of f(1) is, then we provide that as an input to the g function

	# If this is something you'd want to do often in your code, you could use f and g as building blocks for a new function.
	def g_of_f(x):
		return g(f(x))
```

You do have to be a bit careful when composing functions together however: We will still be concerned with domains and codomains. Look at this example:


```Python
	def f(x):
		return x - 5
	
	def g(x):
		return 2 / x
	
	test1 = g(f(10)) # test1 will equal 0.4
	test2 = g(f(5)) # This will trigger an error! f(5) returns 0, then the function g will try to divide by 0 which is not possible!
```

It is your responsibility to think about what are the possible valid inputs your function can handle, and what outputs it can generate, as you will find yourself "composing" them very often!

### Functional powers

In cases where we have a function \\(f: X \to Y\\) and \\(X \subseteq Y\\), we can compose the function *f* with itself! as a shortcut, we can write \\(f^2(x)\\) to indicate \\(f \circ f(x)\\)

more generally, we say that \\(f^n(x) = f \circ f^{n-1}(x)\\)

## Properties of compositions. 

### Associativity 

The associative property of functions states that \\((f \circ g) \circ h\\) is equivalent to \\(f \circ (g \circ h)\\). In more direct terms, if you are composing multiple functions, you may "group" them whichever way you want: Where you place those parentheses is arbitrary, and they are often not used at all.

### Injective compositions

let \\(f: X \to Y\\) and \\(g: Y \to Z\\) be injective functions. Does that mean that \\(f \circ g\\) is injective as well? 

Let's Assume that \\(g \circ f\\) is not injective. This means that there are distinct a, b in X such that \\(g \circ f(a) = g \circ f(b)\\).
- \\(f(a) \neq f(b)\\) since \\(a \neq b\\) and \\(f\\) is injective
- Therefore, since \\(g\\) is injective, it follows that \\(g(f(a)) \neq g(f(b))\\)
- This means that there can not be distinct a, b in X such that \\(g \circ f(a) = g \circ f(b)\\). We have a contradiction!
- Therefore, \\(g \circ f\\) is **injective**

### Surjective compositions

let \\(f: X \to Y\\) and \\(g: Y \to Z\\) be surjective functions. Does that mean that \\(f \circ g\\) is surjective as well? 

- Let z be an arbitrary element of \\(Z\\). \\(\exists y \in Y: g(y) = z\\) since \\(g\\) is surjective.
- Since \\(f\\) is surjective, \\(\exists x \in X: f(x) = y\\)
- Therefore, \\(\exists x \\in X: g(f(x)) = z\\)
- Thus \\(\forall z \in Z, \exists x \in X: g(f(x)) = z\\)

Therefore \\(g \circ f\\) is **surjective.**

What can you conclude about the composition of bijective functions?


## References:
[Chapter 0.4 of Discrete Mathematics: An Open Introduction, 3rd edition](http://discrete.openmathbooks.org/dmoi3/sec*intro-functions.html)
[chapter 1 of Precalculus, 3rd corrected edition by S&Z](https://www.stitz-zeager.com/szprecalculus07042013.pdf)
