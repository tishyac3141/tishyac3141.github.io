---
layout: essay
type: essay
title: "Reflecting on Coding Standards (and trying to find the bright spots)"
# All dates must be YYYY-MM-DD format!
date: 2026-09-24
published: true
labels:
  - Personal Essay
  - Reflection
---
# My Honest First Impression

I'm going to be real: my first week with ESLint felt like having someone look over my shoulder and tap me on the wrist every few seconds. Unused variable. Missing semicolon. Unexpected var, use let or const instead. It's tedious. It's nitpicky. And half the time, my code ran perfectly fine before ESLint had anything to say about it.

So when the question is whether coding standards are the single best technique to improve software quality, my gut reaction was: really? Over testing? Over version control? Over just... thinking through your design?

But after sitting with it for a bit, I think the argument is more subtle than it first appears.

There are two layers to coding standards. The first is the stuff that feels arbitrary: tabs vs. spaces, where you put your braces, whether you use single or double quotes. Honestly, I don't think it matters which convention you pick. What matters is that everyone on a team picks the same one. 

The second layer is where it gets interesting. Rules like preferring const over let, or flagging unused variables, or enforcing consistent return types. Those types of rules are beyond aesthetics and more about catching a specific class of mistakes before they happen. 

# How Standards Teach You a Language

Now that I'm sitting here, thinking about what additional value am I getting from ESLint besides having really nice-looking code, I'm realizing that it has forced me to get better at using the language too. Similar to when I was implementing algorithms in the Amoebot Simulator, the codebase had strict conventions. At first they felt like overhead and just something I have to do, but then they ended up being one of the fastest ways to learn the architecture. Standards give you guardrails, and guardrails tell you something about the shape of the road. There's definitely a lot to learn from being forced to follow a certain style or set of rules.

# The ESLint Experience 

That said, irritatingly enough, a good chunk of the ESLint errors I dealt with this week were genuinely just noise. Reformatting lines that were already readable. Adding a space here, removing a space there. It felt like busywork, and I don't think that kind of enforcement, on its own, makes anyone a better engineer. But when it did keep interrupting my flow to ask "are you sure about that?", it forced a kind of mindfulness. 


I'm not sure if I totally agree that coding standards the single most impactful technique for software quality. I do think they're the technique that has the lowest barrier to entry and the highest passive return. But all of this is certianly also getting taken care of with AI tools. So... what really matters? Open question there. 
