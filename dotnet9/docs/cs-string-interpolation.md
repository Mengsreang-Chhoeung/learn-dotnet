# C# String Interpolation

Another option of [string concatenation](./cs-string-concatenation.md), is **string interpolation**, which substitutes values of variables into placeholders in a string. Note that you do not have to worry about spaces, like with concatenation:

**Example:**

```cs
string firstName = "John";
string lastName = "Doe";
string name = $"My full name is: {firstName} {lastName}";
Console.WriteLine(name);
```

> Also note that you have to use the dollar sign (`$`) when using the string interpolation method.<br>String interpolation was introduced in C# version 6.

# 📜 References

- [C# String Interpolation](https://www.w3schools.com/cs/cs_strings_interpol.php)
