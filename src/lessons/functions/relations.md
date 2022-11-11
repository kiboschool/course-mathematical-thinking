

## Relations

Relations are a cornerstone of mathematical thinking, and arguable of thinking in general. They refer to a mapping of elements, inputs and outputs. If you've used some kind of a table before, then you are using a relation. For example if we wanted to track how much money friends contributed to some fundraisers, we could organize this in a table as follows:

|Name| Contribution|
|-|-|
| Ife | 200|
| Tolu | 150 |
| Olivia | 150 |
| Tolu | 100 |

We could map out data about students' attendance in a school, for example:

|Name|Missed sessions|
|-|-|
| Tomi | 0 |
| Edward | 3 |
| Kwasi | 1 |
| Afia | 1 |

A relation connects elements from a specific set - for example, a series of names in the above tables - and maps them onto values from another set. 

The relation then is really a set of **pairs**, where each pair contains an input and its corresponding output. For example we can restructure them as follows: 
- Table 1: {(Ife, 200), (Tolu, 150), (Olivia, 150), (Tolu, 100)}
- Table 2: {(Tomi, 0), (Edward, 3), (Kwasi, 1), (Afia, 1)}

### Cartesian products
Let's look at table 2. The "inputs" for his relation come from a set of names, let's call it \\(A = {Tomi, Edward, Kwasi, Afia}\\).

These names are mapped onto an integer. Let's say that this course has 20 sessions overall, so the most a student can miss is 20, and the least is 0. We can define the set of outputs as \\(B = {0, 1, 2, ... 20}\\).

To describe our relations, we create a pair of elements (a, b) such that \\(a \in A, b \in B\\). It would not make sense for this relation to include a value like (Tomi, -3), or (Kwasi, Kwasi). 

We have a handy way to describe this idea of pairing elements from two sets: Given two sets A and B we define the **cartesian product** of these two sets as \\(A \times B = {(a, b) \forall a \in A, \forall b \in B}\\). In other words, this is the set of all possible pairs of values coming from both sets. 

Note here that these **pairs** are ordered. (Tomi, 0) is not the same as (0, Tomi). Therefore if A and B are two different sets, then \\(A \times B \neq B \times A\\)

What is the cardinality of \\(A \times B\\)? We should have all the tools needed to compute that: We have \\(|A|\\) options for the first element of the pair, and \\(|B|\\) options for the second. This gives us that \\(|A \times B| = |A|.|B|\\)

### Formal definition

We can now give a proper definition of what a relation is: **A relation is any subset of a Cartesian product.** 

Given two elements \\(a \in A, b \in B\\) and relation R which is a subset of \\(A \times B\\), we can write \\(a R b\\) to indicate that the pair \\((a,b) \in R\\)

## Equivalence relations

Note that the two sets of inputs and outputs do not need to be different, and we can define relations on a cartesian product \\(S \times S\\), the product of a set S with itself.

This enables us to create relations that capture an interesting property: That some values are **equivalent** to each other, i.e that we could swap them out for each other without issue. 

for example let's consider the cartesian product of the set \\(\mathbb Z\\) with itself. This gives us the set of all pairs of integers. 

Consider then the relation \\(R = \{(x, y) | x^2 = y^2\}\\). This relation is a subset of \\(\mathbb R \times \mathbb R\\) that only keeps the pairs of numbers that have the same squared value. We will show how this relation R is an **equivalence relation**

Is \\(_3R_4\\) true? no, as we can easily show that \\(3^2 \neq 4^2\\). In other words, 3 is not equivalent to 4 in this relation.

How about \\(_3R_3\\)? it is true, as \\(3^2 = 3^2\\). It is somewhat obvious, but 3 is equivalent to itself in this relation.

How about \\(_2R_{-2}\\)? That is also true, as \\(2^2 = -2^2\\). How about if we flip it? is \\(_{-2}R_2\\)? yes indeed. This tells us that 2 and -2 are equivalent, we can swap one for the other with no issues.

More generally, an equivalence relation \\(R\\) on a set \\(S\\) requires 3 properties to be true:

- **R is Reflexive**: This means that \\(\forall x \in S: xRx\\)
- **R is symmetric**: This means that \\(\forall x, y \in S: xRy \implies yRx\\)
- **R is transitive**: This means that \\(\forall x, y, z \in S: xRy \land yRz \implies xRz\\)

Let's go back to \\(R = \{(x, y) | x^2 = y^2\}\\):

- **R is reflexive**: \\(\forall x \in \mathbb Z: x^2 = x^2\\), so it follows that  \\((x, x)\in R \forall x \in \mathbb Z\\)
- **R is symmetric**: \\(\forall x, y \in \mathbb Z: x^2 = y^2 \implies y^2 = x^2\\) so if \\(xRy\\) then \\(yRx\\) follows.
- **R is transitive**: if \\(xRy\\) and \\(yRz\\), it follows that \\(x^2 = y^2 = z^2\\) so \\(xRz\\)

Do be careful that you need to explicitly cover all three properties to establish an equivalence relation. There are relation that exhibit some but not all of these properties. For example consider the relation \\(R = {(x, y) | x \leq y}\\):

- Is R reflexive? yes! we can say that a number is less than or equal to itself
- Is R transitive? yes! if \\(x \leq y, y \leq z\\), it follows that \\(x \leq z\\)
- How about the symmetric property? this is where things break! we can say that \\(_3R_5\\) for example, but not that \\(_5R_3\\)

We will revisit equivalence relations in a couple weeks as we move into number theory, but for now, let's look into a different type of relations: functions.