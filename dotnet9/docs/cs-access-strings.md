# C# Access Strings

You can access the characters in a string by referring to its index number inside square brackets `[]`.

This example prints the **first character** in **myString**:

**Example:**

```cs
string myString = "Hello";
Console.WriteLine(myString[0]);  // Outputs "H"
```

> **Note:** String indexes start with 0: [0] is the first character. [1] is the second character, etc.

This example prints the **second character** (1) in **myString**:

**Example:**

```cs
string myString = "Hello";
Console.WriteLine(myString[1]);  // Outputs "e"
```

You can also find the index position of a specific character in a string, by using the `IndexOf()` method:

**Example:**

```cs
string myString = "Hello";
Console.WriteLine(myString.IndexOf("e"));  // Outputs "1"
```

Another useful method is `Substring()`, which extracts the characters from a string, starting from the specified character position/index, and returns a new string. This method is often used together with `IndexOf()` to get the specific character position:

**Example:**

```cs
// Full name
string name = "John Doe";

// Location of the letter D
int charPos = name.IndexOf("D");

// Get last name
string lastName = name.Substring(charPos);

// Print the result
Console.WriteLine(lastName);
```

# 📜 References

- [C# Access Strings](https://www.w3schools.com/cs/cs_strings_access.php)
