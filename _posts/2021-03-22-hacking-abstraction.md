---
layout: post
title:  "Post for free!"
---

I am writing about a proof strategy that has become well known as a "free proof" due to the name given in Walder's _Theorem's for free!_ paper. It is utilizing Reynold's abstraction theorem to prove two terms are related even though they might not seem related if we were to specify a type.

Let's say that we have a relation that lets us compare arbitrary objects. The relation holds only when the two objects are equivalent. I am purposely being vague in the definition here because I don't want to sit here and list every classification of objects in the universe, but let's say it's defined by common sense.

An ice cream is related to an ice cream, so is it sensible for the pair (ice cream, ice cream) to belong in the relation. However, there is more than one kind of ice cream. Does (vanilla ice cream, chocolate ice cream) fit into the relation? What about (Walmart brand ice cream, Hagen Daz brand ice cream)? This means we need to be more specific about what context we are relating things in. If we are in the context of objects, then vanilla ice cream and chocolate ice cream are both objects and therefore they are in the relation. If we are in the context of ice cream, then vanilla and chocolate are both ice cream and so they are in the relation. But there is a point where we go specific enough in our relation such that these two ice cream flavors stop being the same thing. If our relation is over ice cream flavors, then vanilla ice cream and chocolate ice cream are no longer related.

The idea of how specific a classification should be is the "type" of the objects we are comparing. Our relation is always in respect to some type such that we form $$(a,b)\in[\![\tau]\!]$$ where we are comparing objects $$a$$ and $$b$$ inside of the type $$\tau$$. Vanilla ice cream belongs in the type "ice cream flavors" and validly type checks. Vanilla ice cream also belongs in the type of "ice cream." However, vanilla ice cream doesn't belong in the type of "potatoes" so it is not valid to say that $$(\text{vanilla ice cream}, \text{vanilla ice cream})\in[\![\text{potatoes}]\!]$$. Reflexivity is not valid! Instead, we have symmetry and transitivity (ST relation), which enforces that reflexivity holds only the specific cases where we "type check."

To bring things to a more technical example, the example Bob always uses is the absolute value function and the identify function. In the context of the natural numbers, they are equivalent. But in the context of the integers, we fail at the negative integers.

One of the really cool things about types is abstraction. We can define the type $$\forall \alpha. \tau$$ which contains a type variable $$\alpha$$ and a type $$\tau$$ which contains the type variable. Now someone can come along and give us a specific type, and we substitute in this type for the alpha everywhere. Yet our term doesn't change at all! We have essentially created a library that can work in any context you give it.

Now, we will embrace the task of proving that "cat eats fish" and "dog eats steak" are related under the type "happy pet." We know that both sides validly type check. "cat eats" is a function that takes in a value of type "cat's favorite food" and produces a "happy pet." Similarly, "dog eats" takes in "dog's favorite food" and produces a "happy pet." We would be done if fish and steak were the same, but they're clearly not. Or are they?

We need a function that converts a cat into a dog. Where you find this function, I have no clue.

We know that fish is "cat's favorite food," but it is also "someone's favorite food" where we are performing a type abstraction where "someone" is our type variable. Similarly, steak is "someone's favorite food" which now brings fish and steak into a similar type. This means that if we use the function to convert "someone" from a cat into a dog, then this function would change the favorite food from a fish to a steak, making the fish and steak equivalent! Notice that the same function would satisfy comparing "cat eats" to "dog eats" because you just change the cat into a dog and they're still eating.

Here is a diagram to illustrate this process:

![](/assets/images/fish-steak.png){:class="img-responsive"}

The moral of the story, you can't compare apples to oranges, unless you abstract over fruits in which case you can.