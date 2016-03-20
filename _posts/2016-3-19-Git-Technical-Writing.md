---
layout: post
title: Using Git for Technical Writing
---

I recently finished writing [Python Crash Course](http://nostarchpress.com/pythoncrashcourse/), an introductory programming book. The first half of the book is an introduction to Python, and the second half is a set of projects that build on what was presented in the first half. Having a decent understanding of Git made my work as a writer much more manageable. I found myself using Git differently as a writer than I do as a programmer.

Using Git thoughtfully as a writer made it easier to draft the examples I used in the book, write up clear explanations of each example, develop screenshots, and post meaningful code samples online. Now that the book is in print, the use of Git in the drafting process is making it easier to support readers who ask for help working thorugh some of the longer projects. Much of this feels like common sense after the fact, but if you're just getting started with technical writing some of the suggestions that follow may be helpful.

Writing shorter pieces of example code is fairly trivial, but effective use of tools can make that work easier as well. I started an IPython notebook for each chapter in the first half of the book, and kept the entire set of notebooks under version control. When it came to longer examples and projects, Git was essential. My drafting process was simple: write code that illustrated what I was trying to show, and make a commit each time I'd want to say something about that code in the text. Then when it came to write up a section of a chapter, I'd check out the earliest version of the example and start writing about it. This was much easier than having to start from scratch and rework the entire example.

A more significant benefit of using Git came when I was dealing with screenshots. I spent two years writing Python Crash Course, and a lot changed in that time. When I compared some of the screenshots generate early on, they were inconsistent with screenshots taken more recently. I'd upgraded my OS, and upgraded some of the tools I used in the course of writing the book. Even the version of Python changed since I started writing the book. I had been careful to make a commit every time I generated a screenshot. When we were assembling the final version of the book, I skimmed through all the screenshots and regenerated each one. Regenerating a screenshot was as simple as checking out the commit for each screenshot, running the program, and saving a new version of the screenshot. This made it easy to ensure that windows had a consistent look and feel, a consistent size, and there was no difficulty in making slight changes to the code to generate better imagess.

One of the most satisfying parts of seeing a technical book in print is getting reader emails. It's fun to hear about other people who are finally understaning programming for the first time, and to learn about the projects people have been wanting to build. But what do you do when readers ask for help with the longer projects in the book? As an author, you can't walk through every reader's code individually. But it's really insightful to see some people's code and see how well people are following the line of thinking laid out in the book. The ability to complete the projects in the second half of Python Crash Course is critical to people's overall experience with the book.

When I got the first real request for help on one of the projects, I thought a bit about what to do. Alien Invasion is a Space Invaders clone, which starts in chapter 12. A reader [wrote on Twitter](https://twitter.com/Dmag33/status/689533887714844673):

> @ehmatthes Hi Eric, I am currently on Chapter 12 of your book, and cannot seem to get the bullets to appear after finishing pg 260/261.

Part of me wanted to ask for his code, because I was curious to see where his thinking diverged from what I had presented. But the professional in me wanted a more sustainable way to respond to requests for help like this. I thought about it a bit, and realized I already had a simple solution because of how I used Git in the drafting process. The chapter that introduces Alien Invasion builds the game in a series of discrete steps: make a ship, let the user control the ship, refine the ship's movement, let the ship fire bullets, refactor the code for firing bullets. I knew that readers like Chris would probably like to go back to the most recent working version of the project, but they're too new to be using Git yet. So I opened up my Alien Invasion repository, checked out the commit just before where he got off track, and posted that version online. I called this a *restore point*, and [posted a restore point](http://ehmatthes.github.io/pcc/chapter_12/README.html) for each main section in the chapter. I pointed him to these restore points, and a short while later he reported that he was [back on track](https://twitter.com/Dmag33/status/689915933138247680):

> @ehmatthes I figured out the mistake when comparing my code to yours. Thanks again.

I'm posting restore points for the next two chapters as well. Now Chris is more confident about making his way through the rest of the project, and I can easily help the next reader who gets in touch. I'll probably go through and rebuild Alien Invasion from scratch, reading along from the book, and make as many meaningful commits as I can - as many possible restore points as might help readers. I also feel good about having included an appendix covering the basics of version control even though the book is aimed at beginners.

If you're doing some technical writing spend some time thinking about how you can use version control to make your writing process more efficient, and your final product more effective for your readers.



[better description of alien invasion project]
[screenshots]
[link to restore points, in ehm.gh.io/pcc/?]