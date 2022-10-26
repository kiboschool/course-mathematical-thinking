# Binomial Coefficients

## Key Ideas:
- Introducing visual methods for solving combinations with repetition
- Determining formulas for combinations with repetition

## Combinations with repetitions

The clasical example for combinations with repetitions is delicious: Ice cream flavours. Say an ice cream shop offers Vanilla, Chocolate, and Caramel Ice cream. You can get two scoops with your flavors of choice. Nothing stops you from going double Chocolate! This is an instance where *choosing* a given element does not prevent you from selecting it again. 

How can we compute this effectively? To build up intuition for this, I recommend you watch this [video first](https://www.youtube.com/watch?v=EJ2ZkAqh25s&ab_channel=WrathofMath)

Once you have watched it, it should be clear why selecting *k* elements from a set of *n* while allowing repetition is computed as \\(\binom{n + k - 1}{k}\\). Going back to our icecream example then, picking 2 flavors with repetition from a selection of 3 gives us \\(\binom{4}{2}\\)


## Applications

Beyond problems where it is explicit that you can make choices with repeated elements, this approach can be used creatively in problems that don't seem to be about combinations in the first place. 

Take a look at the following equation. Assuming \\(x, y, z \in \mathbb N\\), let x + y + z  = 7. How many solutions are there to this equation? 

One way to tackle this is to turn it into a combination problem: The above equation is equivalent to x + y + z = 1 + 1 + 1 + 1 + 1 + 1 + 1. Each of our three variables will contribute *some* amount of 1's to the sum total. 

Therefore, we can think of this as having to choose which 1's belong to x, which 1's belong to y, and which 1's belong to z. In this case. our set is {x, y, z}, and we will be making 7 choices from that set. 

Applying our formula, this gives us \\(\binom{7+3-1}{7} = \binom{9}{7} = 36\\) different solutions.

With this, we are now ready to transition to probability - the most direct application of all our counting strategies.