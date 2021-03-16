---
layout: post
title:  "Judgements Aren't True"
---
The first thing that will pop up in any logic class are formal rules and judgements. A classic example that I will discuss is the following rule.

$$\frac{A\ \textbf{true} \quad B\ \textbf{true}}{A\land B\ \textbf{true}} \land I$$

The most logical and seemingly correct interpretation one might have of this judgement rule is that it stands for “If A is true and B is true, then A and B is true.” While this mentality is sufficient to get you through a lot of material, it is inherently wrong. The statement of “if … then …” has a truth value associated with it where the statement corresponds to logical implication. We are able to ask whether this statement is true or false and devise a way of figuring that out. Judgements should not have truth values associated with them, they simply exist. We never ask whether a judgment is true or false. They simply are. We can question whether the judgement should belong in our formal system. We can question whether the judgment is sound and complete. But we can’t decide whether it is true or false as wording this question doesn’t even make sense.

To best convey what this rule is doing and how one should interpret, I’ll write a story. You are in a universe filled of weird shapes. As you walk along just sight seeing the crazy mathematically abstract world, you happen to find something that looks like “potato is fruit.” You wrinkle your your face at it and continue moving on. Suddenly, you find a shape that looks like “banana true.” You think this might be handy later so you decide to hang onto it. You take it and pack it nicely into your context backpack. As you continue walking, you find another shape that looks like “hippo true.” You have an idea! You take out your Minecraft workbench and remember this formula where you can convert from two objects that look like “_ true” and mash them together. You put the “banana true” shape into the workbench and the “hippo true” shape into the workbench and after much tiring effort, you created a new shape that looks like “banana and hippo true.” The fact that you have made this thing doesn’t delete the other shapes from existence. In fact, you can copy paste existing objects as many times as you want! You can carry anything you find in your context backpack with you to prove stuff, but it’s always best to carry exactly what you need and nothing more.

At what point in this story did we stop to think about why the objects existed? Never. They simply were. It doesn’t matter if the objects were true or not. They exist. We also never destroyed information. This is a fundamental aspect of constructive logic and it’s ties with programming languages. Things exist. We can take existing things and use them to make other things. Nothing gets used up. Of course there are also other logics that change these approaches such as linear logic only allowing you to use things once or classical logic allowing you to prove things without having necessarily having found a shape lying around but just thinking about it, but this is the most basic essence of constructive logic. We have a universe of things floating around. We can use these things to create more things and this allows us to accumulate the knowledge we have and things we have proven.

Another incorrect understanding is that rules needs to follow an order. ON PAPER, there is no difference between the first judgement and the following:

$$\frac{B\ \textbf{true} \quad A\ \textbf{true}}{A\land B\ \textbf{true}} \land I$$

However, in an implementation of this judgement rule in an algorithm, the order in which we process things might matter. Ideally, we could parallelize the left and the right sides, but usually, one of them is done first. By convention we pick the leftmost one first. This is merely a convention. The order in which we compute these and the amount of time it takes to compute them in a decision procedure doesn’t impact the validity of the rule. Of course, the faster the better.

There is also several “incorrect” representations of this rule, namely that of omitting the “true” markers

$$\frac{A\quad B}{A\land B} \land I$$

I would argue that this rule is okay enough. The “true” judgement acts as a label to what exactly the object is. What “A true” means is that the propositional term A is true. We can just as easily define a new judgement with no label so that “A” means that A is true. Notice that this would mean that the judgement “A” and the propositional term “A” look the same but aren’t the same. Adding the word true helps eliminate this confusion but isn’t necessary in practice. It just makes things nicer to look at if you remove it.