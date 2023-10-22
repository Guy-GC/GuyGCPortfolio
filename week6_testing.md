# Introduction

This entry will go over the testing we did on a new repository we created to compete against
another group. I will summarise the purpose of the code and show the test code, I will also
show the test code and explain the purpose, reason, and any limitations of the test.

# The New Repository

We were given a new repository to work on this week for the test battles. The repository is a
hangman app that has all the functions created but just needs the code to be implemented.
Once the code has been created then we would create the unit test for the function we made.
I worked on a function with someone else as there were only a couple of functions to work on
and the other person was having issues with the university computer and didn't have a laptop
on him so I suggested for him to work with me.

I chose to do the function within our repository called CheckLetterInWord. The purpose of
this function is to check if the word in the game Hangman contains a letter that the
user provides. So if the word is apple and the user guesses 'A' then the function would
return true, if the user guesses 'Z' the function would return false. We did two tests to ensure
the function returns the correct boolean answer (so one test for true and one test for false).

# Test Code

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/TestCapture.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.1 - Unit Test Code</b>
</figcaption>
</figure>

\
Both tests check that the function is returning the correct boolean answer, one for
true and one for false. I have used the toe for both tests and changed the letter to
guess the word. The letter A should return False due to the letter 'A' not being in the 
word 'toe' so the expected answer for the function should be False. The same has been done
for the other test but the expected answer is True due to the letter 'e' being in the word
toe.

\
We could have done a test if the word is null (there is no word) or the letter guessed is
null however these tests should have been done within another function. It may just be good
practice to do these tests, I think another person might have done the null test for the same
function that me and my partner did.

# Post Code Battles

We had an issue with our select word test which threw errors across the testing. There was a file
path within that test which needed to be changed to a relative path. All the functions call the select
word function which led to all the errors. Apart from this problem, our CheckLetterInWord testing would 
have succeeded which is great considering the little testing I have done in the past.
