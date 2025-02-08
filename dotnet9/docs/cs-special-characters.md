# C# Special Characters

Because strings must be written within quotes, C# will misunderstand this string, and generate an error:

```cs
string txt = "We are the so-called "Vikings" from the north.";
```

The solution to avoid this problem, is to use the **backslash escape character**.

The backslash (`\`) escape character turns special characters into string characters:

| Escape character | Result | Description  |
| ---------------- | ------ | ------------ |
| \\'              | '      | Single quote |
| \\"              | "      | Double quote |
| \\\              | \      | Backslash    |

The sequence `\"` inserts a double quote in a string:

**Example:**

```cs
string txt = "We are the so-called \"Vikings\" from the north.";
```

The sequence `\'` inserts a single quote in a string:

**Example:**

```cs
string txt = "It\'s alright.";
```

The sequence `\\` inserts a single backslash in a string:

**Example:**

```cs
string txt = "The character \\ is called backslash.";
```

Other useful escape characters in C# are:

| Code | Result    |
| ---- | --------- |
| \n   | New Line  |
| \t   | Tab       |
| \b   | Backspace |

# 📜 References

- [C# Special Characters](https://www.w3schools.com/cs/cs_strings_chars.php)
