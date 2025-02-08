# C# Classes and Objects

You learned from the previous chapter that C# is an object-oriented programming language.

Everything in C# is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an object. The car has **attributes**, such as weight and color, and **methods**, such as drive and brake.

A Class is like an object constructor, or a "blueprint" for creating objects.

## Create a Class

To create a class, use the `class` keyword:

Create a class named "`Car`" with a variable `color`:

```cs
class Car
{
  string color = "red";
}
```

> When a variable is declared directly in a class, it is often referred to as a **field** (or attribute).<br>It is not required, but it is a good practice to start with an uppercase first letter when naming classes. Also, it is common that the name of the C# file and the class matches, as it makes our code organized. However it is not required (like in Java).

## Create an Object

An object is created from a class. We have already created the class named `Car`, so now we can use this to create objects.

To create an object of `Car`, specify the class name, followed by the object name, and use the keyword `new`:

**Example:**

Create an object called "`myObj`" and use it to print the value of `color`:

```cs
class Car
{
  string color = "red";

  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.color);
  }
}
```

> Note that we use the dot syntax (`.`) to access variables/fields inside a class (`myObj.color`). You will learn more about fields in the next chapter.

## Multiple Objects

You can create multiple objects of one class:

**Example:**

Create two objects of `Car`:

```cs
class Car
{
  string color = "red";
  static void Main(string[] args)
  {
    Car myObj1 = new Car();
    Car myObj2 = new Car();
    Console.WriteLine(myObj1.color);
    Console.WriteLine(myObj2.color);
  }
}
```

## Using Multiple Classes

You can also create an object of a class and access it in another class. This is often used for better organization of classes (one class has all the fields and methods, while the other class holds the `Main()` method (code to be executed)).

- prog2.cs
- prog.cs

**prog2.cs**

```cs
class Car
{
  public string color = "red";
}
```

**prog.cs**

```cs
class Program
{
  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.color);
  }
}
```

> Did you notice the `public` keyword? It is called an **access modifier**, which specifies that the `color` variable/field of `Car` is accessible for other classes as well, such as `Program`.<br>You will learn much more about **access modifiers** and **classes/objects** in the next chapters.

# 📜 References

- [C# Classes and Objects](https://www.w3schools.com/cs/cs_classes.php)
- [C# Multiple Classes and Objects](https://www.w3schools.com/cs/cs_classes_multi.php)
