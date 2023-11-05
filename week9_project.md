# Introduction

This entry will go over the issue from last week with further implementation and
with better code quality, creating a new pull request, and going over the review
of my code from another team member.

# Issue For This Week

I have continued to work on the calendar issue from last week which was: "As an UNDAC Deputy 
Team Leader I want to create and manage a calendar of events so that I can coordinate the work 
of the operational sub-teams." I needed to create functionality with the delete and update event 
buttons to complete the issue. I also forgot last week to create a duration for an event, so I
added duration to the list and allowed the user to choose how long an event is.

# Code Snippets

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%237.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.1 - Code Snippet from Original Solution</b>
</figcaption>
</figure>

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%238.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.2 - Code Snippet From Updated Solution</b>
</figcaption>
</figure>

\
These two code snippets do the same thing but with the first snippet, there is a lot of code
that is not needed as I can just use the list to get the date. I thought when I was first doing
it there was an issue taking the value from the list and assigning it to a DateTime data type. This
is the reason why I had to use a string split and then put all the strings together then convert the
string to DateTime. This a very good example of the KISS and YAGNI principles as the updated version
is a lot simpler and removes unnecessary variables that I do not need anymore and the string splits.





# Project work 2

In week 9, you are continuing with the team project. Your portfolio entry should 
demonstrate how your software engineering practice is improving. It should include
much the same content as last week's:

* A descriptive summary of the issue that you worked on.
* Snippets from your code with commentary showing how you have used good software design 
  practice.
* A descriptive summary of the test code that you have written.
* A reflective summary of any changes that were requested during the code review along 
  with your fixes.
* A descriptive summary of any issues you found with the code that you were asked to review.
* A general reflective section that identifies, for example,
  * New things you have realised this week
  * Common problems that can arise in a team development situation
  * How your practice compares to other people's
  * etc.

Be sure to include links to the original items in the team's GitHub repository.

In the reflective sections, try to identify things that you have done better this week. 
This could include, for example,

* Better application of the principles of clean code.
* Avoiding the repetition of previous mistakes.
* More comprehensive test coverage.
* Adoption of a more systematic personal workflow.
* Improved identification of problems in other people's code.
* etc.
