# C# Class Members

Fields and methods inside classes are often referred to as "Class Members":

**Example:**

Create a `Car` class with three class members: **two fields** and **one method**.

```cs
// The class
class MyClass
{
  // Class members
  string color = "red";        // field
  int maxSpeed = 200;          // field
  public void fullThrottle()   // method
  {
    Console.WriteLine("The car is going as fast as it can!");
  }
}
```

## Fields

In the previous chapter, you learned that variables inside a class are called fields, and that you can access them by creating an object of the class, and by using the dot syntax (`.`).

The following example will create an object of the `Car` class, with the name `myObj`. Then we print the value of the fields `color` and `maxSpeed`:

**Example:**

```cs
class Car
{
  string color = "red";
  int maxSpeed = 200;

  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.color);
    Console.WriteLine(myObj.maxSpeed);
  }
}
```

You can also leave the fields blank, and modify them when creating the object:

**Example:**

```cs
class Car
{
  string color;
  int maxSpeed;

  static void Main(string[] args)
  {
    Car myObj = new Car();
    myObj.color = "red";
    myObj.maxSpeed = 200;
    Console.WriteLine(myObj.color);
    Console.WriteLine(myObj.maxSpeed);
  }
}
```

This is especially useful when creating multiple objects of one class:

**Example:**

```cs
class Car
{
  string model;
  string color;
  int year;

  static void Main(string[] args)
  {
    Car Ford = new Car();
    Ford.model = "Mustang";
    Ford.color = "red";
    Ford.year = 1969;

    Car Opel = new Car();
    Opel.model = "Astra";
    Opel.color = "white";
    Opel.year = 2005;

    Console.WriteLine(Ford.model);
    Console.WriteLine(Opel.model);
  }
}
```

## Object Methods

You learned from the [C# Methods](./cs-methods.md) chapter that methods are used to perform certain actions.

Methods normally belong to a class, and they define how an object of a class behaves.

Just like with fields, you can access methods with the dot syntax. However, note that the method must be `public`. And remember that we use the name of the method followed by two parentheses `()` and a semicolon `;` to call (execute) the method:

**Example:**

```cs
class Car
{
  string color;                 // field
  int maxSpeed;                 // field
  public void fullThrottle()    // method
  {
    Console.WriteLine("The car is going as fast as it can!");
  }

  static void Main(string[] args)
  {
    Car myObj = new Car();
    myObj.fullThrottle();  // Call the method
  }
}
```

> Why did we declare the method as `public`, and not `static`, like in the examples from the [C# Methods Chapter](./cs-methods.md)?
> <br>The reason is simple: a `static` method can be accessed without creating an object of the class, while `public` methods can only be accessed by objects.

## Use Multiple Classes

Remember from the last chapter, that we can use multiple classes for better organization (one for fields and methods, and another one for execution). This is recommended:

**prog2.cs**

```cs
class Car
{
  public string model;
  public string color;
  public int year;
  public void fullThrottle()
  {
    Console.WriteLine("The car is going as fast as it can!");
  }
}
```

**prog.cs**

```cs
class Program
{
  static void Main(string[] args)
  {
    Car Ford = new Car();
    Ford.model = "Mustang";
    Ford.color = "red";
    Ford.year = 1969;

    Car Opel = new Car();
    Opel.model = "Astra";
    Opel.color = "white";
    Opel.year = 2005;

    Console.WriteLine(Ford.model);
    Console.WriteLine(Opel.model);
  }
}
```

> The `public` keyword is called an **access modifier**, which specifies that the fields of `Car` are accessible for other classes as well, such as `Program`.
> <br>You will learn more about Access Modifiers in a later chapter.
> <br>**Tip:** As you continue to read, you will also learn more about other class members, such as constructors and properties.

# 📜 References

- [C# Class Members](https://www.w3schools.com/cs/cs_class_members.php)
