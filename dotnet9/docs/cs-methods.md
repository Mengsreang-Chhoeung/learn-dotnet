# C# Methods

A **method** is a block of code which only runs when it is called.

You can pass data, known as parameters, into a method.

Methods are used to perform certain actions, and they are also known as **functions**.

Why use methods? To reuse code: define the code once, and use it many times.

## Create a Method

A method is defined with the name of the method, followed by parentheses **()**. C# provides some pre-defined methods, which you already are familiar with, such as `Main()`, but you can also create your own methods to perform certain actions:

**Example:**

Create a method inside the Program class:

```cs
class Program
{
  static void MyMethod()
  {
    // code to be executed
  }
}
```

**Example Explained:**

- `MyMethod()` is the name of the method
- `static` means that the method belongs to the Program class and not an object of the Program class. You will learn more about objects and how to access methods through objects later in this tutorial.
- `void` means that this method does not have a return value. You will learn more about return values later in this chapter

> **Note:** In C#, it is good practice to start with an uppercase letter when naming methods, as it makes the code easier to read.

## Call a Method

To call (execute) a method, write the method's name followed by two parentheses **()** and a semicolon;

In the following example, `MyMethod()` is used to print a text (the action), when it is called:

**Example:**

Inside `Main()`, call the `myMethod()` method:

```cs
static void MyMethod()
{
  Console.WriteLine("I just got executed!");
}

static void Main(string[] args)
{
  MyMethod();
}

// Outputs "I just got executed!"
```

A method can be called multiple times:

**Example:**

```cs
static void MyMethod()
{
  Console.WriteLine("I just got executed!");
}

static void Main(string[] args)
{
  MyMethod();
  MyMethod();
  MyMethod();
}

// I just got executed!
// I just got executed!
// I just got executed!
```

# 📜 References

- [C# Methods](https://www.w3schools.com/cs/cs_methods.php)
