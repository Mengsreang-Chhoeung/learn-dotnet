# C# Foreach Loop

There is also a `foreach` loop, which is used exclusively to loop through elements in an **array** (or other data sets):

**Syntax:**

```cs
foreach (type variableName in arrayName)
{
  // code block to be executed
}
```

The following example outputs all elements in the **cars** array, using a `foreach` loop:

**Example:**

```cs
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
foreach (string i in cars)
{
  Console.WriteLine(i);
}
```

> **Note:** Don't worry if you don't understand the example above. You will learn more about Arrays in the C# Arrays chapter.

# 📜 References

- [C# Foreach Loop](https://www.w3schools.com/cs/cs_foreach_loop.php)
