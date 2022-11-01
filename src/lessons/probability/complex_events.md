# Probability

## Key ideas

## And

What is the probability of satifying two different events at once? Let's consider a game that involves rolling two dice at the same time. 

In this case, our sample space S has 36 different outcomes, which we can visualiz in the table below. The top row represents the value of the first dice, the leftmost column the values of the second. The pairs inside the table show all our possible outcomes:

| |1|2|3|4|5|6|
|-|-|-|-|-|-|-|
|**1**|(1,1)|(1,2)|(1,3)|(1,4)|(1,5)|(1,6)|
|**2**|(2,1)|(2,2)|(2,3)|(2,4)|(2,5)|(2,6)|
|**3**|(3,1)|(3,2)|(3,3)|(3,4)|(3,5)|(3,6)|
|**4**|(4,1)|(4,2)|(4,3)|(4,4)|(4,5)|(4,6)|
|**5**|(5,1)|(5,2)|(5,3)|(5,4)|(5,5)|(5,6)|
|**6**|(6,1)|(6,2)|(6,3)|(6,4)|(6,5)|(6,6)|

Let's consider \\(E_1\\) to represent the event that you roll at least a single 1. You can see that there are 11 scenarios that make up this event. They are shown in bold in the table below:

| |1|2|3|4|5|6|
|-|-|-|-|-|-|-|
|**1**|**(1,1)**|**(1,2)**|**(1,3)**|**(1,4)**|**(1,5)**|**(1,6)**|
|**2**|**(2,1)**|(2,2)|(2,3)|(2,4)|(2,5)|(2,6)|
|**3**|**(3,1)**|(3,2)|(3,3)|(3,4)|(3,5)|(3,6)|
|**4**|**(4,1)**|(4,2)|(4,3)|(4,4)|(4,5)|(4,6)|
|**5**|**(5,1)**|(5,2)|(5,3)|(5,4)|(5,5)|(5,6)|
|**6**|**(6,1)**|(6,2)|(6,3)|(6,4)|(6,5)|(6,6)|

Similarly, \\(E_6\\) represents the event that you roll at least a single 6. The table below highlights the 11 outcomes that make up that scenario as well.

| |1|2|3|4|5|6|
|-|-|-|-|-|-|-|
|**1**|(1,1)|(1,2)|(1,3)|(1,4)|(1,5)|**(1,6)**|
|**2**|(2,1)|(2,2)|(2,3)|(2,4)|(2,5)|**(2,6)**|
|**3**|(3,1)|(3,2)|(3,3)|(3,4)|(3,5)|**(3,6)**|
|**4**|(4,1)|(4,2)|(4,3)|(4,4)|(4,5)|**(4,6)**|
|**5**|(5,1)|(5,2)|(5,3)|(5,4)|(5,5)|**(5,6)**|
|**6**|**(6,1)**|**(6,2)**|**(6,3)**|**(6,4)**|**(6,5)**|**(6,6)**|

What is the probability that we achieve both \\(E_1\\) and \\(E_6\\)? In plain english this is the probability that we roll at least one 1 and one 6. 

This can be constructed as a brand new event \\(G\\) which consists of the outcomes that belong to **both** \\(E_1\\) and \\(E_6\\), or more directly, \\(G = (E_1 \cap E_6)\\). 

We therefore can compute \\(P(G) = P(E_1 \cap E_6) = \frac {|E_1 \cap E_6|}{|S|}\\). From the table, you can see that only (1,6) and (6, 1) belong to both evets. This gives us \\(\frac {2}{36}\\)

How about the following scenario:

Let \\(F = {(6,5), (5,6), (6,6)}\\) represent the event that the sum of your dice rolls is greater than 10. What is the probability that both \\(E_1\\) and \\(F\\) occur? as we've shown, P(E \cap F) is equal to \\(\frac {|E \cap F|}{|S|} = \frac {0}{36}\\)

### Disjoint sets:

A quick aside before we proceed: 
We consider two sets *A* and *B* to be disjoint if \\(A \cap B = \emptyset\\). In other words, two disjoint sets have no elements in common.

Broadening the definition, we say that two events are disjoint if they share no outcome in common. This means that the probability of two disjoint events occuring at the same time is always 0, as they have no intersection.

## Or

How about the probability that we satisfy either of two events? Let's start with the same example we left off with, where:
- \\(E_1\\) represents the event that you roll at least a single 1.
- \\(F\\) represent the event that the sum of your dice rolls is greater than 10.

We can create a new event \\(G\\) which consists of the outcomes that belong to **either** \\(E_1\\) or \\(F\\), or more directly, \\(G = E_1 \cup F\\). It follows then that \\(P(G) = P(E_1 \cup F) = \frac {|E_1 \cup F|}{|S|}\\)

How do we compute \\(|E_1 \cup F|\\)? luckily, we know by definition of these two events that they are disjoint, so \\(|E_1 \cup F| = |E_1| + |F|\\). 

This means that \\(P(E_1 \cup F) = \frac {14}{36}\\)

This leads us to our fourth key theorem:

### Theorem 4: 

If *A* and *B* are disjoint events with sample space *S*, then \\(P(A \cup B) = P(A) + P(B)\\)

We can prove this directly: \\(P(A \cup B) = \frac{|A \cup B|}{|S|}\\)
Given that the two sets are disjoint, we have \\(|A \cup B| = |A| + |B|\\)

Therefore, \\(P(A \cup B) = \frac{|A| + |B|}{|S|}\\)

\\(P(A \cup B) = \frac{|A|}{|S|} + \frac{|B|}{|S|}\\)

\\(P(A \cup B) = P(A) + P(B)\\)

## How about non-disjoint events?

Before talking about events, let's focus on sets: We can quickly see visually that if two sets *A* and *B* have some elements in common, we can't simply say that \\(|A \cup B| = |A| + |B|\\) The elements in common would be getting counted twice! Therefore, the correct approach here is \\(|A \cup B| = |A| + |B| - |A \cap B|\\) so that we cancel out the elements that show up in both sets. 

This same logic applies to figuring out the probabilites of non-disjoint events. Let's go back to our previous examples:
- \\(E_1\\) represents the event that you roll at least a single 1.
- \\(E_6\\) represents the event that you roll at least a single 6.

These events are not disjoint, we know we could achieve both outcomes. 

The probability that we roll at least a single 1 **or** a single 6 therefore is \\(P(E_1 \cup E_6) = \frac {|E_1 \cup E_6|}{|S|} = \frac {|E_1| + |E_6| - |E_! \cap E_6|}{36} = \frac {20}{36}\\)

By the same approach of theorem 4, we can generalize the formula for \\(P(A \cup B) = P(A) + P(B) - P(A \cap B)\\)

## Complements of events

For some sample space \\(S\\), we define the complement of an event \\(E\\) to be  all the outcomes that are not present in \\(E\\). Similarly as in sets, we represent the complement of \\(E\\) as \\(\bar E\\).

It follows then that \\((E \cup \bar E) = S\\)

Note that \\(E\\) and \\(\bar E\\) are by definition *disjoint*, as they will never share outcomes in common.

This means that \\(P(E \cup \bar E) = P(E) + P(\bar E)\\) from **Theorem 4**

We also know that \\(P(E \cup \bar E) = P(S) = 1\\) from **Theorem 2**

This enables us to come up with a new, very useful theorem:

### Theorem 5

For some sample space \\(S\\) and event \\(E\\): \\(P(E) = 1 - P(\bar E)\\)

This is very handy in scenarios where computing \\(P(\bar E)\\) is simpler than computing \\(P(E)\\). 

For example, let \\(E\\) be the event that when rolling two dice, you get two different numbers?

By definition, this is 1 minus the probability of obtaining a doubled number. Intuitively, it is simpler to see that there are exactly 6 outcomes where we have doubled numbers: (1,1), (2,2), (3,3), (4,4), (5,5), and (6,6)

Therefore, our probability \\(P(E) = 1-P(\bar E) = 1 - \frac{6}{36} = \frac {5}{6}\\)

In the next section, we will get into a different way to connect events together

## References

Chapters 1.1 and 1.2 of [Introductions to probability](https://open.umn.edu/opentextbooks/textbooks/21)
