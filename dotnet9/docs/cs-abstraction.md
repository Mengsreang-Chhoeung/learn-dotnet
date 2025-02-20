# C# Abstraction

## Abstract Classes and Methods

Data **abstraction** is the process of hiding certain details and showing only essential information to the user.

Abstraction can be achieved with either **abstract** **classes** or [**interfaces**](./cs-interface.md) (which you will learn more about in the next chapter).

The `abstract` keyword is used for classes and methods:

- **Abstract class:** is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).
- **Abstract method:** can only be used in an abstract class, and it does not have a body. The body is provided by the derived class (inherited from).

An abstract class can have both abstract and regular methods:

```cs
abstract class Animal
{
  public abstract void animalSound();
  public void sleep()
  {
    Console.WriteLine("Zzz");
  }
}
```

From the example above, it is not possible to create an object of the Animal class:

```cs
Animal myObj = new Animal(); // Will generate an error (Cannot create an instance of the abstract class or interface 'Animal')
```

To access the abstract class, it must be inherited from another class. Let's convert the Animal class we used in the [Polymorphism chapter](./cs-polymorphism.md) to an abstract class.

> Remember from the [Inheritance chapter](./cs-inheritance.md) that we use the `:` symbol to inherit from a class, and that we use the `override` keyword to override the base class method.

**Example:**

```cs
// Abstract class
abstract class Animal
{
  // Abstract method (does not have a body)
  public abstract void animalSound();
  // Regular method
  public void sleep()
  {
    Console.WriteLine("Zzz");
  }
}

// Derived class (inherit from Animal)
class Pig : Animal
{
  public override void animalSound()
  {
    // The body of animalSound() is provided here
    Console.WriteLine("The pig says: wee wee");
  }
}

class Program
{
  static void Main(string[] args)
  {
    Pig myPig = new Pig(); // Create a Pig object
    myPig.animalSound();  // Call the abstract method
    myPig.sleep();  // Call the regular method
  }
}
```

> **Why And When To Use Abstract Classes and Methods?**<br>To achieve security - hide certain details and only show the important details of an object.<br>**Note:** Abstraction can also be achieved with [Interfaces](./cs-interface.md), which you will learn more about in the next chapter.

# 📜 References

- [C# Abstraction](https://www.w3schools.com/cs/cs_abstract.php)
