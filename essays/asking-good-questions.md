---
layout: essay
type: essay
title: "The Importance of Writing Good Questions (yes, even though we use AI)"
date: 2025-09-10
published: true
labels:
  - Software Engineering
  - Communication
  - Stack Overflow
  - AI
---

## A Vital Skill

Now more than ever, properly structuring a question or issue one is facing is one of the most important skills for an engineer. Even when relying on LLMs - garbage in, garbage out. Without giving proper context, such a powerful tool can give really mediocre output. So, not only is conveying a question well a necessary skill when working in a team, it's now doubly as important with these agents that we interact with in plain English. A similar amount of work has to be done first.

Eric Raymond's essay, [How To Ask Questions The Smart Way](http://www.catb.org/esr/faqs/smart-questions.html), is basically a manual for that skill. His argument is simple. The open source community will help you, but it will not do the thinking for you. Show that you have tried, be precise, and respectful. Maybe the respectful part isn't necessary when interacting with an LLM, but regardless. The core concept is extremely relevant.

Stack Overflow is where this plays out publicly, every day. So I looked at two questions there, one that follows Raymond's advice and one that doesn't, to see how the community actually responds.

## The smart question

The question I picked is [How do I return the response from an asynchronous call?](https://stackoverflow.com/questions/14220321/how-do-i-return-the-response-from-an-asynchronous-call) on Stack Overflow. The asker had a JavaScript function that made an AJAX call and tried to return the result. Instead of the response, they kept getting `undefined`. They included a small, focused code snippet showing exactly the pattern that was failing, described what they expected to happen versus what actually happened, and framed the question broadly enough that it addressed the general concept rather than one specific bug.

That question checks almost every box Raymond cares about. The title is precise and searchable. The example is minimal and reproducible. There is no drama and no dumped wall of unrelated code. It reads like someone who genuinely tried to understand the problem before typing.

The community response was equally telling. The top answer, which now has thousands of upvotes, walks through why the code returns `undefined`, explains the JavaScript event loop, and covers callbacks, promises, and async/await as solutions. It became one of the most referenced answers on the entire site. 

## The not so smart question

For contrast, here is a fabricated example of the same underlying problem, asked badly. I generated it with Claude to illustrate the pattern.

> **Title:** javascript help pls
>
> **Body:** my code isnt working i need help. it says undefined but its supposed to give me the data. why is javascript so broken?? been stuck for hours pls help asap

There is no code, no error message, no version info, no description of what was tried. The title is useless for search. The tone assumes the reader owes them something. And even the framing ("why is javascript so broken") signals that the asker is more interested in venting than in learning.

This is obviously a very extreme example given by Claude, but I think its still relevant in that people, especially beginners, may still chat with their LLM in this same way. It's tempting, considering how it'll give an immediate answer, but that answer will have no depth. We still have to do the work. Or at least, we should have a separate session to understand the problem before then finding a solution.

## What actually stuck with me

The obvious lesson is that clear questions get clear answers. The less obvious one is that writing a good question is itself a debugging technique. Whenever I've done my version of smart questions (in that I asked a superior for help), I noticed how much of the work was already done by the time I'd formulated the question. 

That is probably why Raymond's essay has aged so well. It reads like it is about etiquette, but it is really about thinking clearly. And thinking clearly is the whole job, especially with so much AI.

## A note on AI

I used Claude to help me brainstorm the structure of this essay and to generate the fabricated "not smart" question. But most of the writing is purely mine.