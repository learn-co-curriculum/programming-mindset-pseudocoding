# Pseudocoding

## Learning Goals

- Work through the process of writing pseudocode

## Introduction

Have you ever sat down to write something, such as an essay for school or an
email to a coworker, and found that you needed to write a first draft before the
final version that you turned in or sent? The first draft is a good opportunity
to get your ideas all out without worrying about making them perfect from the
beginning. You can do the same thing for code by writing a "first draft" using
high-level language that describes what is happening but saves you from writing
out the full code syntax. We call this _pseudocoding_.

Pseudocoding is useful because it helps us make sure that we concentrate on the
primary objectives of our code rather than the details or the format. This also
aligns with our Flatiron Process, which reminds us to focus on small problems
first and work our way up. So when we begin a new coding project, pseudocode is
a great first step. Here, we'll work through the process of writing it.

## Work Through the Process of Writing Pseudocode

We're going to write code to create even chunks of delicious baguette for
several people at our party. Baguettes are good to think about because they're
basically rulers that you can eat. Here's a picture.

![Brett and Jemaine are "Fou-de-fa-fa" for a baguette](https://curriculum-content.s3.amazonaws.com/pfwtfp/pfwtfp-pseudocode-demonstration/conchords_baguette.png)

_A gluten-bomb of deliciousness_

_Note: For this exercise we'll ignore that the baguette is rounded at the ends
and that there may be tiny differences between sections. Most people you'd
want to share a baguette with would ignore these as well_

Let's run through our steps to solve the problem. You can follow along with
pencil and paper or marker and whiteboard if you like! That's often how
psuedocoding is done.

### Step 1: Identify the problem

The problem is that there is a number of people with whom I'd like to share
some tasty baguette. But I also want to make sure that everyone gets an equal
amount.

### Step 2: Identify the output that would solve the problem

If I were to have a collection of pieces that were all of the same size,
everyone could share equally in the delicious baguette goodness.

So the change to the baguette in a way that solves the problem would be:

"Divide a baguette evenly among a number of people and return the pieces"

> **Talk Like a Programmer**: Most programmers and math types would say "divide
> among _n_ people."

### Step 3: Name the Procedure That Fixes the Problem

So let's call this procedure "divide baguette evenly."

The process name tells us what we should expect it to return: a collection of
evenly-sized bread pieces.

> **Decor Tip:**  Maybe put the even bread pieces a nice straw basket with a
> decorative gingham handkerchief lining it?

<img src="https://curriculum-content.s3.amazonaws.com/pfwtfp/pfwtfp-pseudocode-demonstration/bread-and-butter.jpg" alt="Sliced Bread" width="60%">

### Step 4: Identify What Inputs are Needed to Create the Output

To create the even pieces of baguette we certainly need....**a baguette**.

There's also a hint in this adjective: we keep using _even_. What is
_even_? For our purposes, _even_ means that the pieces all have the same
_length_. Given that our procedure includes the words "among _n_ people," we
need to know the **number of people**

So our inputs are:

1. Baguette
2. Number of people

<img alt="Step 1 of Pseudocode" src="https://curriculum-content.s3.amazonaws.com/pfwtfp/pfwtfp-pseudocode-demonstration/dedr.jpg" width="60%">

### Step 5: Define the Procedure’s Implementation

In our discussion of _even_ above, we found that knowing the **even length**
would be helpful to us. The **even length** is calculated by dividing the
**baguette\_length** by the number of people (or, **n**).

At this point we know the **even\_length**.

> **Tip**: This is the purpose of local variables in a procedure (function,
> method, all the same thing). They're there to make the implementation
> _clearer_ by holding information that gets reused in the procedure.

"Wait a second!" you might be thinking. We didn't define any way to _measure_
the baguette. That's _true_. This is pseudocode, not _actual_ code. When you can
easily imagine that something to get a value exists, there's no reason to not
use it _as if_ it exists when it's reasonably clear.

<img alt="Step 2 of Pseudocode" src="https://curriculum-content.s3.amazonaws.com/pfwtfp/pfwtfp-pseudocode-demonstration/psc_step_2.JPG" width="60%">

So while the baguette's length is longer than an even piece, the baguette can
be cut. The part that's cut off should go into a basket and the part that
remains should be tested for whether another piece can be cut off of it. At the
end, we'll be done and have our pieces.

<img alt="Step 3 of Pseudocode" src="https://curriculum-content.s3.amazonaws.com/pfwtfp/pfwtfp-pseudocode-demonstration/psc_step_3.JPG"> 

"Wait a second!" you might be thinking. You're using weird methods like `add()`
or `x, y = someProcedure(argument)`! Those don't exist. That's not Ruby /
Python / JavaScript!?"

Again, we're writing _pseudocode_ and there's no standard for what it looks
like. The goal here is not to write the code, but to _think about what the code
needs to do_. If one language has a very clear way of expressing that idea,
sometimes you might use it.

Here's the pseudocode in text format:

```text
Procedure DivideBaguetteEvenly(baguette, n):
  baguette_length = measure(baguette)
  even_length = baguette_length / n
  collection = []

  while baguette_length > even_length:
    piece, rest = cut_bread(baguette, even_length)
    collection.add(piece)

    baguette = rest
    baguette_length = measure(baguette)

  even_pieces = collection
  return even_pieces
```

### Next Steps

We're going to cover "Step 6: Verify the Procedure's Output" and "Step 7: Code
It" in a later lesson. While _we_ think the pseudocode is readable and
correct, what do you think? We're going to ask you about it in the next lesson.

Step through the pseudocode in your mind or on paper. Do you get the output
you expect?

## Conclusion

Pseudocoding is a valuable way to make sure you're designing your methods in
the Flatiron Process. Building small, focused, tested procedures your can rely
upon ensures that when all those procedures work together, the program _works_.

While pseudocode might, sometimes, feel like extra work, it has a powerful
ability to break programmers out of default assumptions and help them write
focused, clear code.
