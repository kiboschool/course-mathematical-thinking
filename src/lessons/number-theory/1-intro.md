# Division
## Key Ideas:
- Define divisibility and alternative ways of expressing it
- Introduce the division algorithm
- Defining the concept of modulo, as well as its equivalent in Python programming

## Remainders and divisibility

Out of the four fundamental mathematical operations you have grown accustomed to, division is somewhat special. Let's focus on the set of all integers for a moment. Adding and multiplying integers together is guaranteed to give us a new integer. Substraction broadens that scope, where the result may also be a negative integer.

Division of integers on the other hand can yield wildly different results, you may still get an integer, or a defined rational fraction, such as //(frac{3}{4}//), or an irrational number such as //(frac{1}{3}//)

Understanding the mechanics of division gives us deeper insights into numbers and how they connect. We will apply these insights in problem solving, and see how some have enabled the manufacturing of electronics in the first place! as usual though, let us start with formalizing our language and with some definitions:

## Defining divisibility

Let's consider two integers *m* and *n*. if \\(\frac{n}{m}\\) is also an integer, we say that *m divides n*. We can also represent this symbolically as \\(m | n\\). All the following statements are equivalent:

- *m* divides *n*
- *n* is a multiple of *m*
- \\(m | n\\)
- \\(n = mk\\) for some integer *k*

Note that \\(m | n\\) is a proposition, which means it can be True or False. \\(4 | 20\\) holds, but \\(3 | 7\\) does not.

## The division algorithm

The definition above is nice for numbers that divide each other, but that is not always the case. How do we capture that two numbers don't quite divide each other completely? We have a handy theorem to support that:

Let *a* and *b* be two integers. We can **always** find an integer *q* such that: \\(a = qb + r\\), where \\(0 \leq r < |b|\\). In this scenario, we define *r* as the **remainder** of dividing a by b.

This may seem a bold statement, but it is easy to prove. Let *q* be the largest integer such that \\(qb \leq a\\), then we can compute \\(r = a - qb\\).

We have been using this pattern for a while when describing even and odd numbers. an even number can be represented as \\(2k\\) for some integer *k*, whereas an odd number can be represented as \\(2k + 1\\)

### Modulo

We often care a lot about the remainder of dividing two integers, so we have defined an operator for that. Following up on the definition above, if \\(a = qb + r\\), where \\(0 \leq r < |b|\\), we can say that *a modulo b = r*, which is shorter to write and say. 

In Python, you can also easily compute the modulo of two integers by using the **%** operator
```Python
	>>> 5 % 2 # will output 1, as the remainder of dividing 5 by 2 is 1
```


In the next sections we will look at several applications of these concepts: We will introduce the concept of binary numbers, and their relevance to computer science. We will then look at common denominators of integers, then finally, we will introduce a brand new type of problem based on the division algorithm in the section on congruence.

## References:

- [Chapter 2 of Number Theory, in context and interactive](https://math.gordon.edu/ntic/ntic/section-div-alg.html)
- [Chapter 5.2 of Discrete Mathematics, an open introduction, 3rd edition](https://discrete.openmathbooks.org/dmoi3/sec_addtops-numbth.html)