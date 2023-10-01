# Introduction

This entry will go over a code snippet, explain the problems with the snippet going through the
different code smells that if or if it doesn't follow the code smell, and providing a code
snippet that has been fixed.

# Code Review

We were given by our lecturers multiple code snippets followed by a couple of questions. 
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
The given code can compile and run but outputs Mustang when it should output Ford
based on what the code is showing (Console.WriteLine(Ford.model);). One change that
I made was getting rid of the public Car as you can see at the top the public
string model is equal to the Mustang and it will still make the initial value for the model, you
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
I believe that the first code snippet violates the KISS, YAGNI, and DRY general principles.
The KISS (Keep it Simple, Stupid) principle has to do with the readability of the code. The reason 
why programmers should apply this principle is that the code becomes easier to understand and
it can be easier to locate and fix bugs when the code is simpler. I believe the code has been made simpler
due to the removal of the unnecessary class constructor and the Car Ford = new() { Model = "Ford" }; the line
has been made easier to understand and functions correctly.


This principle also kind of ties up with the other principle YAGNI (You Ain't Gonna Need It) when something
has been partially implemented or just dead code you should remove it. I think that again, the class constructor 
should be removed.

Another principle that has been violated is the DRY principle. The DRY (Don't Repeat Yourself)
I believe that the string Model has been repeated as the string has been declared to then initialise
a value in a separate line when it can be done in one line and the two lines are very similar.

There are two other principles that haven't been mentioned as the code snippet doesn't violate
those principles which are the Standard C# Conventions and the SOLID principle. The Standard
C# Convention, this has to do with the naming of namespaces, classes etc. Whether it is PascalCase
or camelCase and being clear with the naming of variables (e.g. naming your variable UserG instead
of UserGroup). The SOLID principle is the acronym for Single responsibility principle, Open/Closed
principle, Liskov substitution, Interface Segregation Principle, and Dependency inversion principle.
I could go over each one but I can assure you that it doesn't violate any of these principles.

