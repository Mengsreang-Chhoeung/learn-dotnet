# C# Break and Continue

## C# Break

You have already seen the `break` statement used in an earlier chapter of this tutorial. It was used to "jump out" of a `switch` statement.

The `break` statement can also be used to jump out of a **loop**.

This example jumps out of the loop when `i` is equal to `4`:

**Example:**

```cs
for (int i = 0; i < 10; i++)
{
  if (i == 4)
  {
    break;
  }
  Console.WriteLine(i);
}
```

## C# Continue

The `continue` statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

This example skips the value of `4`:

**Example:**

```cs
for (int i = 0; i < 10; i++)
{
  if (i == 4)
  {
    continue;
  }
  Console.WriteLine(i);
}
```

## Break and Continue in While Loop

You can also use `break` and `continue` in while loops:

**Break Example:**

```cs
int i = 0;
while (i < 10)
{
  Console.WriteLine(i);
  i++;
  if (i == 4)
  {
    break;
  }
}
```

**Continue Example:**

```cs
int i = 0;
while (i < 10)
{
  if (i == 4)
  {
    i++;
    continue;
  }
  Console.WriteLine(i);
  i++;
}
```

# 📜 References

- [C# Break and Continue](https://www.w3schools.com/cs/cs_break.php)
