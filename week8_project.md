# Introduction

This entry will go over the issue that I worked on in our GitHub repository, talking about the
process, creating the pull request with an assignee, and then issues that I faced reviewing
a team member's code in the repository.

# Issue For This Week

I decided to assign myself the following task: "As an UNDAC Deputy Team Leader I want to create
and manage a calendar of events so that I can coordinate the work of the operational sub-teams."
The task requires me to make a calendar that can show meetings/events if I click on a specified day; and be able to add, edit, and delete meetings/events.

# Code Snippets

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%235.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.1 - Code Snippet #1</b>
</figcaption>
</figure>

\
I believe that I have used multiple different software design principles within my
code using the KISS, DRY, useful comments, good function naming, and even the use of
whitespace. For the useful comments, I used only two comments meaning that I don't
over-comment nor make comments that just state the obvious. The first comment is used to
show further improvements later down the line which in this case is to create a spreadsheet
with all the event data so it can be saved and then accessed later on. I have kept the code
overall pretty simple, adding variables to the meetings list, and creating event handlers so
I can create classes that run when a button is pressed or when the date picker has changed values.
The use of whitespace makes the code look a lot more readable and doing so makes it look clean.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%236.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.1 - Code Snippet #2</b>
</figcaption>
</figure>

\
I have kept this function very basic just adding the user-inputted into a list when the user clicks
the 'add event' button and then displays that the event has been saved into the list. The code follows
other software design principles such as YAGNI, DRY, and KISS. You could make an argument that the change
of text for the label isn't necessarily needed but I believe that it lets the user know if the event has
properly saved.

The only thing close to a test that I have done is the if-else statement making sure there can't be no
description of the event. The user story isn't quite complete but this task I think takes more time than
a lot of other issues. I still need to make a proper unit test plus the proper implementation of the delete
and update buttons.

# Code Review

I received a very good review saying that my code is clean and understandable with no changes to be made
to my code. Due to conflicts with the .csproj file and the actual issue not fully being complete, my
code has not been merged into the main branch which means the code review I received is just general
feedback.

# Summary

two problems that could arise are there could be a lot of issues trying to merge into the main with so many
small changes being made in lots of different branches. Another problem is if both the coder and the reviewer
don't see any problems/code smells it might lead to another person having to review the code this can result in
a lot of time being wasted on reviewing rather than fixing issues. I worked on my project in a file on my computer
(not on the branch within the repository). I do this because I don't want to make changes in the mainpage file
in the repository as it will lead to conflicts and isn't the biggest priority at the moment.

Link to my XAML [code](https://github.com/wardliii/Green-Team/blob/Guy's_Branch_v2/Calendar.xaml) and the C#
[code](https://github.com/wardliii/Green-Team/blob/Guy's_Branch_v2/Calendar.xaml.cs) in the GitHub repository.
