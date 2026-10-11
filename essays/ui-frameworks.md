---
layout: essay
type: essay
title: "UI Frameworks"
date: 2026-10-10
published: true
labels:
  - Software Engineering
  - Frontend Development
  - UI Frameworks
---

## Why Bootstrap
Following along on my journey of getting back into software engineering, getting front-end to look pretty has led to learning to use Bootstrap 5. I think it's so useful; the predefined classes take care of so many little things that would be incredibly tedious to implement using just HTML and CSS. For example - we always want things to resize well on mobile, tablet, or desktop. Bootstrap takes care of that without us having to explicitly define it. Overall, I do find it easier and faster to use compared to just CSS. It takes care of a lot of little things. One nitpick though is that I do find Boostrap harder to read within the HTML code, as opposed to if everything was styled using CSS, then it's easier to go straight to the CSS file, find the corresponding class for a given section, and make any edits there. 

## Is Bootstrap state-of-the-art? Should I always use it?
I wanted to do some research to check out whether one should always use Bootstrap, and found a bunch of different articles and reddit threads. 
As it turns out, it isn't a trivial choice that yes, we should use frameworks all the time! 
[This link](https://www.reddit.com/r/webdev/comments/nbfml9/does_anyone_develop_websites_with_just_html_css/) has a lot of people talking about how HTML, CSS, and Javascript is enough. I never considered that frameworks can also add weight to an application, so some people are memory-constrained and therefore cannot use a framework. Also, CSS itself is incredibly versatile and a lot can be done with it. Some people mentioned on that thread that frameworks can be useful in larger teams because it can standardize the code itself, which I think is a very valid point. 

For example, here's a [website](https://www.drvictoriachan.com/) that was built using only HTML and CSS. It's a really good website, and I don't see how Bootstrap could "make it better". I think it really comes down to the developer and their programming

Also, Bootstrap is way behind compared to React. React seems to be the primary choice. I did a comparison of downloads from npm over the past 5 years:

![graph of comparisons of ui frameworks downloaded using npm](/img/frameworks-downloads.png)

React and Bootstrap came out at the same time, yet React is multiple orders of magnitude more popular. So it shows that React is clearly a very popular choice.

Bottom line, my choice is currently leaning to using Bootstrap when time is a constraint and as a learning tool, but focus on React for real-world development. And more importantly, I want to get into everything that CSS has to offer. Which may be an unending task! 

## Parting Thoughts and AI
On a totally separate project, I quickly developed a labeling tool for just a couple of use to label some drone images to run through a classification model. I used Claude Code for this project, and it used just HTML and CSS for it. Of course, it's a simple app, with a singular purpose, but worth noting that with the advent of code-generating tools, some of these frameworks may start becoming redundant. The only real advantage of them that I see is that its clean and standardized code, which matters when dev teams get larger. 

