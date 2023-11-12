# Introduction

This entry will go over the issue that arose from the code review last week going over the loop function
and then creating the summaries for every function within the code.

# Issue For This Week

I decided to fix the issues from the last code review. Which said that there was duplicated code whenever
I looped through the list of events to either delete or update a particular event. I created a new class to
loop through the events and still be able to delete or update an event respectively within their classes.

# Code Snippets

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2310.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.1 - New Loop Function</b>
</figcaption>
</figure>

\
This is the new loop function I made to get rid of duplicated code. I decided to make the function bool
to allow the call of the function to be put into an if statement. If the code returns true, text will show up
displaying "Event has been saved" or "Event has been deleted". If the class returns false then the text will
say "No event on that day" or "No event to be deleted". This code has code principles such as KISS, DRY, and YAGNI,
the code has good readability due to its good coding standards with indentation, use of comments, and good use of
whitespace.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2311.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.2 Original Update Function</b>
</figcaption>
</figure>

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2312.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.3 New Update Function</b>
</figcaption>
</figure>

\
The new Update function uses the KISS principle as it only needs to make a variable for the element within
the XAML, make sure an option has been chosen for the element, and create a DateTime variable to be used for
the comparison for a date within the list of events. The code then calls the function within an if statement. If 
there is a date that matches with the one the user inputted then it will return true. This function now truly uses the
The DRY principle by not needing to have the same for loop in two different functions.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2313.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.4 Original Delete Function</b>
</figcaption>
</figure>

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2314.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.5 New Delete Function</b>
</figcaption>
</figure>

\
The new Delete function is even shorter than the Update one being reduced from 23 lines to 12 lines. The new
delete function just needs to take the values from the page. This info will go into the loop function and the
call for the loop function is within the if statement. This new code has better KISS principles and DRY principles
than the original code

# Code Review

The code review was very positive and wasn't too much due to issues from last week being fixed within this 
week's code. This is the review:

```
Code looks clean, follows DRY, YAGNI and KISS. Good job

Happy with this code, clean code principles have been applied and looks good to merge to main.
```

# Summary

I problem I ran into this week was the issues provided to us have nearly run out and a lot of issues that haven't
been assigned have been pretty much reserved as it might go hand in hand with the issue they are currently working
with. The issue I'm working with doesn't have another issue that goes with it e.g. an issue to assign specific people
with an event. If I have the chance to work on another issue that isn't a follow-up of someone else's issue then I will
do it, but if not I will create a database for the calendar and then do testing. I realised that the reason why to create
a summary rather than just general comments within the code is that you can hover over each method called and your summary
comments are shown to explain which is much more informative.
