# Introduction
This entry will go over six rules of clean code, I will summarise each rule, provide an example, and
explain how my example implements the rule. I will also show my doxygen comments from the GitHub
repository, provide some commentary on the comments, and show some examples where I get rid of the
comments to stick with the principles of clean codes.

# Rules of Clean Code

##### There are many rules of clean code, here are six examples of clean code:

## Meaningful Names

Names are everywhere within software, naming functions, variables, classes etc. Giving names a
meaningful name makes your code easier to read and makes the functions, variables etc. more searchable
within your codespace.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%231.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.1 - Example of Meaningful Names</b>
</figcaption>
</figure>

\
The highlighted names are good names for my class, private string, and the instance of Car.
They are given simple and easy-to-understand names which makes them more meaningful than if I
put a random string of letters together. The names are given the correct naming convention the
class is given PascalCase and camelCase for the private string.

## Functions

Functions should be kept small, and simple; be given a good (and meaningful) name; and should do
only one thing. The reason why you should follow this clean code principle. This will make your 
functions very clear and precise allowing any programmer to understand a function quickly.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%233.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.2 - Example of Functions</b>
</figcaption>
</figure>

\
The main function is simple and small, it prints the car model that has been set in the function
onto the console. This example shows a good use of functions.

## Comments

Comments are used to compensate for our attempt to express our code clearly. Comments should
be used on code that can be difficult to understand, however, you should consider rewriting the 
code instead to make it more inspired. It is good for your comment to explain why your code is
doing something rather than what it is doing.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%232.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.3 - Example of Comments</b>
</figcaption>
</figure>

\
There may only be one comment but if there were more comments it would be unneeded as the
code is clear and the code doesn't need to be rewritten due to its simplicity. The comment
is used to convey that the model string needs an initial value.

## Error Handling

Error handling is used to make sure the user has no problems when using your code. Use try-and-catch
statements and make sure you can't return null with if statements. Proper error handling can lead to
more robust code, it may make code harder to read but if done correctly both robustness and readability
shouldn't really be affected. There aren't any try-and-catch statements within the code that I have
provided because there isn't any user-inputted data. If you need a user to input an integer you can use
a try-and-catch statement to catch if anyone inputs any letters or symbols.

## Formatting

Formatting code is very important and can make your code more easily readable, and add consistency
to your code. If you follow the same format throughout the whole code with correct indentation and
alignment it can make reading your code so much easier, especially, if someone else is reading it.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%234.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.4 - Example of Formatting</b>
</figcaption>
</figure>

\
The highlighted part of the code shows the correct and consistent indentation, the code also shows
good alignment and is very easy to read for someone who didn't write the code.

## DRY

As mentioned in the last entry, DRY (Don't Repeat Yourself) is a principle to avoid duplicating code.
Duplicated code can lead to inconsistencies.

\
I don't really need to highlight anything with the code that I have as it is hard to show that something
hasn't been duplicated but if you read the code there isn't anything repeated or not needed.
