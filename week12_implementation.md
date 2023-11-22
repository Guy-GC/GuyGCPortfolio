# Introduction

This entry will go over the addition of the NoOverlap function to make sure two or more events don't run at the same time
or overlap. I will also go over all the pull requests I commented on and what changes I suggested for those pull requests.

# Issue For This Week

I decided to continue and finish the calendar issue by adding a function that detects events that overlap with one another.
This function will be used when an event is created or updated, it doesn't need to be used for deleting an event as it 
can't overlap with another event if it doesn't exist. This is a code snippet of the NoOverlap function:

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2315.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.1 - New NoOverlap function</b>
</figcaption>
</figure>

\
I decided to use for each when looping through all the meetings as there is less to write with a for each statement than a
for statement with an integer that goes through each element within the list. This is a good example of the DRY principle
as it keeps the code a little simpler by reducing the number of characters, it makes the code look a lot easier to understand,
and it still does the same as a regular for loop. I also made sure that if a meeting ends at 4 PM and another one starts at
4 PM that this isn't considered an overlap.

I have also used other good coding principles like good commenting. I have made a summary of the function explaining what
it does, and only used comments within the function whenever some bits of code needed a little explaining.

I made the function a bool for the same reason the LoopEvent function is also a bool. I used if statements that refer to the
function as shown below:

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2316.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.2 - NoOverlap call in If Statement in LoopEvents function for Updating Events</b>
</figcaption>
</figure>

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2317.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.3 - NoOverlap call in If Statement in AddEvent function</b>
</figcaption>
</figure>
