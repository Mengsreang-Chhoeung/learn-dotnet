# C# Comments

Comments can be used to explain C# code, and to make it more readable. It can also be used to prevent execution when testing alternative code.

## Single-line Comments

Single-line comments start with two forward slashes (`//`).

Any text between `//` and the end of the line is ignored by C# (will not be executed).

This example uses a single-line comment before a line of code:

**Example:**

```cs
// This is a comment
Console.WriteLine("Hello World!");
```

This example uses a single-line comment at the end of a line of code:

**Example:**

```cs
Console.WriteLine("Hello World!");  // This is a comment
```

## Multi-line Comments

Multi-line comments start with `/*` and ends with `*/`.

Any text between `/*` and `*/` will be ignored by C#.

This example uses a multi-line comment (a comment block) to explain the code:

**Example:**

```cs
/* The code below will print the words Hello World
to the screen, and it is amazing */
Console.WriteLine("Hello World!");
```

> **Single or multi-line comments?** <br> It is up to you which you want to use. Normally, we use `//` for short comments, and `/* */` for longer.

# 📜 References

- [C# Comments](https://www.w3schools.com/cs/cs_comments.php)
