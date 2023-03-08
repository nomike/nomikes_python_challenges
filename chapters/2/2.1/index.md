# Chapter 2.1 - Your first interactive python session

[TOC]

## Starting an interactive session

In your terminal start python:

```plaintext
nomike@max:~$ python
Python 3.10.7 (main, Nov 24 2022, 19:45:47) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> ```

As you can see in the example above, the python interpreter prints some information to the screen first. It tells you that it's Python, which version of it and a couple of other things which are not important right now.

It tells you how to get help, the copyright message and so on. And then it waits for you to enter commands by displaying a prompt.

That prompt is the same concept as with your shell but instead of `nomike@max:~$ ` it simply is `>>>`.

On this prompt you can do simple calculations. For example:

```plaintext
>>> 10 + 32
42
>>> 
```

And now you finally know the answer to the big question about life and everything.

You can use other mathematical operators and even brackets:

```plaintext
>>> (2 + 4) * 10
60
>>> 
```

## Exiting the interpreter

Before you continue to read, try to think of what your approach of exiting this interactive python session would be.

You've already learned, that you can exit your shell with the `exit` command.
An interactive python session is essentially just another shell so lets try using `exit`:

```plaintext
>>> exit
Use exit() or Ctrl-D (i.e. EOF) to exit
>>> exit()
```

Python really tries to be helpful and beginner-friendly and politely tells you that in order to exit you either need to use the `exit()` command or press Ctrl-D on your keyboard. I just used the "exit()" command to return back to my shell.

***Tip:** If you are in the shell, you can exit it with Ctrl-D as well, that's a nice bit of consistency!*

## Printing text to the terminal

Adding numbers quickly gets boring. Let's do, what all programmers do in their first ever program: Let's greet the world!

```plaintext
>>> print("hello, world")
hello, world
```

Not surprisingly, this has the effect of printing the text "hello, world" to your screen.
What happens is, that a function called "print" is called and the parameter "hello, world" is given to it. This function then somehow takes care of sending the text to the terminal, which then takes care of displaying it on your screen.

The python interpreter converts all of this this into a big chunk of machine code, which is then executed by the CPU, and at some point you end up with the text "hello, world" on your terminal.

## Functions

Functions in python are similar to functions in in mathematics e.g. "f(x) = 2 * x".
In python that function would look like this:

```python
def f(x):
    return 2 * x
```

The syntax is a bit different, but you probably recognize the similarities.

And somewhere in the sheer endless depths of the python source code, there is a definition of the `print` function.

## Variables

Like in mathematics you can have variables in programming languages which can store all kinds of data for you:

```python
a = 10
print(10 + a)
print(a * 2 + 14)
b = 20
c = a + b
print(c)
```

## Math influences

As programming drew a lot of inspiration from mathematics, most of the rules are the same. For example operator precedence (e.g. point before line) works the same. as seen in the example above.

## A word on parentheses

While there could be endless debates on social media about whether the answer to `8 / 2 * (2 + 2)` is 1 or 16, programming code should not be up for debate at all (try putting this into an interactive python session to get the right answer). To make code predictable and easy to understand it is advisable to use parentheses in this case:

`(8 / 2) * (2 + 2)`

Now it's much more obvious what's happening.

## Operators

Basic operators look a bit different then what you're used to. The symbols for addition and subtraction are as you'd expect: `+` and `-`.

For Multiplication however, you will realize that the common math symbol for that could not be found on your computer keyboard. While modern computers could use and display the multiplication dot (`⋅`) it is not used in programming and most programming languages adopted a simple star `*` for that.

The same applies to division where the division symbol `÷` was substituted by a forward slash `/`.

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

But in python rather than comparing whether the data stored in variable `a` equals 10, it will assign 10 to the variable.

The way this was solved, is to use two equals symbols for comparing things:

```python
a == 10
```

There are other comparison operators as well, such as `>`, `<`,`>=` and `<=`.
If you want to check whether one term not equals another, you can use `!=`:

```python
a != 10
```

## Basic variable types

A variable could contain different kinds of things and might behave differently based on the type of data. I will show you some examples soon,

### Integers

Wikipedia defines an integer as "a real number that can be written without a fractional component.", but it might be easier to understand as "a number without a comma.".

Examples of integers are

```plaintext
10
0
-134
12345
```

### Floats

Numbers with fractions are called floats and they look like this:

```python
1.4
0.4
.9
-2.0
-.14
```

As you can see, the `0` before the comma could be omitted, but in my opinion it makes the code less readable, so you should better include it.

### Characters

A character is one symbol which could be printed to screen (e.g. 'a' or '?').

### Strings are lists of characters

Multiple characters in a list are called a string. You have seen this in previous examples already.

They need to be enclosed in double quotes so that python knows you literally mean the text "print" and not the function with the same name.

### Booleans

Whereas elementary algebra deals with numbers, boolean algebra deals with truth-values. Something could either be true or false.

When you use comparisons for example, the result is always a boolean:

```plaintext
>>> a = 10
>>> a >= 4
True
>>> a > 4
True
>>> a == 11
False
```

Boolean values are represented by the keywords `True` and `False`.

***Note:** In contrast to some other programming languages (C, C++, Java, etc.) those keywords are written with uppercase first letters.*

## Boolean operators

Now that we have booleans, we also need a couple of more operators. Similar to mathematics you can use the keywords `and`, `or` and `not`:

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

## The nothing

The value of variable could be nothing. That's different to `0` for example, which is something.

> (Pyornkrachzark) Near my home, there used to be a beautiful lake, but then... then it was gone.
> 
> (Gluckuk) Did the lake dry up?
> 
> (Pyornkrachzark) No. It just wasn't there anymore. Nothing was there anymore. Not even a dried-up lake.
> 
> (Gluckuk) A hole?
> 
> (Pyornkrachzark) A hole would be something. No, it was Nothing.

The keyword for nothing used in python is `None`.

```python
a = None
```

You can use it in case you don't know a value yet or if it is not defined.

## Modulo

Module is an operator which you might not have heard of yet, as it's not commonly used in mathematics.
It gives you the remainder of an integer division. The symbol used for this is `%`.

If you divide a by b, modulo tells you the remainder of that division:

```python
5 % 2 == 1
```

Or spelled out: 5 equals 2 times 2 plus 1

```python
12 % 3 == 0
```

12 equals 4 times 3 plus 0

## Dynamic typing

Python is dynamically typed. This means that the type of a variable is determined during runtime and not during programming.

In Java for example you need write code like this:

```java
String hello = "Hello world!";
int a = 5;
Integer b = 6;

hello = a;  // This will cause a compile error as a doesn't have the correct data type
```

In python you don't have to write data types for variables:

```python
hello = "Hello world!"
a = 5
b = 6

hello = a   # This will work just fine
```

While the program is executed, the compiler does determine the type of the variable though.

Dynamic typing makes coding easier, less cumbersome and more flexible. It comes with the drawback however, that it's easier for you to mess things up, as your IDE can't easily wan you when you are using incompatible data types somewhere.

A solution for this are type hints, which have been introduced in python 3.5:

```python
a: int = 4
name: str

name = "nomike"
a = "hello"
```

This program will execute without issues, python is still dynamically typed. But if you're using an IDE, it might point out that you might have an error in your code.

For the moment, we will progress without type hints and I will explain them in more detail in a later chapter.

## Conclusion

This chapter again doesn't have an exercise. If you followed along with the examples, you should have had the opportunity to play around in an interactive python session already. So go straight on to [chapter 2.2](../2.2/) which is all about storing python code in files and requesting input from the user. It will also include the first programming challenge. I promise!
