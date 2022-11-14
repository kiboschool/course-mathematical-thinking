1. Consider the function \\(f: {1, 2, 3, 4} \to {1, 2, 3, 4}\\)
[problem 1](images/week6*p1.svg)
  1. is *f* injective? explain: *f* is not injective, as f(1) = f(4) = 3
  2. is *f* surjective? explain: *f* is not surjective, as there is no value of the domain that is mapped to 2

2. 
Assigning grades can be viewed as a relation between students and grades. As a student can only have a single grade at the end of the term, we satisfy the key property to be a function. Our domain would be the set of all possible students, and our codomain the set of all possible grades. 

3. 
Checking the reflexive property of R:
  For any fraction a/b, we have that a/b R a/b since ab = ab

Checking the symmetric property of R:
  If a/b R c/d, then ad = bc. This means that cb = da, so we have c/d R a/b

Checking the transitive property of R:
  If a/b R c/d, and c/d R e/f we have that:
  - ad = bc
  - cf = de
  Multiplying the first equation by f we have that: adf = bcf
  It follows that adf = bde as we can substitute cf for de
  Dividing both sides by d, which is non-zero we obtain:
  af = be
  Therefore a/b R e/f

As all three properties are satisfied, R is an equivalence relation.

4. Consider the following function: \\(f: \mathbb N \to \mathbb N\\) with the recurrence relation \\(\\f(n+1) = \cmd{\frac{f(n)}{2}  if  f(n)  is  even}{3f(n) + 1  if  f(n)  is  odd})
Notice that if f(0) = 1, we get that:
- f(1) = 4
- f(2) = 2
- f(3) = 1
- f(4) = 4 ...

So we have a cycle.

  1. if f(0) = 5, can f be injective? Explain why or give a specific example of two elements from the domain with the same image.
  - we have f(1) = 16, f(2) = 8, f(3) = 4, f(4) = 2, f(5) = 1, f(6) = 4, then we cycle again.
  - Therefore, multiple values map to the same image as f(3) = f(6) = 4
  1. if f(0) = 3, can f be injective? Explain why or give a specific example of two elements from the domain with the same image.
  - we have f(1) = 10, f(2) = 5, f(3) = 16, then we cycle as in the above example. In particular, we have that f(5) = f(8) = 4
  1. show that no matter the initial value, f can not be surjective:
  - assume f is surjective. That means there exists a value n in N such that f(n) = 1. Let k be the smallest value for which f(k) = 1.
  - k != 0, since if f(0) = 1 we know f is not surjective, as its effective domain is {1, 2, 4}, not N
  - Let's consider the set S = {0, 1, 2, 3, ..., k - 1}. 
  - Let I represent the image of each element of S, so I = {f(0), f(1)...f(k-1)}. This set contains a finite number of elements.
  - Therefore, consider an integer m such that m does not belong to I, and m does not belong to {1, 2, 4}. Such an element exists as I is a finite set.
  - Therefore, there exists an integer m such that there is no n that satisfies f(n) = m
  - Therefore we have a contradiction and f is not surjective.

5. Let \\(f: X \to Y\\) and \\(g: Y \to Z\\) be functions. We define \\(g \circ f: X \to Z\\) as the composition of the two functions.
  1. If \\(f\\) and \\(g\\) are both injective, must \\(g \circ f) be injective as well? Explain
  - let \\(a, b \in X\\) such that \\(a \neq b\\).
  - This means that \\(f(a) \neq f(b)\\) as \\(f\\) is injective and a and b are distinct.
  - Therefore, \\(g(f(a)) \neq g(f(b))\\) as \\(g\\) is also injective.
  - Therefore, it follows that \\(\forall a, b \in X: g \circ f(a) = g \circ f(b) \iff a = b\\)
  - This can also be proven by contradiction. Assuming \\(g \circ f\\) is not injective so there are distinct a, b in X such that \\(g \circ f(a) = g \circ f(b)\\), then finding a contradiction given that g is injective.

  1. If \\(f\\) and \\(g\\) are both surjective, must \\(g \circ f) be surjective as well? Explain
  - Let z be an arbitrary element of \\(Z\\). \\(\exists y in Y such that g(y) = z\\) since \\(g\\) is surjective.
  - Since \\(f\\) is surjective, \\(\exists x in X such that f(x) = y\\)
  - Therefore, \\(\exists x in X such that g(f(x)) = z\\)
  - Thus \\(\forall z \in Z, \exists x \in X: g(f(x)) = z\\) and \\(g \circ f\\) is surjective.
  