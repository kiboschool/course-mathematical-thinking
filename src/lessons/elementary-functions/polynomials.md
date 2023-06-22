# Polynomials

## Key Ideas

- Define monomials
- Define polynomials
- Define identify the degrees of monomials and polynomials.
- Define and identify the coefficients of a polynomial.

## Interest

Sometimes we are interested in modeling or describing several events that do not behave directly like a line. Such as the height of a rollercoaster, the time complexity of several sorting algorithms, the height of a ball thrown in the air, just to mention a few.

In this section we will be able to identify polynomials, the jargon around them and a few of their properties.

## Examples 
The dish in a dish antenna follows the shape of the graph of a polynomial of second degree in two variables such as 

\\(4x^2 + 4y^2\\)



## Monomials

A monomial is a term composed of the product between one or more variables and a real number. For example, if \\(x, y,\\) and \\(z\\) are variables, then the following are monomials

- \\(2x\\)

- \\(3x^2\\)

- \\(5xy\\)

- \\(\pi x^3 y z^2\\)

- \\(1\\)

The **degree** of a *monomial* is the sum of the exponents of its variables. 

- \\(2x\\) has degree 1

- \\(3x^2\\) has degree 2

- \\(5xy\\) has degree 2

- \\(\pi x^3 y z^2\\) has degree 6

- \\(1\\) has degree 0

The **number of variables** of a monomial is the number of distinct variable symbols that appear.

- \\(2x\\) is a polynomial on 1 variable.

- \\(3x^2\\) is a polynomial on 1 variable.

- \\(5xy\\) is a polynomial on 2 variables.

- \\(\pi x^3 y z^2\\) is a polynomial on 3 variables.

- \\(1\\) has no variables.

The **coefficient** of a monomial is the number that multiplies the variables of the monomial.

## Polynomials

A **polynomial** is a term composed by a sum of monomials. For example:

- \\(2x +1\\) 

- \\(3x^3 +2x\\)

- \\(x+2xy + z^2\\)

- \\(1\\)

The **degree** of a *polinomial* is the highest degree of that of its monomials. For example:

- \\(2x +1\\) has degree 1

- \\(3x^3 +2x\\) has degree 3

- \\(x+2xy + z^2\\) has degree 2

- \\(1\\) has degree 0


The **number of variables** of a polynomial is the number of distinct variable symbols that appear in all of the terms. For example:

- \\(2x +1\\) has 1 variable

- \\(3x^3 +2x\\) has 1 variable

- \\(x+2xy + z^2\\) has 3 variables

- \\(1\\) has 0 variables

The **coefficients** of a polynomial are the list of all coefficients that appear in any of the monomials that add up to the polynomial. 

- \\(2x +1\\) has 1,2 as its coefficients

- \\(x+2xy + 3z^2\\) has 1,2,3 as its coefficients

- \\(1\\) has 1 as its coefficient

When looking at a polynomial in one variable of degree \\(n\\) that has less than \\(n+1\\) monomials, we will consider 0 as a coefficient of the polynomial, as you may think of zero as the number multiplying \\(x^m\\) where \\(m\\) is smaller than n.

- We can say that \\(3x^3 +2x\\) has 3,2,and 0 as its coefficients.

Again when dealing with polynomials with one variable we might also be interested in the order of the coefficients starting by the omes corresponding to monomials with the higher degrees.

- We can list the coefficients of  \\(3x^3 +2x\\) as (3,0,3,0).

The **leading coefficient** of a polynomial in one variable is the non-zero coefficient corresponding to the monomial with the highest degree. For example:

- \\(2x +1\\) has 2 as its leading coefficient.

- \\(3x^3 +2x\\) has 3 as its leading coefficient.

## Graphs of Polynomials

In general graphs of polynomials are not easy to trace perfectly, unles you are familiar with some techniques from calculus, and further mathematical courses.

For polynomials in one variable there are some **tendencies** that you can obtain for the graph just from looking at the degree and the leading coefficient. In particular we will care mostly about the parity (whether it is odd or even) of the degree of the polynomial, and the sign (whether it is positive or negative) of the leading coefficient.

- If the degree of the polynomial is even and the leading coefficient is positive then the shape will look like an upside cup

- If the degree of the polynomial is even and the leading coefficient is negative, then the shape will look like a upside-down cup

- If the degree of the polynomial is odd and the leading coefficient is positive then the graph is going to start at the negatives, cross the x-axis and continue to grow in the positives

- If the degree of the polynomial is odd and the leading coefficient is negative then the graph is going to start at the negatives, cross the x-axis and continue to decrease in the negatives.

## Summation Notation 

When convenient we will use the Sigma-summation notation to abbreviate sums. In general if you have a list of elements 
\\(x_1, x_2, ..., x_n\\) and you want to express their sum, instead of writing the potentially ambiguous \\(x_1 + x_2 + ... + x_n\\) we would write \\(\sum_{i=1}^{n}x_n\\)

The above sum is read fully as the "indexed sum by i from \\(i\\) equal to 1 up to \\(i\\) equal to \\(n\\) of \\(x_i\\)", but we will abbreviate it as "the sum from \\(i = 1\\) to \\(n\\) of \\(x_i\\)".


### Examples

Consider the sum of the first ten natural numbers.

- \\(\sum_{i=1}^{10} i=55\\)

Or a polynomial where the coefficients correspond to odd numbers.
- \\(\sum_{i=0}^{3}(2i+1)x^i = 1+3x+5x^2+7x^3\\)

## Product Notation

When convenient we will use the Pi-product notation to abbreviate products. In general if you have a list of elements 
\\(x_1, x_2, ..., x_n\\) and you want to express their product, instead of writing the potentially ambiguous \\(x_1 \cdot x_2 \cdot ... \cdot x_n\\) we would write \\(\prod_{i=1}^{n}x_n\\)

The above product is read fully as "the indexed product by i from \\(i\\) equal to 1 up to \\(i\\) equal to \\(n\\) of \\(x_i\\)", but we will abbreviate it as "the product from \\(i = 1\\) to \\(n\\) of \\(x_i\\)".


### Examples

- Let \\(f\\) be any function \\(\prod_{n=5}^{10}f(n)=f(5)f(6)f(7)f(8)f(9)f(10)\\)

- \\(\prod_{i=1}^5 i = 120\\)

- \\(\prod_{n=1}^{4}2^i = 1024\\)

