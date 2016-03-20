---
layout: post
title: Using Git for Technical Writing
---

I recently finished writing [Python Crash Course](http://nostarchpress.com/pythoncrashcourse/), an introductory programming book. The first half of the book is an introduction to Python, and the second half is a set of projects that build on what was presented in the first half. I found myself using Git differently as a writer than I do as a programmer. Having a decent understanding of Git made the process of writing a full-length technical book much more manageable. 

Using Git as a writer made it easier to draft the examples I used in the book, write up clear explanations of each example, compile screenshots, and post meaningful code samples online. Now that the book is in print, the use of Git in the drafting process is making it easier to support readers who ask for help working through some of the longer projects. Much of this feels like common sense after the fact, but if you're just getting started with technical writing some of the suggestions that follow may be helpful.

### Git in the drafting process

Writing shorter pieces of example code is fairly trivial, but effective use of tools can make that work easier as well. I created an [IPython notebook](http://jupyter.org/) for each chapter in the first half of the book, and kept the entire set of notebooks under version control. When it came to longer examples and projects, Git was essential. My drafting process was simple: write code that illustrated what I was trying to show, and make a commit each time I'd want to say something about that code in the text. Then when I was ready to write a new chapter, I'd check out the earliest version of the example and start writing about it. This was much easier than having to start from scratch and rework the entire example.

### Using Git to manage screenshots

Using Git as a writer was also helpful in dealing with screenshots. I spent two years writing Python Crash Course, and a lot changed in that time. When I looked back at some of the screenshots generated early on, they were inconsistent with screenshots taken more recently. I'd upgraded my OS, and upgraded some of the tools I used in the course of writing the book; even the version of Python changed since I started writing. I had been careful to make a commit every time I generated a screenshot. When we were assembling the final version of the book, I went back through all the screenshots and regenerated each one. Regenerating a screenshot was as simple as checking out the commit for that screenshot, running the program, and saving a new image. This made it easy to ensure that windows had a consistent look and feel, a consistent size, and I was free to make slight changes to the code in order to generate better images.

### Using Git to support readers

One of the most satisfying parts of seeing a technical book in print is getting reader emails. It's fun to hear from readers who are finally understanding programming for the first time, and to learn about the projects people have been wanting to build. But what do you do when readers ask for help with the longer projects in a book? As an author you can't walk through every reader's code individually. However it's really helpful to see some people's code and see how well readers are following the line of thinking laid out in the book.

When I got the first real request for help on one of the projects, I thought a bit about what to do. Alien Invasion is a Space Invaders clone, which starts in chapter 12. A reader named Chris [wrote on Twitter](https://twitter.com/Dmag33/status/689533887714844673):

> @ehmatthes Hi Eric, I am currently on Chapter 12 of your book, and cannot seem to get the bullets to appear after finishing pg 260/261.

Part of me wanted to ask for his code, because I was curious to see where his thinking diverged from what I had presented. But also wanted wanted a more sustainable way to respond to requests for help like this. I realized I already had a simple solution because of how I used Git in the drafting process. The chapter that introduces Alien Invasion builds the game in a series of discrete steps: make a ship, let the user control the ship, refine the ship's movement, let the ship fire bullets, and then refactor the code for firing bullets. I knew that readers like Chris would probably like to go back to the most recent working version of the project, but they're too new to be using Git in their own work yet. So I opened up my Alien Invasion repository, checked out the commit just before where he got off track, and posted that version online. I called this a *restore point*, and [posted a restore point](http://ehmatthes.github.io/pcc/chapter_12/README.html) for each main section in the chapter. I pointed him to these restore points, and a short while later he reported that he was [back on track](https://twitter.com/Dmag33/status/689915933138247680):

> @ehmatthes I figured out the mistake when comparing my code to yours. Thanks again.

I'm posting restore points for the next two chapters as well. Now Chris is more confident about making his way through the rest of the project, and I can easily help the next reader who gets in touch. I'll probably go through and rebuild Alien Invasion from scratch, reading along from the book and making as many meaningful restore points as possible. It also makes me feel good to have included an appendix covering the basics of version control even though the book is aimed at beginners.

If you're doing some technical writing, spend some time thinking about how you can use version control to make your writing process more efficient. Your final product will be more useful for your readers, and your work in supporting them will be easier as well.

- - -

[Python Crash Course](http://nostarchpress.com/pythoncrashcourse/) is available through [No Starch Press](http://nostarchpress.com/pythoncrashcourse) and [Amazon](http://www.amazon.com/Python-Crash-Course-Project-Based-Introduction/dp/1593276036/). If you're new to Python, check out the set of [Beginner's Python Cheat Sheets](http://ehmatthes.github.io/pcc/cheatsheets/README.html) that accompany the book.

[![Python Crash Course cover]({{ site.baseurl }}/images/cover.jpg)](http://nostarchpress.com/pythoncrashcourse)