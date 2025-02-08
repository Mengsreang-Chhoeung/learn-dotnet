# C# Method Parameters

## Parameters and Arguments

Information can be passed to methods as parameter. Parameters act as variables inside the method.

They are specified after the method name, inside the parentheses. You can add as many parameters as you want, just separate them with a comma.

The following example has a method that takes a `string` called **fname** as parameter. When the method is called, we pass along a first name, which is used inside the method to print the full name:

**Example:**

```cs
static void MyMethod(string fname)
{
  Console.WriteLine(fname + " Refsnes");
}

static void Main(string[] args)
{
  MyMethod("Liam");
  MyMethod("Jenny");
  MyMethod("Anja");
}

// Liam Refsnes
// Jenny Refsnes
// Anja Refsnes
```

> When a **parameter** is passed to the method, it is called an **argument**. So, from the example above: `fname` is a parameter, while `Liam`, `Jenny` and `Anja` are **arguments**.

## Multiple Parameters

You can have as many parameters as you like, just separate them with commas:

**Example:**

```cs
static void MyMethod(string fname, int age)
{
  Console.WriteLine(fname + " is " + age);
}

static void Main(string[] args)
{
  MyMethod("Liam", 5);
  MyMethod("Jenny", 8);
  MyMethod("Anja", 31);
}

// Liam is 5
// Jenny is 8
// Anja is 31
```

> Note that when you are working with multiple parameters, the method call must have the same number of arguments as there are parameters, and the arguments must be passed in the same order.

## Default Parameter Value

You can also use a default parameter value, by using the equals sign (`=`).

If we call the method without an argument, it uses the default value ("Norway"):

**Example:**

```cs
static void MyMethod(string country = "Norway")
{
  Console.WriteLine(country);
}

static void Main(string[] args)
{
  MyMethod("Sweden");
  MyMethod("India");
  MyMethod();
  MyMethod("USA");
}

// Sweden
// India
// Norway
// USA
```

> A parameter with a default value, is often known as an **"optional parameter"**. From the example above, `country` is an optional parameter and `"Norway"` is the default value.

## Return Values

In the [Parameters & Arguments](#parameters-and-arguments) section, we used the `void` keyword in all examples, which indicates that the method should not return a value.

If you want the method to return a value, you can use a primitive data type (such as `int` or `double`) instead of `void`, and use the `return` keyword inside the method:

**Example:**

```cs
static int MyMethod(int x)
{
  return 5 + x;
}

static void Main(string[] args)
{
  Console.WriteLine(MyMethod(3));
}

// Outputs 8 (5 + 3)
```

This example returns the sum of a method's **two parameters**:

**Example:**

```cs
static int MyMethod(int x, int y)
{
  return x + y;
}

static void Main(string[] args)
{
  Console.WriteLine(MyMethod(5, 3));
}

// Outputs 8 (5 + 3)
```

You can also store the result in a variable (recommended, as it is easier to read and maintain):

**Example:**

```cs
static int MyMethod(int x, int y)
{
  return x + y;
}

static void Main(string[] args)
{
  int z = MyMethod(5, 3);
  Console.WriteLine(z);
}

// Outputs 8 (5 + 3)
```

## Named Arguments

It is also possible to send arguments with the _`key: value`_ syntax.

That way, the order of the arguments does not matter:

**Example:**

```cs
static void MyMethod(string child1, string child2, string child3)
{
  Console.WriteLine("The youngest child is: " + child3);
}

static void Main(string[] args)
{
  MyMethod(child3: "John", child1: "Liam", child2: "Liam");
}

// The youngest child is: John
```

# 📜 References

- [C# Method Parameters](https://www.w3schools.com/cs/cs_method_parameters.php)
- [C# Default Parameter Value](https://www.w3schools.com/cs/cs_method_parameters_default.php)
- [C# Return Values](https://www.w3schools.com/cs/cs_method_parameters_return.php)
- [C# Named Arguments](https://www.w3schools.com/cs/cs_method_parameters_named_args.php)
