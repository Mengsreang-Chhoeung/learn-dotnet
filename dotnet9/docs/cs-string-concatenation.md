# C# String Concatenation

The `+` operator can be used between strings to combine them. This is called **concatenation**:

**Example:**

```cs
string firstName = "John ";
string lastName = "Doe";
string name = firstName + lastName;
Console.WriteLine(name);
```

> Note that we have added a space after "John" to create a space between firstName and lastName on print.

You can also use the `string.Concat()` method to concatenate two strings:

**Example:**

```cs
string firstName = "John ";
string lastName = "Doe";
string name = string.Concat(firstName, lastName);
Console.WriteLine(name);
```

## Adding Numbers and Strings

> **WARNING!**<br>C# uses the `+` operator for both **addition** and **concatenation**.<br>**Remember:** Numbers are added. Strings are concatenated.

If you add two numbers, the result will be a number:

**Example:**

```cs
int x = 10;
int y = 20;
int z = x + y;  // z will be 30 (an integer/number)
```

If you add two strings, the result will be a string concatenation:

**Example:**

```cs
string x = "10";
string y = "20";
string z = x + y;  // z will be 1020 (a string)
```

# 📜 References

- [C# String Concatenation](https://www.w3schools.com/cs/cs_strings_concat.php)
