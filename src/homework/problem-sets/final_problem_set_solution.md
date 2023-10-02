# Problem Set 7

## Submission

- You may collaborate with up your peers. If you do, be sure to mention who you 
  collaborated with explicitly in your submission. For example, write "I worked
  with Ope and Mehdi on this problem set" at the top.
- Show your work. Direct answers will not be accepted.

Submit your response in Gradescope, either using the app or the website.

## Problems

1. Perform the following conversions:
    1. 27 in base 10 to base 2
    	- 27 = 13.2 + 1 
    	- 13 = 6.2 + 1 
    	-  6 = 3.2 + 0 
    	-  3 = 1.2 + 1
    	-  1 = 0.2 + 1
    	- Therefore 27 is equivalent to 11011 in binary 
    2. 111111 in base 2 to base 10
    	- this is 1+2+4+8+16+32 = 63
    3. 101 in base 10 to base 2
    	- 101 = 50.2 + 1
    	-  50 = 25.2 + 0
    	-  25 = 12.2 + 1
    	-  12 = 6.2 + 0
    	-  6 = 3.2 + 0 
    	-  3 = 1.2 + 1
    	-  1 = 0.2 + 1
    	- Therefore 101 is equivalent to 1100101 in binary
2. Compute GCD(1240, 6660)
	- Applying the euclidian algorithm we obtain:
	- 6660 = 5.1240 + 460
	- 1240 = 2.460 + 320
	- 460 = 1.320 + 140 
	- 320 = 2.140 + 40 
	- 140 = 3.40 + 20
	- 40 = 2.20 + 0
	- So GCD(1240, 6660) = 20 
3. Let *a* be a positive integer. Prove that GCD(*a*, *a*+1) = 1
	- We can apply the GCD here. Let's make our notation a bit clearer and set x = a+1, y=a
	- we get that x = y + 1
	- y = a.1 + 0
	- Therefore GCD(x, y) = 1 as it is our last non 0 remainder.

4. Prove that GCD(*a*, *a+2*) = 1 if *a* is odd, and GCD(*a*, *a+2*) = 2 if *a* is even
	- We can use a similar trick with x = a+2 and y = a. Let's apply the euclidian algorithm
	- x = y + 2
	- To move forward in the next step, we must divide y by 2.
	- if y is even then: y = 2.k + 0, so our last non zero remainder is 2
	- if y is odd, then y = 2k + 1 we must add another step.
	- k = 1.k + 0
	- Our last non zero remainder is 1
5. Show that if \\(a \equiv b (\text{mod n})\\) and if \\(b \equiv c (\text{mod n})\\), then \\(a \equiv c (\text{mod n})\\)
	- by definition, we know that \\(n | a-b\\) and \\(n | b - c\\)
	- This means that \\(n | a - b + b - c\\)
	- \\(n | a - c\\)
	- By definition then, it follows that \\(a \equiv c (\text{mod n})\\)
6. Check if the following congruences are valid and simplify them if possible
    1. \\(15x \equiv 9 \text{ (mod 25)}\\)
    	- gcd(15, 25) = 5, which does not divide 9
    	- Therefore the congruence is false
    1. \\(6x \equiv 3 \text{ (mod 9)}\\)
    	- gcd(6, 9) = 3 which divides 3, so we can proceed
    	- \\(2x \equiv 1 \text{ (mod 3)}\\) as gcd(9,3) = 3
    	- \\(2x \equiv 4 \text{ (mod 3)}\\)
    	- \\(x \equiv 2 \text{ (mod 3)}\\) as gcd(3,2) = 1
    1. \\(14x \equiv 42 \text{ (mod 50)}\\)
    	- Let's compute gcd(50, 14):
    		- 50 = 3.14 + 8
    		- 14 = 1.8 + 6
    		- 8 = 1.6 + 2
    		- 6 = 3.2 + 0 so gcd(50,14) divides 42. We can proceed
		- \\(7x \equiv 21 \text{ (mod 25)}\\) as gcd(50,2) = 2
		- \\(x \equiv 3 \text{ (mod 25)}\\) as gcd(50, 7) = 1
7. Describe the general solution for *x* and *y*, if it exists: \\(35x + 47y = 1\\)
	- We must first compute the GCD(35, 47) to see if there is a solution:
		- 47 = 1.35 + 12
		- 35 = 1.24 + 11
		- 24 = 2.11 + 2
		- 11 = 5.2 + 1
		- 2 = 2.1 + 0
	- GCD(35, 47) = 1 so there are solutions to the diophantine equation.
	- We can start by taking the congruence modulo 35: \\(47y \equiv 1 (\text{mod 35}))
	- \\(47y \equiv 1 (\text{mod 35}))
	- \\(12y \equiv 1 (\text{mod 35}))
	- \\(12y \equiv 36 (\text{mod 35}))
	- \\(y \equiv 3 (\text{mod 35})) as gcd(12, 35) = 1
	- So y = 35k + 3
	- Plugging back intot he initial equation we get:
		- 35x + 47(35k + 3) = 1
		- 35x + 47(35k) = -140
		- x + 47k = 4
		- x = 4 - 47k
	- Our general solution is therefore x = 4-47k and y = 35k+3

## References:
Problems 1-3 were drawn from:
- [chapter 6 of Precalculus, 3rd corrected edition by S&Z](https://www.stitz-zeager.com/szprecalculus07042013.pdf)
- [Chapter 2 and 4 of Number Theory, in context and interactive](https://math.gordon.edu/ntic/ntic/section-div-alg.html)
- [Chapter 5.2 of Discrete Mathematics, an open introduction, 3rd edition](https://discrete.openmathbooks.org/dmoi3/sec_addtops-numbth.html)