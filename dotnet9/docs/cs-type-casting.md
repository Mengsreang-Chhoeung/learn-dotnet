# C# Type Casting

Type casting is when you assign a value of one data type to another type.

In C#, there are two types of casting:

- **Implicit Casting (automatically) -** converting a smaller type to a larger type size
  `char` -> `int` -> `long` -> `float` -> `double`

- **Explicit Casting (manually) -** converting a larger type to a smaller size type
  `double` -> `float` -> `long` -> `int` -> `char`

## Implicit Casting

Implicit casting is done automatically when passing a smaller size type to a larger size type:

**Example:**

```cs
int myInt = 9;
double myDouble = myInt;       // Automatic casting: int to double

Console.WriteLine(myInt);      // Outputs 9
Console.WriteLine(myDouble);   // Outputs 9
```

## Explicit Casting

Explicit casting must be done manually by placing the type in parentheses in front of the value:

**Example:**

```cs
double myDouble = 9.78;
int myInt = (int) myDouble;    // Manual casting: double to int

Console.WriteLine(myDouble);   // Outputs 9.78
Console.WriteLine(myInt);      // Outputs 9
```

## Type Conversion Methods

It is also possible to convert data types explicitly by using built-in methods, such as `Convert.ToBoolean`, `Convert.ToDouble`, `Convert.ToString`, `Convert.ToInt32` (`int`) and `Convert.ToInt64` (`long`):

**Example:**

```cs
int myInt = 10;
double myDouble = 5.25;
bool myBool = true;

Console.WriteLine(Convert.ToString(myInt));    // convert int to string
Console.WriteLine(Convert.ToDouble(myInt));    // convert int to double
Console.WriteLine(Convert.ToInt32(myDouble));  // convert double to int
Console.WriteLine(Convert.ToString(myBool));   // convert bool to string
```

> **Why Conversion?** <br> Many times, there's no need for type conversion. But sometimes you have to. Take a look at the next chapter, when working with [user input](./cs-user-input.md), to see an example of this.

# 📜 References

- [C# Type Casting](https://www.w3schools.com/cs/cs_type_casting.php)
