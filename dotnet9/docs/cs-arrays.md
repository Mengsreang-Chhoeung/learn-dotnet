# C# Arrays

## Create an Array

Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

To declare an array, define the variable type with **square brackets**:

```cs
string[] cars;
```

We have now declared a variable that holds an array of strings.

To insert values to it, we can use an array literal - place the values in a comma-separated list, inside curly braces:

```cs
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

To create an array of integers, you could write:

```cs
int[] myNum = {10, 20, 30, 40};
```

## Access the Elements of an Array

You access an array element by referring to the index number.

This statement accesses the value of the first element in **cars**:

**Example:**

```cs
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Console.WriteLine(cars[0]);
// Outputs Volvo
```

> **Note:** Array indexes start with 0: [0] is the first element. [1] is the second element, etc.

## Change an Array Element

To change the value of a specific element, refer to the index number:

**Example:**

```cs
cars[0] = "Opel";
```

**Example:**

```cs
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
Console.WriteLine(cars[0]);
// Now outputs Opel instead of Volvo
```

## Array Length

To find out how many elements an array has, use the `Length` property:

**Example:**

```cs
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Console.WriteLine(cars.Length);
// Outputs 4
```

## Other Ways to Create an Array

If you are familiar with C#, you might have seen arrays created with the `new` keyword, and perhaps you have seen arrays with a specified size as well. In C#, there are different ways to create an array:

```cs
// Create an array of four elements, and add values later
string[] cars = new string[4];

// Create an array of four elements and add values right away
string[] cars = new string[4] {"Volvo", "BMW", "Ford", "Mazda"};

// Create an array of four elements without specifying the size
string[] cars = new string[] {"Volvo", "BMW", "Ford", "Mazda"};

// Create an array of four elements, omitting the new keyword, and without specifying the size
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

It is up to you which option you choose. In our tutorial, we will often use the last option, as it is faster and easier to read.

However, you should note that if you declare an array and initialize it later, you have to use the `new` keyword:

```cs
// Declare an array
string[] cars;

// Add values, using new
cars = new string[] {"Volvo", "BMW", "Ford"};

// Add values without using new (this will cause an error)
cars = {"Volvo", "BMW", "Ford"};
```

# 📜 References

- [C# Arrays](https://www.w3schools.com/cs/cs_arrays.php)
