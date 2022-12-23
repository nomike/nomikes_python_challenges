# Chapter 2.1 - Your first interactive python session

As you can see in the example above, the python interpreter prints some information to the screen first. It tells you that it's Python, which version of it and a couple of other things which are not important right now.

It tells you how to get help, the copyright message and so on. And then it waits for you to enter commands by displaying a prompt.

That prompt is the same concept as with your shell but instead of `nomike@max:~$` it simply is `>>>`.

You can then do simple calculations for example:

```plaintext
>>> 10 + 32
42
>>> 
```

and now you finally know the answer to the big question about life and everything.

You can use other mathematical operators and even brackets:

```plaintext
>>> (2 + 4) * 10
60
>>> 
```

## Exiting the interpreter

Before you continue to read, what would be your approach of exiting your interactive python session?

You've already learned that you can exit your shell with `exit` and an interactive python session is essentially just another shell.

```plaintext
>>> exit
Use exit() or Ctrl-D (i.e. EOF) to exit
>>> exit()
```

Python really tries to be helpful and beginner friendly and politely tells you that in order to exit you either need to use the `exit()` command or press Ctrl-D on your keyboard.

## Printing text to the terminal

As adding numbers quickly gets boring, let's do what we've all been waiting for: Let's greet the world!

```plaintext
>>> print("hello, world")
hello, world
```

What this does is to invoke the function called "print" and pass the parameter "hello, world" to it.
The python interpreter converts this to a big number of machine code which is then executed by the CPU and at some point you end up with the text "hello, world" on your terminal.

You can think of functions as they are in mathematics (e.g. "f(x) = 2 * x") as they work exactly the same.

In python "f(x) = 2 * x" would look like this for example:

```python
def f(x):
    return 2 * x
```

The syntax is a bit different, but you see the similarities.

Somewhere in the depths of the python source code, is a definition of the `print` function.

## Strings

In the hello world example the text "hello, world" is passed to the `print` function.
You have seen that numbers could just be entered literally when we added 10 + 32 above.
If you want to represent text however, you need to tell python that you mean this as literal text

This could be done by wrapping it in double quotes.

So for example `print` refers to the function with that name, `"print"` however, refers to the literal text.

You can see this in the hello world example above.

## Variables

Like in mathematics you can have variables in programming languages which can store all kinds of data for you:

```python
a = 10
print(10 + a)
print(a * 2 + 14)
b = 20
c = a + b
print(c)

name = "nomike"
print(name)
```

## Math influences

As programming drew a lot of inspiration from mathematics, most of the rules are the same, for example operator precedence (e.g. point before line) as seen in the example above.

## A word on parentheses

There could be endless debates on social media about whether the answer to `8 / 2 * (2 + 2)` is 1 or 16 (try putting this into an interactive python session to get the right answer), programming code should not be up for debate at all. It is thus advisable to use parentheses in this case:

`(8 / 2) * (2 + 2)`

Now it's much more obvious.

## Operators

Basic operators look a bit different then what you're used to. The symbols for addition and subtraction are as you'd expect: `+` and `-`.

For Multiplication however, you will realize that the common math symbol could not be found on your computer keyboard. While modern computers could use and display the multiplication dot (`⋅`) it is not used in programming and most language use a simple star `*` for that.

The same applies to division where the common symbol `÷` was substituted by a forward slash `/`.

## Assignment

As shown in the example above, you can use the equals symbol to assign a value to a variable:

```python
a = 10
```

## Comparison

This puts us in a dilemma though. In school we have learned that you could compare two variables like that:

```plaintext
a = 10
```

But in python rather than comparing whether the data stored in variable `a` equals to 10, it will assign 10 to the variable.

The way this was solved is to use two equals symbols for comparing things:

```python
a == 10
```

There are other comparison operators as well, such as `&gt;`, `&lt;`,`&gt;=` and `&lt;=`.
If you want to check whether one term not equals another, you can use `!=1`:

```python
a != 10
```

## Basic variable types

A variable could contain different things and might behave differently based on the type of data.

### Integers

Wikipedia defines an integer as "a real number that can be written without a fractional component.", but it might be easier to understand as "a number without a comma."

Examples of integers are

```plaintext
10
0
-134
12345
```

### Floats

Computers need to represent every number in binary and the most common method for storing numbers with comma is the floating point representation. Here are some examples:

```python
1.4
0.4
.9
-2.0
-.14
```

As you can see, the `0` could be omitted, but IMHO it makes the code less readable so you should try to avoid that.

### Characters

A character is one symbol which could be printed to screen (e.g. 'a' or '^').

### Strings are lists of characters

Multiple characters in a list are called a string. You have seen this in previous examples already.

### Booleans

Whereas elementary algebra deals with numbers, boolean algebra deals with truth-values. Something could either be true or false.

When you use comparisons for example, the result is a boolean:

```plaintext
>>> a = 10
>>> a >= 4
True
>>> a > 4
True
>>> a == 11
False
```

## Boolean operators

The presence of booleans also requires the addition of a couple of more operators. Similar to mathematics you can use the keywords `and`, `or` and `not`:

```plaintext
>>> a = 10
>>> b = 20
>>> (a > 5) and (b < 20)
False
>>> (a > 5) or (b < 20)
True
>>> not ((a > 5) or (b < 20))
False
```

This chapter again doesn't have an exercise. If you followed along with the examples, you should have had the opportunity to play around in an interactive python session already. So go straight on to [chapter 2.2](../2.2/) which is all about storing python code in files and requesting input from the user. It will also include the first programming challenge. I promise!
