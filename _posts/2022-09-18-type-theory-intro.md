---
layout: post
title:  "Intro to Type Theory"
---

"What do you work on" is a pretty normal thing people ask me upon hearing I'm a PhD student.
I wish I could completely explain the joy of working with proof assistants and the intricacies of logical relations to everyone, but when all I have is a short elevator pitch to explain the entire field, I find myself confused at where to start.
This post will be a very informal, incomplete introduction to type theory which is hopefully framed in a way that most software developers might learn something new.

Let's say you write a function that has a return type int. This means that if we run this function and it terminates, we expect the final result to be some number like 0, -1, or 1337.
Even if we know nothing about how the function is implemented, we already have some guarantees for the final result because of the type of the function.
We see that the function (closed computation) of type int runs (normalizes) until it reaches a nice looking int (canonical form).

"int" is a very boring type. Instead, we can have something like "even numbers" or "trees of depth two" or "isomorphisms from apples to oranges" or just about anything you might want to represent through code.
Each one of these interesting types contains built in guarantees for how the final form should look like, and these guarantees can be verified at compile time, before you even run your code (no test cases needed).
No code documentation is needed either, because the type of the program explains precisely what the program does.
We can fully eliminate all sources of bugs if we just have sufficiently expressive types.

If that's not enough, we can even represent mathematical conjectures as types. For example, we can represent the [Collatz conjecture](https://en.wikipedia.org/wiki/Collatz_conjecture) as a type! If we manage to write a function that has this type, we will have proven the conjecture and win a quite a lot of money. The expression of the type constitutes a proof of the conjecture.

This magical world where everything is formalized into types is still a long ways away from being fully realized.
Proof assistants such as Coq, Isabelle/HOL, Agda, and Twelf all have interesting features that help us create cool types and prove code correct, and they're gradually getting better to the point where more people can use them and develop proofs in them.
Logical relations are a powerful tool for reasoning about types and helping create these systems, and we're still unpacking everything these logical relations bring to the table.
It's a wonderful world here in Type Theory land, and if any of this post has sparked an interest in you, I encourage you to dig in more on the subject!