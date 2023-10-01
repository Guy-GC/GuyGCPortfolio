# Introduction

This entry will go over a code snippet, explain the problems with the snippet going through the
different code smells that if or if it doesn't follow the code smell, and providing a code
snippet that has been fixed.

# Code Review

We were given by our lecturers multiple code snippets followed up by a couple of questions. 
The code snippet I chose is:
```C#
class Car
{
  public string model;

  // Class constructor
  public Car()
  {
    model = "Mustang"; // Set the initial value for model
  }

  static void Main(string[] args)
  {
    Car Ford = new Car();
    Console.WriteLine(Ford.model);
  }
}
```
The given code can compile and run but outputs Mustang when it should output ford
based on what the code is showing (Console.WriteLine(Ford.model);). One change that
I made was getting rid of the public Car as you can write at the top that the public
string model is equal to Mustang and it will still make the initial value for model, you
just need to get and set the model. I also did a little syntax change and also made set the
model to Ford. Instead of Car Ford = new Car(); I made it Car Ford = new() { Model = "Ford" };
This is my version of the code snippet.
```C#
class Car
{
    private string model = "Mustang"; // Set the initial value for model
    public string Model { get { return model; } set { model = value; } }
    static void Main(string[] args)
    {
        Car Ford = new() { Model = "Ford" };
        Console.WriteLine(Ford.Model);
    }
}
```







# Code review

This section documents your practical work from week 4 in which you attempt a series of 
code review challenges. For your portfolio, do the following:

1. Choose the code review challenge which best demonstrates your skills.
2. Copy the code into your portfolio using a Markdown
   [fenced code block](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks).
3. Provide some descriptive commentary that identifies the problems.
4. Show your improved version of the code in a second code block.
5. Explain in one or more paragraphs why your solution is a good one.

**DO**

* Use grammatically correct sentences and paragraphs for your commentary.
* Make clear reference to the code in your commentary. GitHub Markdown does not support
  line numbers and so you need to make sure that the reader knows which line you are
  referring to from your description.
* Refer to recognised principles or rules when describing your solution. "I thought it
  would be better that way" is not sufficient: you need to have specific reasons.

**DON'T**

* Include multiple examples. Make the decision about which example shows your best
  work and use that one.
