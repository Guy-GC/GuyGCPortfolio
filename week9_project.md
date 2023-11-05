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
is a lot simpler and removes unnecessary variables that I do not need anymore and the multiple string
splits that are redundant.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%239.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.3 - Code Snippet From Update Function</b>
</figcaption>
</figure>

\
I have used the KISS principle keeping the code short and understandable, comparing the
user-inputted date with the dates stored in the list and changing the values within the
list at the correct index.

# Code Review

The code review was very positive agreeing with the good code principles. This is part of
the review:
```
The code appears to be well-written with good naming conventions.
it is clear and self-explanatory. the class itself could benefit from documentation
comments at the top to summarise the purpose of the class.
I can see you have made changes to simplify the code following the Kiss principle.
The code appears fine for merging and contains no conflicts
```

The suggestion of adding summaries to the code is very valid and can be easily
added with very minimal time taken. The next suggestion is the following:
```
lines 126- 128 seem like they could benefit from being in their own method to
minimize duplicate code this code is also used in lines 71 to 73.
```

This is something I did notice when creating the different functions but decided to
just leave it. Maybe if I created another function that cycles through the list I might
make a function that does cycle through the list to stay in DRY code.

# Summary

As mentioned last week, the team development process isn't the best. I thought that maybe instead
of every week we create code, create tests, review, and if needed fix code that has been flagged
in review. We could give ourselves a deadline for the code and unit tests, and a deadline for the reviews
as this could result in more rigorous reviewing and more suggestions to change the code in the review.
I think this week I used a better application of the principles of clean code with the string split
section I mentioned earlier. As a team, we decided to prioritise focusing on working towards completing
the issues remotely as testing has caused problems. we plan to discuss in person implementing testing
moving forward for week 9 if possible.

Link to my XAML [Code](https://github.com/wardliii/Green-Team/blob/main/Calendar.xaml) and the C#
[Code](https://github.com/wardliii/Green-Team/blob/main/Calendar.xaml.cs) in the GitHub repository.
