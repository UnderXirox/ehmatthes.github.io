---
layout: post
title: Using Git for Technical Writing
---

I recently finished writing [Python Crash Course](http://nostarchpress.com/pythoncrashcourse/), and a working understanding of git made the job much easier. Using git made it easier to draft the examples I used in the book, write up thorough explanations of each example, develop screenshots for the book, post meaningful code samples online. Now that the book is in print, the use of git in the drafting process is making it easier to support readers who ask for help working through some of the chapters.

In order to write about code, we need some code to write about. Writing shorter pieces is fairly trivial, although good use of tools can make that work more efficient as well. When it came to longer examples and projects, git was essential. My drafting process was simple: write code that illustrated what I was trying to show, and make a commit each time I'd want to say something about that code in the text. Then when it came to write up a section of a chapter, I'd check out the earliest version of the example and write about it. This was much easier than having to start from scratch and rework the entire example.

The first significant benefit of using git came when I was dealing with screenshots for the book. I spent two years writing Python Crash Course, and a lot changed in that time. When I compared some of the screenshots generate early on, they were inconsistent with screenshots taken more recently. I'd upgraded my OS, and upgraded some of the tools I use in the course of writing the book. Even the version of Python has changed since I started writing the book. I was careful to make a commit every time I generated a screenshot. When we were assembling the final version of the book, I skimmed through all the screenshots and regenerated each one. This made it easy to ensure that windows had a consistent look and feel, they had a consistent geometry, and there was no friction in making slight changes to the code to generate better examples.

One of the most satisfying parts of seeing a technical book in print is getting reader emails [quote some here, without being spammy]. But what do you do when readers ask for help with complex projects? As an author, you can't walk through every reader's code individually. But it's really insightful to see some people's code and see how well people are following the line of thinking laid out in the book. The ability to complete the projects in the second half of Python Crash Course is critical to their overall experience with the book, and with Python as a language.

When I got the first real request for help on one of the projects, I thought a bit about what to do. Reader Chris... wrote on Twitter:

I'm stuck... [quote]

Part of me wanted to ask for his code, because I was curious to see where his thinking diverged from what I presented. But the professional in me wanted a more sustainable way to respond to requests for help like this. I thought about it a bit, and realized I already had a simple solution because of how I used git in the drafting process. The chapter that introduces Alien Invasion builds the game in a series of discrete steps: make a ship, let the user control the ship, refine the ship's movement, let the ship fire bullets, refactor the code for firing bullets. I knew that Chris would probably like to go back to the most recent working version of the project, but he's too new to be using git yet. So I opened up my Alien Invasion repository, checked out the commit just before where he got off track, and posted that version online. I called this a "restore point", and posted a restore point for each main section in the chapter. I pointed him to these restore points, and a short while later he said he was back on track:

[quote]

I posted restore points for the next two chapters as well. Now Chris is more confident about making his way through the rest of the project, and I'm ready to help out the next reader who gets in touch. I'll probably go through and rebuild Alien Invasion from scratch, reading along from the book, and make as many meaningful commits as I can - as many possible restore points as might help readers. I also feel good about having included an appendix covering the basics of version control in a book aimed at beginners.

This will also make it easy to revise Python Crash Course when it's time to update it for a second edition. If you're doing some technical writing, spend some time thinking about how you can use version control to make your writing process more efficient, and your final product more effective for your readers.




[permission from chris to quote him]
[better description of alien invasion project]
[screenshots]
[conclude with a set of recommendations]